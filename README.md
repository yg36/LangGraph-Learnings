# LangGraph Learnings

Hands-on notebook series for learning LangGraph fundamentals.

This repository is a learning log for understanding how agentic AI workflows are built with graph-based state, nodes, edges, sequential execution, and conditional routing. The notebooks move from a single-node graph to multi-step and branching workflows.

## What I Practiced

- Defining graph state with `TypedDict`
- Building `StateGraph` workflows
- Adding nodes with `graph.add_node(...)`
- Connecting nodes with `graph.add_edge(...)`
- Compiling graphs with `graph.compile()`
- Invoking compiled graphs with structured input state
- Passing and updating state between nodes
- Creating sequential graph flows
- Using `START`, `END`, and `add_conditional_edges` for branching logic
- Visualizing a graph with Mermaid output

## Notebook Map

| Notebook | Focus | What it demonstrates |
| --- | --- | --- |
| `LangGraph_1.ipynb` | First state graph | A single greeter node updates message state and returns `heyYG`. |
| `LangGraph_2.ipynb` | Multi-input state | A graph receives a name and list of values, then computes a summed response. |
| `LangGraph_3.ipynb` | Operation logic | A node switches between addition, multiplication, and invalid-operation handling. |
| `Langraph_4.ipynb` | Sequential graph | Two connected nodes update the answer state in order. |
| `Langgraph_5.ipynb` | Multi-node pipeline | A greet -> age -> skills flow builds a final profile-style message. |
| `Langgraph_6.ipynb` | Conditional routing | Uses `START`, `END`, and `add_conditional_edges` to route between addition and subtraction nodes. |

## Why This Matters

LangGraph is useful because real AI agents are rarely just one model call. They need:

- state
- control flow
- decision points
- retry or branching paths
- clear boundaries between steps

These notebooks helped me understand the foundation behind agent workflows before moving into larger LLM/RAG agents.

## Tech Stack

- Python
- Jupyter Notebook
- LangGraph
- TypedDict
- IPython display / Mermaid visualization

## Run Locally

```bash
git clone https://github.com/yg36/LangGraph-Learnings.git
cd LangGraph-Learnings
python -m venv .venv
.venv\Scripts\activate
pip install langgraph notebook ipython
jupyter notebook
```

Then open the notebooks in order:

1. `LangGraph_1.ipynb`
2. `LangGraph_2.ipynb`
3. `LangGraph_3.ipynb`
4. `Langraph_4.ipynb`
5. `Langgraph_5.ipynb`
6. `Langgraph_6.ipynb`

## Current Status

This is a fundamentals repository. It is intentionally simple and focused on learning the LangGraph execution model.

## Next Steps

- Add tool-calling nodes
- Add LLM-backed nodes
- Add memory/checkpointing
- Build a small agent workflow using conditional graph routing
- Connect LangGraph concepts with RAG and recruiter-style AI workflows
