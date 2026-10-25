# SM7325 shared support

This repository owns confirmed SM7325 CPU, GIC, timer, PSCI and UFS resource
descriptions, shared kernel settings and the corresponding XNU patch series.
The Samsung SM-T733 device repository owns DRAM, firmware, peripheral wiring,
display policy, Apple identity and userdata layout.

Hardware sources and fixed revisions are recorded in soc.toml. Read README.md
before changing resource addresses. Keep DTS data and its consumer ABI together.
Never calculate file hashes for confirmation. Do not add or run tests unless
the user requests them. Preserve the original license of imported patches.
