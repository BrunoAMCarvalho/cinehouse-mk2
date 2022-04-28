# cinehouse-mk2
Projeto Cinehouse DH

let catalogo = [
    {
        codigo: 1,
        titulo: 'Titanic',
        duracao: 3.5,
        atores: ['Leonardo Dicaprio','Kate Winslet'],
        anoDeLancamento: 1997,
        emCartaz:false
    },
     {
        codigo: 2,
        titulo: 'Encanto',
        duracao: 2,
        atores: ['Mirabel Madrigal','bruno Madrigal'],
        anoDeLancamento: 2021,
        emCartaz:true

    }
]

let adicionarfilme = filme => catalogo.push(filme)
adicionarfilme(
    {
        codigo: 3,
        titulo: 'Eternos',
        duracao: 3,
        atores: ['Starfox','Thena'],
        anoDeLancamento: 2021,
        emCartaz:true
    }
)
console.log(catalogo)

console.log(catalogo[0].codigo)

let buscarFilme = codigo => {
    for (let i = 0; i < catalogo.length; i++){
        if(catalogo[i].codigo === codigo){
            return catalogo[i]
        }

    }
}

console.log(buscarFilme(2))

let alterarStatusEmCartaz = codigo => {
    for(let i = 0; i < buscarFilme.length; i++) {
        if(catalogo[i].emCartaz){
            catalogo[i].emCartaz = false
        }else{
            catalogo[i].emCartaz = true
        }
    }
}

console.log(alterarStatusEmCartaz(1))
console.log(catalogo[0])