# Step Debugger

The step debugger shows you step by step what happens in your patch after a trigger or value change: which ops run, which ports are triggered and how values change.

![](img/stepdebugger.png)

## Usage

1. Add `StepDebugTrigger` or `StepDebugNumber` where you want to start recording
   - `StepDebugTrigger`: add it to a trigger chain to record everything that happens after it is triggered
   - `StepDebugNumber`: add it to a number connection to record everything that happens when the value changes
2. Open **Patch Debugger** in the editor menu, or open the command palette (`[mod] + p`) and enter `Patch Debugger`

The list shows every step in order:
- the op name
- `in` or `out`, and the port
- for values: old value → new value

Use **clear** to empty the list.

## Tips

- Give each op a `Title` to see in the list where a recording started
- Switch off `Active` to stop recording without removing the op
- Recording a trigger that runs every frame fills up the list very fast: use it on triggers that happen only once, like a button or a change, or try using TriggerOnce Operator

## Op links
- [StepDebugTrigger](/op/Ops.Debug.StepDebugger.StepDebugTrigger)
- [StepDebugNumber](/op/Ops.Debug.StepDebugger.StepDebugNumber)
