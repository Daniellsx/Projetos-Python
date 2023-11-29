from tkinter import *
import tkinter
from datetime import datetime
import pytz

fuso_horario = pytz.timezone('America/Sao_Paulo')

meses = ["Janeiro", "Fevereiro", "Março", "Abril", "Maio", "Junho", "Julho", "Agosto", "Setembro", "Outubro", "Novembro", "Dezembro"]
dias_da_semana = ["Segunda-feira", "Terça-feira", "Quarta-feira", "Quinta-feira", "Sexta-feira", "Sábado", "Domingo"]

#Cores
cor1 = "#3d3d3d" #preta
cor2 = "#fafcff" #branca
cor3 = "#21c25c" #verde
cor4 = "#eb463b" #vermelha
cor5 = "#dedcdc" #cinza
cor6 = "#3080f0" #azul
cor7 = "#ffcbdb" #rosa

fundo = cor1
cor = cor7

janela = Tk()
janela.title("Relógio")
janela.geometry("440x180")
janela.resizable(width=FALSE, height=FALSE)
janela.configure(bg = cor1)

def relogio():
    tempo = datetime.now(fuso_horario)
    
    hora = tempo.strftime("%H:%M:%S")
    dia_da_semana = dias_da_semana[tempo.weekday()]  # Obtém o dia da semana como um índice
    dia = tempo.strftime("%d")
    mes = meses[int(tempo.strftime("%m")) - 1]  # Obtém o mês como um índice
    ano = tempo.strftime("%Y")
    
    l1.config(text=hora)
    l1.after(200, relogio)
    l2.config(text=dia_da_semana + " " + dia + "/" + mes + "/" + ano)

l1 = Label(janela, text="", font=("Arial 60"), bg=fundo, fg=cor)
l1.grid(row=0, column=0, sticky=NW, padx=5)

l2 = Label(janela, text="", font=("Arial 18"), bg=fundo, fg=cor)
l2.grid(row=1, column=0, sticky=NW, padx=5)

relogio()
janela.mainloop()
