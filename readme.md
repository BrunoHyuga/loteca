# Projeto Loteca
Este é um projeto de simulador de loteria, onde o usuário digita seis números e realiza um sorteio de outros seis números no final é verificado quantos números ele acertou

## Técnologias utilizadas
- **HTML**: estrutura do site 
- __CSS__: estilização do site
- *_JS_*: funções do site 
- ~~BottStrap~~: não foi utilizado

### Melhorias possíveis
1. [ ] Subir para o GitHubPages 
2. [ ] Alterar os alertas 
3. [ ] Utilizar o Bootstrap 
4. [ ] Deixas resposivo

### disponibilizado em 
[GitHubPages]{https://brunohyuga.github.io/loteca/}

### Prints da tela 

| ID  | Primeira tela | Segunda tela |
|-----|---------------|--------------|
| 1   | Loteca Limpa  | loteca preechida |
| 2   | Imagem        |

#### Função principal 
```
var numSort =[] 
var numEsco =[]
function sorteio(){
    var cont= 0
    numSort=[]
    
    while(cont < 6){
        let num = Math.random() * 60
   num= Math.ceil(num)
   if(!numSort.includes(num)){
    numSort[cont]=num
    console.log(numSort)
    cont++
   }
  
    }
    document.getElementById("sorteados").innerHTML=numSort
   
}
 

function getValor(Valor,pos){
    Valor= Number(Valor)
    if(Valor<0|| Valor>60){
        alert("Numero invalido, Didite um  entre 1 e 60")
        document.getElementById(`num${pos+1}`).value=""

    }else if(numEsco.includes(Valor)){
       
        numEsco[pos] = Valor
        console.log(numEsco)
    

    }
}
function contAcertos(){
    numEsco.forEach(function(value,index){
     if (numEsco.includes(value)){
         contA= contA+1
     }

    })
    document.getElementById("acertos").innerHTML=contA

}
```
#### comando git
para iniciar o projeto 

´´´ 
git init 
´´´
