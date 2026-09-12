# UClamp Task Profiles for Android

A configurable Android task-profile baseline originally tuned for Qualcomm Kona devices (Snapdragon 865/865+). It is not tied to a single device and can be adapted to other platforms by validating their cgroup hierarchy, kernel features, memory configuration, and profile callers.

## Compatibility

This configuration is a reference baseline, not a universal drop-in replacement. Before using it on another device, verify:

- Android version and cgroup v1/v2 layout
- controllers and subgroup paths defined by the device's `cgroups.json`
- availability of `cpu.uclamp.min`, `cpu.uclamp.max`, and `cpu.uclamp.latency_sensitive`
- memory limits and device RAM capacity
- which framework, init, or Power HAL components invoke each aggregate profile

A rooted device using Magisk or KernelSU is recommended for testing and deployment. Keep a recoverable backup of the original configuration.
