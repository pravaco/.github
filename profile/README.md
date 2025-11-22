Open sourced work: API for computer use(prava-sdk, ca-server)
Models: Grounding+planning hardness for OSWorld. Privately I used codex+extensive planning to benchmark max but OSWorld scores were brittle.
Research: 
a) Edited the vision encoder such that we would show the latest "compiled" screenshot instead of having to re-encode the whole thing again, which worked but was slightly slower
b) re-implemented MSFT's GUI-Actor which essentially trains a small attention head to try predict which patch/region instead of coordinate grounding


**API:**
[CUA Control API docs](https://pravaco.github.io/prava-sdk/)

[Control API library implementation](https://github.com/pravaco/prava-sdk)

[Made the control api compatible with existing Claude cua/openai setups by reverse engineering their function calling](https://github.com/pravaco/ca-server)

**Models:**
[prava-fc](https://github.com/pravaco/prava-models/tree/master)
doesnt include latest models which use codex(for strong tool calling) + qwen3 for good grounding + codex to write mini bash scripts to enhance computer control

**Research:**
[Differential Vision Encoding for CUA](https://github.com/pravaco/diffcua/tree/main/differential_vision)

[Coordinate-Free Visual Grounding](https://github.com/pravaco/diffcua/tree/main/attention_click)
