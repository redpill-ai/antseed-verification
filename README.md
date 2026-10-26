# RedPill AntSeed seller

RedPill offers GPT models through its AntSeed seller and the RedPill API.

**Partial TEE:** AntSeed seller node can present TDX attestation; upstream inference is not TEE.

- Seller peer ID: `7e9905496f803214bbe714c154397643890ddc4f`
- Seller wallet: `0x7e9905496f803214bbe714c154397643890dDC4f`
- Domain: [redpill.ai](https://redpill.ai)
- Ownership proof: [antseed.json](antseed.json)
- Service catalog: [redpill-catalog.json](redpill-catalog.json)

The catalog lists USD prices per one million tokens, including cached input.
The seller checks the public catalog every five minutes. Valid updates are
cached; failed downloads or invalid updates keep the last valid catalog.
Adding model IDs recycles the seller child after draining active channels.
Price increases have an additional announcement delay of at least ten minutes;
price cuts take effect immediately after refresh.

The peer's TEE badge applies to the seller node. It does not claim confidential
upstream inference. This catalog therefore does not use the `confidential`
category.
