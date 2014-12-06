forcelyma.github.io
===================
  <!DOCTYPE >
<html> 
<head>
<title> Quiz de:
</title>
</head> 
<body>
<h1> Quiz de entretenimento</h1>
<img src= "http://gamefone.com.br/wp-content/uploads/2014/05/capa-P4.png" />


<a href="https://github.com/forcelyma"> Caso queira visitar minha página </a>

<p> Uma forma de passar o tempo </p>
<p> Uma forma de entretenimento </p>
<p> Uma forma de enriquecer nossos conhecimentos </p>
</body>

</html>
import random


perguntas = [
    "Quem foi o rei do pop?",
    "Qual o nome do filho de Bebel na seria da globo a grande família?",
    "No filme Guerra Mundial Z como a família escapa dos zumbis?",
    "Onde se passa a história de Velozes e Furiosos 5?",
    "Quando Elvis Presley nasceu?",
    "Qual é o nome completo do cantor Lucas Lucco?",
    "Qual o nome do primeiro filme da série 007?",
    "Quem é o autor(a) do livro Jogos vorazes?",
]

respostas = [
#("a primeira resposta de cada pergunta é a certa")
    ["Michael Jackson","Juntin Bieber","Thiaguinho"],
    ["Floriano","Rodrigo","JR"],
    ["Roubam um carro que estava nas ruas","pelo esgoto","entraram no predio mais proximo"],
    ["No Brasil","No México","USA"],
    ["8 de Janeiro de 1935","22 de julho de 1969","11 de setembro de 1922"],
    ["Lucas Correa de Oliveira","Lucas Sanches Lucco","Lucas Vieira de Oliveira"],
    ["007 contra o Satânico Dr. No","007 Cassino Royale","007 Permissão para Matar"],
    ["Suzanne Collins","Joanne Murray","Annie Bryant"],
]


#------------
def main():
    for índice,pergunta in enumerate(perguntas):
        print(str(índice+1) + ": " + pergunta)

        # shuffle embaralha só pra mostrar na tela
        respostas_embaralhas = list(respostas [índice])
        random.shuffle(respostas_embaralhas)

        x = []
        for opção,r in zip(["a","b","c"],respostas_embaralhas):
            x.append(opção + ") " + r)
            print(opção + ") " + r)

        # entrada do usuário
        resposta = input("Qual a resposta? ") # resposta vai ser uma letra

        for r in x:
            if r.startswith(resposta) == True:
                if r.find(respostas[índice][0]) != -1:
                    print("+------------+")
                    print("|  Parabéns  |")
                    print("|Você acertou|")
                    print("+------------+")
                    break
        else:
            print("+---------------+")
            print("|  Você errou   |")
            print("+---------------+")

main()
</html>
