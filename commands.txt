erro de instalação:
os links para os executaveis não foram criados. Se precisar, use o seguinte comando
sudo ln -s /usr/lib/llvm-15/bin/llc /usr/bin/llc
troque llc pelo comando desejado denro da pasta llvm-15/bin

#Criando ll assembly
clang -S example.c -o exampleAssembly.ll

#criando ll IR
clang -S -emit-llvm example.c -o exampleIR.ll

#movendo de memória para registrador (tem que 'desabilitar o optnone)
clang -S -Xclang -disable-O0-optnone -S -smit-llvm  example.c -o exampleIROptNone.ll
opt -S -mem2reg exampleIROptNone.ll -o exampleIRMem2Reg.ll

Compilação:
llc --version
#gera código de máquina (assembly, ou similar)  do programa para outras arquiteturas
llc exampleIR.ll -march=arm -o sum.arm
llc exampleIR.ll -march=x86-64

#criar bitcode (representação binária)
llvm-as-15 exampleIR.ll -o exampleIR.bc

#traduzir bytecode para assembly
llc exampleIR.bc -o exampleIR.x86 

#criar .dot (CFG) (tem que ser da versão com optnone desabilitado)
opt -dot-cfg exampleIROptNone.ll

#criar .dot (CFG) somente os vertices, sem as instruções
opt -dot-cfg-only exampleIROptNone.ll

#criar .dot (CFG) somente das regiões
opt -dot-regions-only exampleIROptNoneRegions.ll

#criar .dot (CFG) dominator tree (verificar o que é exatamente)
opt -dot-dom teste.ll

#criar .dot (CFG) dominator tree (verificar o que é exatamente), somente os vertices, sem as instruções
opt -dot-dom-only teste.ll

#criar .dot (CFG) callgraph
opt -dot-callgraph teste.ll

#dot2pdf (CFG)
dot -Tpdf .main.dot -o identity.pdf


Analyses

#loop Pass
function Pass
module Pass
callgraph scc Pass
region Pass
machine function Pass
