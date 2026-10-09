> [!WARNING]
> **This repository is deprecated and no longer maintained.**
>
> Polygon zkEVM has been retired. Polygon CDK chains now run on
> [cdk-op-reth](https://github.com/0xPolygon/cdk-op-reth) and settle to the
> [Agglayer](https://github.com/agglayer/agglayer) with pessimistic proofs and
> full execution proofs. This code is kept for reference only. It will not
> receive bug fixes, security patches, or releases.
>
> **Use instead:**
> - Proving: [agglayer/provers](https://github.com/agglayer/provers)
> - Agglayer node: [agglayer/agglayer](https://github.com/agglayer/agglayer)
> - Docs: [docs.polygon.technology](https://docs.polygon.technology)
>
> **Have funds locked in contracts on zkEVM mainnet?** See
> [zkevm-proof-of-ownership-kit](https://github.com/agglayer/zkevm-proof-of-ownership-kit).
>
> Security issues in live Polygon systems: see [SECURITY.md](https://github.com/0xPolygon/.github/blob/main/SECURITY.md).

# zkevm-rom
This repository contains the zkasm source code of the polygon-hermez zkevm

## Usage
````
npm i
npm run build
````
The resulting `json` file will be created in the `./build` directory

### Advanced options
- `-i ${input zkasm file}`: specify input source `zkasm` path
  - default value: `main/main.zkasm`
- `-o ${destination rom file}`: specify output path for the resulting `json`
  - default value: `build/rom.json`
- `-s ${steps}`: specify steps as $2^{steps}$
  - default value: current steps in `constants.zkasm`

Example:
```
npm run build -- -i ${path} -o ${path} -s ${steps}
```

