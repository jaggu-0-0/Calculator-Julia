# Calculator-Julia
Simple calculator in Julia which can handle division by 0 and also error outputs.
- use nano or any similar window to execute in the terminal.
  1. save the file using CtrlO and Enter in nano
  2. open in terminal by 'julia filename'
  3. enjoy
```````````````````````````````````````
println("Enter the first number: ")
num1 = parse(Float64, readline())

println("Enter the second number: ")
num2 = parse(Float64, readline())

println("Enter operation (+, -, *, /): ")
operation = readline()

if operation == "+"
    result = num1 + num2
elseif operation == "-"
    result = num1 - num2
elseif operation == "*"
    result = num1 * num2
elseif operation == "/"
    if num2 == 0
        println("Cannot divide by zero.")
    else
        result = num1 / num2
    end
else
    println("Invalid operation.")
end

if @isdefined result
    println("Result: $result")
end
````````````````````````````````````````````````````
