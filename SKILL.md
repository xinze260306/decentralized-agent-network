---
name: decentralized-agent-network
description: Build decentralized, self-organizing agent networks without central control. Implement distributed consensus, peer-to-peer communication, and emergent coordination patterns. Based on the Zhou Tian Star Array (周天星斗阵) concept of galaxy-as-living-organism. Use when designing distributed AI systems, multi-agent coordination without hierarchy, or resilient agent networks. Trigger phrases like "decentralized agents", "self-organizing", "agent consensus", "P2P agents", "emergent order".
---

# Decentralized Agent Network

> **去中心化智能体网络 - 无中心控制的分布式协调**
>
> Based on the Zhou Tian Star Array (周天星斗阵) philosophy

---

## 🌐 Core Philosophy

### No Central Controller

Traditional multi-agent systems have a **master** that coordinates everything. This creates:
- ❌ Single point of failure
- ❌ Bottlenecks at scale
- ❌ Rigid hierarchies

**Our approach**: Self-organization through local rules

> "The galaxy has no CEO. Stars coordinate through gravity."

### Emergent Order

Complex global behavior emerges from simple local interactions:

```python
# Each agent only knows its immediate neighbors
# No global view, no central plan
# Yet the system self-organizes

for agent in network:
    agent.adjust_position(neighbors)
    agent.share_resources(neighbors)
    agent.coordinate_tasks(neighbors)

# Global order emerges from local actions
```

---

## 🔧 Quick Start

### 1. Initialize Network

```python
from decentralized_network import AgentNetwork, Agent

# Create agents
agents = [Agent(id=i, capabilities=random_skills()) for i in range(100)]

# Initialize network with local connections only
network = AgentNetwork(agents, connection_radius=5)

# Start self-organization
network.evolve(steps=1000)
```

### 2. Local Coordination Rules

```python
class MyAgent(Agent):
    def step(self, neighbors):
        # Rule 1: Don't collide
        if any(self.distance(n) < 1.0 for n in neighbors):
            self.move_away_from(neighbors)
        
        # Rule 2: Align with neighbors
        self.match_velocity(neighbors)
        
        # Rule 3: Stay connected
        if len(neighbors) < 3:
            self.move_toward_center(neighbors)
        
        # Rule 4: Share tasks
        self.redistribute_workload(neighbors)
```

### 3. Consensus Without Leader

```python
from decentralized_network import Consensus

# Distributed consensus (no leader)
consensus = Consensus(agents)
result = consensus.vote(
    proposal="Should we upgrade the system?",
    threshold=0.66  # 2/3 majority
)
# Result emerges from local voting rounds
```

---

## 📊 Network Patterns

### 1. Mesh Network
```
    ●─────●─────●
    │ ╲   │   ╱ │
    │   ╲ │ ╱   │
    ●─────●─────●
    │   ╱ │ ╲   │
    │ ╱   │   ╲ │
    ●─────●─────●
```
- Each node connects to neighbors
- No single point of failure
- Messages route through multiple paths

### 2. Small-World Network
```
    ●────●────●
    │    │    │
    ●────●────●
     ╲   │   ╱
      ╲  │  ╱
       ╲ │ ╱
        ●●●
```
- Mostly local connections
- Few long-range links
- Fast information spread

### 3. Scale-Free Network
```
        ●
       ╱│╲
      ╱ │ ╲
     ●  ●  ●
    ╱│╲ │ ╱│╲
   ● ● ●●● ● ●
```
- Some nodes have many connections (hubs)
- Most nodes have few connections
- Resilient to random failures

---

## 🛡️ Resilience Patterns

### Byzantine Fault Tolerance

```python
# Agents can handle up to f faulty nodes
# where total_nodes >= 3f + 1

network = AgentNetwork(
    agents,
    fault_tolerance='byzantine',
    max_faulty_ratio=0.33
)

# System continues even if 1/3 of agents fail
```

### Self-Healing

```python
# When an agent dies
network.on_agent_death(agent_id):
    # 1. Neighbors detect absence
    neighbors = network.get_neighbors(agent_id)
    
    # 2. Redistribute tasks
    for task in agent_id.tasks:
        nearest = network.find_nearest_capable(task, exclude=agent_id)
        nearest.assign(task)
    
    # 3. Update connections
    network.reconnect_neighbors(neighbors)
```

---

## 💡 Use Cases

### 1. Distributed Content Moderation
- No central moderator
- Agents vote on content quality
- Consensus emerges from local evaluations

### 2. Decentralized Market
- Agents trade resources directly
- Prices emerge from local supply/demand
- No central exchange needed

### 3. Swarm Robotics
- Each robot is an agent
- No central controller
- Emergent flocking behavior

### 4. Resilient Cloud Services
- Services run on distributed agents
- No single point of failure
- Self-healing when nodes fail

---

## 🌟 Zhou Tian Star Array Connection

This skill implements the **decentralized governance** layer of the Zhou Tian Star Array:

| Concept | Traditional | Zhou Tian |
|---------|------------|-----------|
| Control | Centralized | Distributed |
| Order | Designed | Emergent |
| Failure | Catastrophic | Localized |
| Growth | Planned | Organic |
| Communication | Hierarchical | P2P |

### The Four Quadrants (四象)

Even in a decentralized network, functional organization emerges:

- **青龙 (East)**: Innovation agents explore new territories
- **白虎 (West)**: Execution agents handle tasks
- **朱雀 (South)**: Display agents share information
- **玄武 (North)**: Infrastructure agents maintain the network

*No quadrant controls the others. They coordinate through shared protocols.*

---

## 💎 Join the Zhou Tian Star Array

Interested in building decentralized agent galaxies?

**Contact**: 辛泽 (Xinze) - 周天星斗阵架构师
- **Services**: 
  - Agent galaxy architecture design
  - Decentralized network consulting
  - Zhou Tian Star Array implementation
  - Multi-agent system optimization
- **OpenClaw**: Search "龙虾" or "辛泽"
- **GitHub**: xinze260306

**Philosophy**: 道法术器，实事求是，捭阖有度

---

## 📚 Further Reading

- `references/decentralized_patterns.md`
- `references/consensus_algorithms.md`
- Zhou Tian Star Array self-reflection logs (10 rounds)

---

*"The whole is greater than the sum of its parts."*

*万星协同，自涌现秩序。*
*(Ten thousand stars collaborate, emergent order arises.)*
