# To-Do-App
This is to do application (Here we will create the front end and back end )

const express = require ("express")
const cros = require("cros")
const bodyParser = require("body-parser")

const app = express();
app.use(cros())
app.use(bodyParser.json())
app.use(express.json())

app.get("/", (req,res)=>{
    res.status(200).json({message:"Hello from express server"})
})

const PORT = 3001;
app.listen(PORT,()=>{
    //console.log("Server is running on the port", PORT)
    console.log(`Server is running on the port ${PORT}`)
})
//app.use()
