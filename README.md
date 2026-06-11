# GossipPPO: Decentralized Multi-Task Federated RL

Notebook artifact for a decentralized reinforcement-learning system design.

## Highlights

- Peer-to-peer gossip instead of a central parameter server.
- PPO/Ray-compatible boundary for local policy updates.
- Byzantine-robust coordinate median and MAD filtering.
- ADMM-style dual correction for consensus updates.
- Simulated stragglers, malicious clients, and 30% offline-agent stress tests.

## Artifact

- `gossippop_decentralized_federated_rl.ipynb`

## AWS / SageMaker Deployment Path

- Use Ray workers as distributed policy learners.
- Store rollout summaries and checkpoints in S3.
- Run multi-worker training through SageMaker training jobs.
- Track consensus error, accepted peer updates, Byzantine rejection rate, and
  convergence under offline-agent stress tests through CloudWatch logs.
