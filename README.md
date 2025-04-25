**OGAIHT_MINER** é um fork do *cpuminer-multi* de TPruvot com otimizações importadas de outros mineradores 

Todo o código é considerado aberto e gratuito. Se alguém tiver um direito sobre qualquer parte do código, poste seu caso para *OGAIHT_MINER* por e-mail.

Programas de mineração frequentemente são sinalizados como malware por programas antivírus. Isso é um falso positivo, eles são sinalizados simplesmente por serem mineradores de criptomoeda. O código-fonte está aberto para qualquer pessoa inspecionar. Se você não confia no software, não o use.


Relatar bugs  
Bugs podem ser relatados por e-mail para minerfacture@gmail.com ou abrindo uma issue no GitHub:  
[https://github.com/mbr-2018/ogaiht_miner/issues](https://github.com/mbr-2018/ogaiht_miner/)


Veja o arquivo *RELEASE_NOTES* para o changelog e *INSTALL_LINUX* ou *INSTALL_WINDOWS* para instruções de compilação.

### Requisitos


1. Uma CPU de arquitetura x86_64 com suporte mínimo a SSE2. Isso inclui Intel Core2 e versões mais recentes, além dos equivalentes AMD. Para aproveitar as otimizações AES_NI, é necessário uma CPU com AES_NI. Isso inclui Intel Westmere e versões mais recentes, além dos equivalentes AMD. Outras otimizações estão disponíveis em alguns algoritmos para CPUs com AVX e AVX2, respectivamente para Sandybridge e Haswell.

CPUs mais antigas são suportadas pelo *cpuminer-multi* de TPruvot, mas com desempenho reduzido.

CPUs ARM não são suportadas.

2. Sistema operacional Linux de 64 bits. Distribuições baseadas no Ubuntu e Fedora, incluindo Mint e CentOS, são conhecidas por funcionarem e terem todas as dependências em seus repositórios. Outras distribuições podem funcionar, mas podem exigir mais esforço. Versões antigas, como CentOS 6, não funcionam devido à falta de recursos. 
O Windows de 64 bits é suportado com mingw_w64 e msys ou binários pré-compilados.

MacOS, OSx e Android não são suportados.

3. Pool Stratum. Alguns algoritmos podem funcionar com mineração de carteira usando getwork ou GBT. Os resultados podem variar.

### Algoritmos Suportados


- allium: Garlicoin
- anime: Animecoin
- argon2: Argon2 coin (AR2)
- argon2d250: argon2d-crds, Credits (CRDS)
- argon2d500: argon2d-dyn, Dynamic (DYN)
- argon2d4096: argon2d-uis, Unitus (UIS)
- axiom: Shabal-256 MemoHash
- blake: Blake-256 (SFR)
- blake2b: Blake2b 256
- blake2s: Blake-2 S
- blakecoin: blake256r8
- bmw: BMW 256
- bmw512: BMW 512
- c11: Chaincoin
- decred
- deep: Deepcoin (DCN)
- dmd-gr: Diamond-Groestl
- groestl: Groestl coin
- hex: x16r-hex
- hmq1725: Espers
- hodl: Hodlcoin
- jha: Jackpotcoin
- keccak: Maxcoin
- keccakc: Creative coin
- lbry: LBC, LBRY Credits
- luffa: Luffa
- lyra2h: Hppcoin
- lyra2re: lyra2
- lyra2rev2: lyra2v2
- lyra2rev3: lyrav2v3, Vertcoin
- lyra2z
- lyra2z330: Lyra2 330 rows, Zoin (ZOI)
- m7m: Magi (XMG)
- myr-gr: Myriad-Groestl
- neoscrypt: NeoScrypt(128, 2, 1)
- nist5: Nist5
- pentablake: Pentablake
- phi1612: phi
- phi2: Luxcoin (LUX)
- phi2-lux: idêntico a phi2
- pluck: Pluck:128 (Supcoin)
- polytimos: Ninja
- power2b: MicroBitcoin (MBC)
- quark: Quark
- qubit: Qubit
- scrypt: scrypt(1024, 1, 1) (padrão)
- scrypt:N: scrypt(N, 1, 1)
- sha256d: Double SHA-256
- sha256q: Quad SHA-256, Pyrite (PYE)
- sha256t: Triple SHA-256, Onecoin (OC)
- sha3d: Double keccak256 (BSHA3)
- shavite3: Shavite3
- skein: Skein+Sha (Skeincoin)
- skein2: Double Skein (Woodcoin)
- skunk: Signatum (SIGT)
- sonoa: Sono
- timetravel: Machinecoin (MAC)
- timetravel10: Bitcore
- tribus: Denarius (DNR)
- vanilla: blake256r8vnl (VCash)
- veltor: (VLT)
- whirlpool
- whirlpoolx
- x11: Dash
- x11evo: Revolvercoin
- x11gost: sib (SibCoin)
- x12: Galaxie Cash (GCH)
- x13: X13
- x13bcd: bcd
- x13sm3: hsr (Hshare)
- x14: X14
- x15: X15
- x16r
- x16rv2: Ravencoin (RVN)
- x16rt: Gincoin (GIN)
- x16rt-veil: Veil (VEIL)
- x16s: Pigeoncoin (PGN)
- x17
- x21s
- x22i
- x25x
- xevan: Bitsend (BSD)
- yescrypt: Globalboost-Y (BSTY)
- yescryptr8: BitZeny (ZNY)
- yescryptr8g: Koto (KOTO)
- yescryptr16: Eli
- yescryptr32: WAVI
- yespower: Cryply
- yespowerr16: Yenten (YTN)
- yespower-b2b: generic yespower + blake2b
- zr5: Ziftr

### Errata


Algoritmos antigos que não são mais utilizados com frequência não terão as otimizações mais recentes.
Cryptonight e variantes não são mais suportados, use outro minerador.
Neoscrypt trava no Windows, use a versão legada.

CPUs AMD anteriores à Piledriver, incluindo Athlon x2 e Phenom II x4, não são suportadas pelo *OGAIHT_MINER* devido a uma implementação incompatível do SSE2 nessas CPUs. Alguns algoritmos podem travar o minerador com uma instrução inválida. Recomenda-se usar um minerador não otimizado como o *cpuminer-multi*.

*OGAIHT_MINER* não funciona minerando o algoritmo Decred no Nicehash e só produz rejeições "invalid extranonce2 size".
Testes de benchmark não funcionam para x11evo.

### Bugs

Os usuários são incentivados a postar seus relatórios de bugs usando as issues no GitHub:

[https://github.com/mbr-2018/ogaiht_miner/issues](https://github.com/mbr-2018/ogaiht_miner/issues)



Todos os relatórios de problemas devem ser acompanhados de uma definição adequada do problema. Isso deve incluir como o problema ocorreu, a linha de comando e a saída do minerador mostrando as mensagens de inicialização e quaisquer erros. Um histórico também é útil, ou seja, funcionava antes?

### Doações

*OGAIHT_MINER* não tem taxas de nenhum tipo, mas doações são aceitas.

LCC: MBZ8cJzdDWfdHtSWY1hv9rS2hwtdvK3gdu

Feliz mineração!

