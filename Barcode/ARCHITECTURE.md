Processors used in Axis products are based on various architectures:
- MIPS (ARTPEC-4 and ARTPEC-5)
- ARM7HF (ARTPEC-6, ARTPEC-7, Ambarella S2L and S3L)
- AARCH64 (Ambarella S5 and S5L)

To determine the architecture used, go to Settings - System - Plain config and select the Properties section.
Under System, the architecture and chipset is listed.

Alternatively, use the following command to list the properties:

http://ip_address/axis-cgi/admin/param.cgi?action=list&group=root.properties.system

