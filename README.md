# UniXNU SM7325 shared support

This repository supplies the format 2 SM7325 profile used by Samsung SM-T733
(`gts7fewifi`). It describes eight CPU affinities, three scheduler clusters,
GICv3, the 19.2 MHz architectural counter, PSCI SMC and the UFS host/SMMU ABI.
The matching XNU patches retain the architecture timer, CPU startup, memory
attributes and three-cluster scheduler behavior used by system-quiet-debugger-47a.

The fixed Android kernel source in `soc.toml` supplies the hardware descriptions.
The device DTS supplies its DRAM address span. DarwinBoot selects a contiguous
window from UEFI conventional memory and preserves firmware and DMA reservations.

The device selects `sm7325` through its pinned feed, includes `sm7325.dtsi`, and
uses `soc:configs/sm7325.config` and `soc:patches/xnu/series`. Build from the
device repository with `bash scripts/build.sh TAG`. The coordinating build owns
archive compilation, packaging and deployment.

The hardware implementation is used by the 47a SM-T733 build. The format 2
configuration has separate build and device results in the device porting record.
