import { useState } desde "react";
importar JSConfetti desde 'js-confetti'
Aplicación de funciones() {


  const jsConfetti = nuevo JSConfetti()
  const [randomValor, setRandomValor] = useState({})

  const [imagenCargada, setImagenCargada] = useState(false);
  const [agrandar, setAgrandar] = useState(45)


  const [valueSi, setValueSi] = useState(false)

  Que sea aleatorio = [{
    Código: 1,
    description: "Di si por favor",
    img: "https://i.pinimg.com/originals/db/aa/c1/dbaac13f6278b91a15e480752b8a7242.gif"
  },
  {
    Código: 1,
    descripción: "Piénsalo de nuevo".,
    img: "https://i.pinimg.com/originals/77/6b/21/776b215bed3deeef47fd3aa657685a18.gif"
  }
    ,
  {
    Identificación: 2,
    description: "Vamos, atrévete a decir que sí.",
    img: "https://www.gifmaniacos.es/wp-content/uploads/2019/05/gatitos-kawaii-gifmaniacos.es-19.gif"
  },
  {
    Identificación: 3,
    description: "No tengas miedo, será genial.",
    img: "https://i.pinimg.com/originals/e1/c3/88/e1c388133e0f998e25bb17c837b74a14.gif"
  },
  {
    Código: 4,
    description: "Confía en mí, será divertido.",
    img: "https://media.tenor.com/Bn88VELdNI8AAAAi/peach-goma.gif"
  },
  {
    Identificación: 5,
    description: "No tengas dudas, te hará sonreír.",
    img: "https://i.pinimg.com/originals/c6/b3/0d/c6b30d1a2dc178aeb92de63295d4ae64.gif"
  },
  {
    Código: 6,
    description: "Te prometo que será inolvidable.",
    img: "https://media.tenor.com/N2oqtqaB_G0AAAAi/peach-goma.gif"
  },
  {
    Código: 7,
    description: "No dejes que el miedo te detenga.",
    img: "https://i.pinimg.com/originals/db/aa/c1/dbaac13f6278b91a15e480752b8a7242.gif"
  },
  {
    Código: 8,
    description: "Confía en el destino, nos está dando una señal.",
    img: "https://media.tenor.com/cbEccaK9QxMAAAAi/peach-goma.gif"
  },
  {
    Identificación: 9,
    description: "Confía en mí.",
    img: "https://i.pinimg.com/originals/db/aa/c1/dbaac13f6278b91a15e480752b8a7242.gif"
  },
  {
    Código: 10,
    description: "No te arrepentirás.",
    img: "https://media.tenor.com/I7KdFaMzUq4AAAAi/peach-goma.gif"
  }]

  const randomResponse = () => {
    let index = Matemáticas.piso(Matemáticas.aleatorio() * 11);
    consola.log(random[índice])
    if (agrandar <= 500) {
      setAgrandar(agrandar + 10)
    }
    setRandomValor(random[index]);
  }


  const handleImageLoad = () => {
    setImagenCargada(true);
  }


  devolución (
    <main id="canvas" className="fondo w-screen h-screen bg-no-repeat bg-cover flex items-center justify-center bg-center ">
      {
        !valueSi ? (
          <div nombredeclase="p-5">
            <h1 className="text-white font-bold text-5xl text-center">¿Quieres ser mi San Valentin? </h1>
            <img src={Objeto.keys(randomValor).longitud === 0 ?
              "https://i.pinimg.com/originals/db/aa/c1/dbaac13f6278b91a15e480752b8a7242.gif" : valor aleatorio.img} alt="San Valentin" className="mx-auto" width={400} height={400} />
            <div className="grid grid-cols-1 md:grid-cols-2 mt-10 gap-5 items-center">
              <botón enHaga clic={() => {
                setValueSi(true)

                jsConfeti.addConfetti({
                  emojis: ['', '', '', '😍 🥰 ❤️ 😘'],
                  emojiTamaño: 70,
                  confetiNúmero: 80,
                })

              }} className={'bg-green-500 text-white font-bold p-2 rounded-md text-xl h-${agrandar}'} style={{ height: agrandar   }}>
                Si
              </botón>
              <botón
                className="bg-red-500 text-white font-bold p-2 rounded-md text-xl"
                onClick={randomResponse}
                disabled={imagenCargada} // Deshabilita el botón si la imagen no se ha cargado
              >
                {Objeto.keys(randomValor).longitud === 0 ? "No" : randomValor.descripción}
              </botón>
            </Div>
          </Div>
        ) : (
          <div className="flex justify-center items-center flex-col space-y-10">
            <h1 className="text-4xl text-white font-bold">Sabia que dirias que si ❤️ ! </h1>
            <img src="https://i.pinimg.com/originals/9b/dc/c6/9bdcc6206c1d36a37149d31108c6bb41.gif" alt="" className="mx-auto" />
          </Div>
        )
      }
    </principal>
  )
}

exportar la aplicación predeterminada
