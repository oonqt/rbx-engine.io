## Installation

```npm install rbx-engine.io```

## Example

```ts
import Engine from 'rbx-engine.io'
const Socket = new Engine<string>() // Connects to localhost

Socket.On('open', () => {
	print('Connected')
	Socket.Send('test')
})

Socket.On('message', (data) => {
	print(`Message recieved: ${data}`)
})

Socket.On('close', (data) => {
	print('Disconnected')
})
```
