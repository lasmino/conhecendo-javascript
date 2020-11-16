# conhecendo-javascript
#iniciando_js# Um testador de idade atraves de interatividade do js & DOM
function verficar() {
    var data = new Date()
    var ano = data.getFullYear()
    var fano = document.getElementById(`txtano`)
    var res = document.querySelector(`div#home`)
    if (fano.value.length == 0 || Number(fano.value) > ano) {
        alert("[ERRO] verifica os dados e tente novamente!")
    } else {
        var fsex = document.getElementsByName(`radsexo`)
        var idade = (ano - Number(fano.value))
        var genero = ''
        var img = document.createElement('img')
        img.setAttribute('id', 'foto')

        if (fsex[0].checked) {
            genero = 'Homem'
            if (idade >= 0 && idade < 10) {
                //crianca
                img.setAttribute(`src`, `crianca.png`)
            } else if (idade < 21) {
                //jovem
                img.setAttribute(`src`, `rapaz.png `)
            } else if (idade < 50) {
                //Adulto
                img.setAttribute(`src`, `jovem.png`)
            } else {
                //velho
                img.setAttribute(`src`, `velho.png`)
            }
        } else if (fsex[1].checked) {
            genero = 'Mulher'
            if (idade >= 0 && idade < 10) {
                //crianca
                img.setAttribute(`src`, `acrianca.png`)
            } else if (idade < 21) {
                //jovem
                img.setAttribute(`src`, `rapariga.png`)
            } else if (idade < 50) {
                //Adulto
                img.setAttribute(`src`, `ajovem.png`)
            } else {
                //velho
                img.setAttribute(`src`, `velha.png`)
            }
        }
        res.innerHTML = `Detectamos ${genero}    com, ${idade} anos `
        res.getElementsByClassName.textAlign = `center`
        res.appendChild(img)
    }
}
