Este arquivo está incluído no pacote binário para Windows. Instruções de compilação para Linux e Windows podem ser encontradas em RELEASE_NOTES.
cpuminer é um programa de console que é executado a partir de um prompt de comando do DOS. Não há interface gráfica (GUI) e não há suporte para mouse.

Programas de mineração frequentemente são sinalizados como malware por programas antivírus. Isso é um falso positivo, eles são sinalizados simplesmente por serem mineradores de criptomoeda. O código-fonte está aberto para qualquer pessoa inspecionar. Se você não confia no software, não use.

Escolha o arquivo exe que melhor corresponda às características da sua CPU ou use tentativa e erro para encontrar o mais rápido que não trave. Preste atenção nas características listadas na inicialização do cpuminer para garantir que você está minerando na velocidade ótima usando os melhores recursos disponíveis.

Os nomes das arquiteturas e as opções de compilação são fornecidos apenas para a série Intel Core. CPUs mais simples como Pentium e Celeron geralmente não possuem os recursos mais recentes.

CPUs AMD anteriores à Piledriver, incluindo Athlon x2 e Phenom II x4, não são compatíveis com cpuminer-opt devido a uma implementação incompatível do SSE2 nessas CPUs. Alguns algoritmos podem travar o minerador com uma instrução inválida. Recomenda-se usar um minerador não otimizado como o cpuminer-multi.

Mais informações sobre as arquiteturas de CPU Intel e AMD e seus recursos podem ser encontradas na Wikipédia.

https://pt.wikipedia.org/wiki/List_of_Intel_CPU_microarchitectures

https://pt.wikipedia.org/wiki/List_of_AMD_CPU_microarchitectures

Nome do exe            Flags de compilação       Nome da arquitetura

ogaihtmineros-sse2.exe      "-msse2"                  Core2, Nehalem  
ogaihtmineros-aes-sse42.exe "-march=westmere"         Westmere  
ogaihtmineros-avx.exe       "-march=corei7-avx"       Sandybridge  
ogaihtmineros-avx2.exe      "-march=core-avx2 -maes"  Haswell, Skylake, Coffeelake  
ogaihtmineros-avx512.exe    "-march=skylake-avx512"   Skylake-X, Cascadelake-X  
ogaihtmineros-zen           "-march=znver1"           AMD Ryzen, Threadripper

Se você gosta deste software, sinta-se à vontade para fazer uma doação:

LCC: MBZ8cJzdDWfdHtSWY1hv9rS2hwtdvK3gdu
