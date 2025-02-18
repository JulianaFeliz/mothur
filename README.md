# mothur

#baixando mothur do código fonte
wget https://github.com/mothur/mothur/archive/refs/tags/v1.48.2.tar.gz
tar -xvzf v1.48.2.tar.gz
cd mothur-1.48.2

#script de programa criado do codigo-fonte
#!/bin/bash
#SBATCH --time=0-0:5 #especifica o tempo máximo de execução do job, dado no padrão dias-horas:minutos
#SBATCH --partition=amd-512  # partição para a qual o job é enviado

./mothur-1.48.2 #o ponto e a barra indicam o caminho até a pasta atual.

#criar o executavel do programa
gcc mothur.c -o mothur

#ecxecutar o programa
sbatch jobmothur
