# go2_mjlab

```sh
uv run go2_list_envs
```

```sh
just tensorboard
```

```sh
just run go2_train Mjlab-Velocity-Rough-Unitree-Go2 \
    --env.scene.num-envs 4096 \
    --agent.max-iterations 10000 \
    --video True \
    --video-length 100 \
    --agent.logger tensorboard

just run go2_train Mjlab-Velocity-Flat-Unitree-G1 \
    --env.scene.num-envs 4096 \
    --agent.max-iterations 10000 \
    --video True \
    --video-length 100 \
    --agent.logger tensorboard
```

```sh
just run go2_record Mjlab-Velocity-Rough-Unitree-Go2 \
    --checkpoint-file logs/rsl_rl/go2_velocity/2025-12-12_01-03-24/model_1950.pt \
    --num-envs 12 \
    --num-steps 1000
```

```sh
just run go2_play Mjlab-Velocity-Rough-Unitree-Go2 \
    --checkpoint-file [path-to-checkpoint] \
    --video True \
    --video-length 200

just run go2_play Mjlab-Velocity-Rough-Unitree-Go2 \
    --checkpoint-file [path-to-checkpoint] \
    --video True \
    --video-length 200

```
