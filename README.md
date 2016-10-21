#-*-coding:UTF-8-*-
from Tkinter import*
class janela:
	def __init__(self,root):

		self.root = root
		
		fontes2 = ('Times','14')
		fontes =  ('Verdana', '14' )
		raiz['bg'] = '#de703d'
		raiz.geometry("800x600+300+300")
		raiz.title("Gerenciador") 

		self.b1 = Button(self.root,text='Cadastrar produto',width=18)
		self.b1.bind("<Button-1>",self.cadastrar)
		self.b1.place(x=300, y=300)

		
		self.b2 = Button(self.root,text='Deletar produto',width=18)
		self.b2.bind("<Button-1>",self.deletar)
		self.b2.place(x=300, y=330)

		self.b3 = Button(self.root,text='Estoque',width=18)
		self.b3.bind("<Button-1>",self.estoque)
		self.b3.place(x=300, y=360)

		self.b4 = Button(self.root,text='Vendas',width=18)
		self.b4.bind("<Button-1>",self.vendas)
		self.b4.place(x=300, y=390)
		
		
	def cadastrar(self,event):
		class screen:
			def __init__(self,root):
				self.root = root
				fontes2 = ('Times','14')
				fontes =  ('Verdana', '14' )
				tela.title('Cadastrar produto')
				self.msg1 = Label(self.root,text='Cadastramento',font='bold')
				self.msg1.grid()
						
				self.msg2 = Label(self.root , text='Insira o codigo de barras:', font=fontes2)
				self.msg2.grid(row=1,columnspan=1,sticky=N)
				#Codigo de barras
				self.Cod = Entry(self.root,width=15,font=fontes)
				self.Cod.focus_force()
				self.Cod.grid(column=1,row=1,sticky=W)

				self.msg3 = Label(self.root,text='Insira o Nome do produto:',font=fontes2)
				self.msg3.grid(row=2,columnspan=1,sticky=N)
				#Codigo de barras
				self.nome = Entry(self.root,width=15,font=fontes)
				self.nome.focus_force()
				self.nome.grid(column=1,row=2,sticky=W)

				self.msg4 = Label(self.root,text='Insira a quantidade de produtos:',font=fontes2)
				self.msg4.grid(row=3,columnspan=1,sticky=N)
				#Codigo de barras
				self.quantidade = Entry(self.root,width=15,font=fontes)
				self.quantidade.focus_force()
				self.quantidade.grid(column=1,row=3,sticky=W)

				self.msg5 = Label(self.root,text='Insira o valor do produto:',font=fontes2)
				self.msg5.grid(row=4,columnspan=1,sticky=N)
				#Codigo de barras
				self.nome = Entry(self.root,width=15,font=fontes)
				self.nome.focus_force()
				self.nome.grid(column=1,row=4,sticky=W)

				self.b5 = Button(self.root,text='Confirmar',bg='deepskyblue',pady=10)
				self.b5.grid(row=5,column=2,sticky=W)



		tela = Tk()
		screen(tela)
		tela.mainloop()	
	'''def deletar(self,event):
		#class delete:
		#	def __init__(self,root):
				self.root = root
				fontes2 = ('Times','14')
				fontes =  ('Verdana', '14' )
				delt.title('Deletar produto')
				self.msg7 = Label(self.root,text='Deletar',font='bold')
				self.msg7.grid()

				self.msg8 = Label(self.root,text='Insira o codigo de produto:',font=fontes2)
				self.msg8.grid(row=1,columnspan=1,sticky=N)
				#Codigo de barras
				self.codigo = Entry(self.root,width=15,font=fontes)
				self.codigo.focus_force()
				self.codigo.grid(column=1,row=1,sticky=W)

				self.b6 = Button(self.root,text='Confirmar',bg='deepskyblue',pady=10)
				self.b6.grid(row=2,column=2,sticky=W)
		delt = Tk()
		delete(delt)
		delt.mainloop()

			'''

	def estoque(self,event):
		class estok:
			def __init__(self,root):
				self.root = root
				fontes2 = ('Times','14')
				fontes =  ('Verdana', '14' )
				est.title('Estoque')
				
				self.b7 = Button(self.root,text='Ver estoque',width=18)
				self.b7.bind("<Button-1>",self.ver)
				self.b7.grid(row=1,column=1,sticky=W)


				self.b8 = Button(self.root,text='Ver histórico de sáida',width=18)
				self.b8.grid(row=2,column=1,sticky=W)
			def ver(self,event):
				class look:
					def __init__(self,root):	

						self.root = root
						fontes2 = ('Times','14')
						fontes =  ('Verdana', '14' )
						lok.title('Produtos')





				lok = Tk()
				look(lok)
				lok.mainloop()



		est = Tk()
		estok(est)
		est.mainloop()



	def vendas(self,event):
		class vend:
			def __init__(self,root):	
				self.root = root
				fontes2 = ('Times','14')
				fontes =  ('Verdana', '14' )
				vd.title('Vendas')

				self.b8 = Button(self.root,text='Ver medía diária',width=18)
				self.b8.bind("<Button-1>",self.ver)
				self.b8.grid(row=1,column=1,sticky=N)

				self.b9 = Button(self.root,text='Ver valor bruto do mês',width=18)
				self.b9.bind("<Button-1>",self.bruto)
				self.b9.grid(row=2,column=1,sticky=N)

				self.b10 = Button(self.root,text='Ver valor arrecadado',width=18)
				self.b10.bind("<Button-1>",self.arrecadado)
				self.b10.grid(row=3,column=1,sticky=N)

			def ver(self,event):
				class olhar:
					def __init__(self,root):
						self.root = root
						fontes2 = ('Times','14')
						fontes =  ('Verdana', '14')
						instancia.title('Medía')
				instancia = Tk()
				olhar(instancia)
				instancia.mainloop()	
			def bruto(self,event):
				class brut:
					def __init__(self,root):
						self.root = root
						fontes2 = ('Times','14')
						fontes =  ('Verdana', '14')
						inst.title('Medía')
				inst = Tk()
				brut(inst)
				inst.mainloop()


			def arrecadado(self,event):
				class arrecade:
					def __init__(self,root):
						self.root = root
						fontes2 = ('Times','14')
						fontes =  ('Verdana', '14')
						inst.title('Dias')
				inst = Tk()
				arrecade(inst)
				inst.mainloop()
						
						


		vd = Tk()
		vend(vd)
		vd.mainloop()








raiz = Tk()
janela(raiz)
raiz.mainloop()
