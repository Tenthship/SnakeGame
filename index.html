// Variables
const canvas = document.querySelector('canvas')
const c = canvas.getContext('2d')
const scoreEl = document.querySelector('#score')
var score = 0
const width = window.innerWidth
const height = window.innerHeight
const sizing = 50
const snakeArray = []
const size = 0.9 * sizing
let animationId
var randPos = {
    x: 0,
    y: 0
}
var directions = {
    right: false,
    up: false,
    left: false,
    down: false
}

// Setting up canvas
canvas.width = 17 * sizing
canvas.height = 15 * sizing
canvas.style.position = 'absolute';
canvas.style.left = `${(width / 2) - (canvas.width / 2)}px`
canvas.style.top = `${(height / 2) - (canvas.height / 2)}px`

function init(){
    // Setting vertical lines
    for(var i = sizing; i < canvas.width; i += sizing){
        c.beginPath()
        c.moveTo(i, 0)
        c.lineTo(i, canvas.height)
        c.strokeStyle = 'white'
        c.stroke()
    }

    // Setting horizontal lines
    for(var i = sizing; i < canvas.height; i += sizing){
        c.beginPath()
        c.moveTo(0, i)
        c.lineTo(canvas.width, i)
        c.strokeStyle = 'white'
        c.stroke()
    }
}



// Creating snake
class Snake{
    constructor(position){
        this.position = position
        this.size = size
        this.velocity = {
            x: 0,
            y: 0
        }
        this.directions = {
            right: false,
            up: false,
            left: false,
            down: false
        }
    }
    draw(){
        c.fillStyle = 'green'
        c.fillRect(this.position.x + (sizing - this.size) / 2, this.position.y  + (sizing - this.size) / 2, this.size, this.size)
    }
    update(){
        this.position.x += (this.velocity.x * sizing)
        this.position.y += (this.velocity.y * sizing)
    }
}

class Fruit{
    constructor(position){
        this.position = position
        this.size = size
    }
    draw(){
        c.fillStyle = 'red'
        c.fillRect(this.position.x + (sizing - this.size) / 2, this.position.y  + (sizing - this.size) / 2, this.size, this.size)
    }
}

const snake = new Snake({
    x: 3 * sizing,
    y: 7 * sizing
})

snakeArray[0] = snake

var fruit = new Fruit({
    x: 7 * sizing,
    y: 10 * sizing
})


function animate(){
    animationId = requestAnimationFrame(animate)
    c.clearRect(0, 0, canvas.width, canvas.height)
    snakeArray.forEach((snake) => {
        snake.draw()
    })
    fruit.draw()
    if(snake.position.x === fruit.position.x && snake.position.y === fruit.position.y){
        if(directions.right === true){
            snakeArray.push(new Snake({
                x: snake.position.x - sizing,
                y: snake.position.y
            }))
        }else if(directions.up === true){
            snakeArray.push(new Snake({
                x: snake.position.x,
                y: snake.position.y + sizing
            }))
        }else if(directions.left === true){
            snakeArray.push(new Snake({
                x: snake.position.x + sizing,
                y: snake.position.y
            }))
        }else if(directions.down === true){
            snakeArray.push(new Snake({
                x: snake.position.x,
                y: snake.position.y - sizing
            }))
        }

        score += 1
        scoreEl.innerHTML = score
        randPos.x = Math.floor(Math.random() * 17) * sizing
        randPos.y = Math.floor(Math.random() * 15) * sizing
        for(let k = 0; k < snakeArray.length; k++){
            while(randPos.x === snakeArray[k].position.x && randPos.y === snakeArray[k].position.y){
                randPos.x = Math.floor(Math.random() * 17) * sizing
                randPos.y = Math.floor(Math.random() * 15) * sizing
            }
        }

        fruit = new Fruit({
            x: randPos.x,
            y: randPos.y
        })
    }
    if(snake.position.x < 0 || snake.position.x > canvas.width - sizing || snake.position.y < 0 || snake.position.y > canvas.height - sizing){
        cancelAnimationFrame(animationId)
    }

    for(let p = 1; p < snakeArray.length; p++){
        if(snakeArray[p].position.x === snake.position.x && snakeArray[p].position.y === snake.position.y){
            cancelAnimationFrame(animationId)
        }
    }



    init()
  
}

setInterval(() => {
    for(let i = snakeArray.length - 1; i > 0; i--){
        snakeArray[i].position.x = snakeArray[i - 1].position.x
        snakeArray[i].position.y = snakeArray[i - 1].position.y
    }

    snakeArray[0].update()

}, 200)

window.addEventListener('keydown', (event) => {
    switch(event.key){
        case 'ArrowRight':
            snake.velocity.x = 1
            snake.velocity.y = 0
            directions.right = true
            directions.up = false
            directions.left = false
            directions.down = false
            break
            case 'ArrowUp':
            snake.velocity.x = 0
            snake.velocity.y = -1
            directions.right = false
            directions.up = true
            directions.left = false
            directions.down = false
            break
        case 'ArrowLeft':
            snake.velocity.x = -1
            snake.velocity.y = 0
            directions.right = false
            directions.up = false
            directions.left = true
            directions.down = false
            break
        case 'ArrowDown':
            snake.velocity.x = 0
            snake.velocity.y = 1
            directions.right = false
            directions.up = false
            directions.left = false
            directions.down = true
    }
})


animate()

