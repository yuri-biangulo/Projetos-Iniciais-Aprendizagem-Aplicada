'''04. e 05.
Supondo que a população de um país A seja da ordem de 80000 habitantes
 com uma taxa anual de crescimento de 3% e que a população de B seja 200000 habitantes
  com uma taxa de crescimento de 1.5%. Faça um programa que calcule e escreva
   o número de anos necessários para que a população do país A ultrapasse ou 
   iguale a população do país B, mantidas as taxas de crescimento. 

Altere o programa anterior permitindo ao usuário informar as populações 
e as taxas de crescimento iniciais. Valide a entrada e permita repetir a operação. 
'''

'''1 passo : dados de entrada '''
pop_a = int(input("Digite o tamanho da população A: "))
while pop_a < 0:
  pop_a = input("Digite novamente \n o valor informado deve ser maior que 0")
taxa_a = int(input("Digite a taxa de crescimento de A: "))

pop_b = int(input("Digite o tamanho da população B: "))
while pop_b < 0:
  pop_b = input("Digite novamente \n o valor informado deve ser maior que 0")
taxa_b = int(input("Digite a taxa de crescimento de B: "))


ano = 0
while pop_a < pop_b: 
  ano += 1 
  pop_a = int((1 + taxa_a/100 )* pop_a)
  pop_b = int((1 + taxa_b/100)*pop_b)
  print("Ano %d:" % ano)
  print("Populacao A %d:" % pop_a)
  print("Populacao B %d:" % pop_b)
print("Ultrapassa no ano", ano)
