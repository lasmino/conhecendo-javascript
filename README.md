# conhecendo-javascript
iniciando_js
function carregar() {
    var mesg = document.getElementById('msg')
    var img = document.getElementById('imagens')
    var hora = new Date()
    var agora = hora.getHours()
    mesg.innerText = `agora sao ${agora} horas `
    if (agora >= 0 && agora < 12) {
        //manha
        img.src = "foto/manhana.png"
        document.body.style.background = '#1F212F'
    } else if (agora >= 12 && agora < 18) {
        //tarde
        img.src = "foto/tardea.png"
        document.body.style.background = '#795F12'
    } else if (agora >= 18 && agora <= 23) {
        img.src = "foto/noitea.png"
        document.body.style.background = '#131315'
            //noite
    } else {
        mesg.innerText = 'Erro! as horas sao invaldas'
        document.body.style.background = '#072034'
        img.src = innerText('Ohps!')

        //madrugada
    }

}
