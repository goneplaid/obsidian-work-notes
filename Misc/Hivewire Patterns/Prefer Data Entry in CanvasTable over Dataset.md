# Prefer Data Entry in CanvasTable over Dataset

---

# [[2021-03-23]]
#hivewire-patterns #data-entry #canvas-table #dataset

---

Get into the habit of never doing data entry directly in a [[Dataset]].

Datasets will most likely contain all kinds of extraneous fields, such as lookup and link fields, which will get in the way.

Instead, add a [[CanvasTable]] to a [[Workspace]] and then customize what fields you want to see by hiding unnecessary fields. In many cases, it's helpful to add related tables to your view, like a [[CanvasTable]] for a [[Lookup]] or a [[Rollup]].

