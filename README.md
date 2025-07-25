# khai báo hàm 
Từ khóa fn
fn add(x: Int, y:Int)
{
  x + y
}
fn multiply(x: Int, y: Int)->Int{
  x+y
}
,,,,

fn add_one(x: Int)->Int{
  x + 1
}
fn twice (f: fn(t)->t, x: t)->t{
  f(f(x))
}
fn add_two(x: Int)->Int{
  twice(add_one,x)
}
test tFunction(){
  add_two(2) == 2+ 1+1
}
...

# hàm ẩn danh(dùng để khai hàm ngay trong function khác )
fn run(){
  let add = fn(x,y){x+y}
  add(1,2)
}
test tAnony(){
  run() == 3
}

...
# Đối số có ràng buộc kiểu dữ liệu 
fn hello(s1: Int, s2: Int, s: Int){
  s1 + s2 == s
}
test thello(){
  hello(s1: 1, s2: 2, s: 3) == hello (s2: 2, s1: 1, s:3)
}
...
đặt tên biến ngắn
fn thelloworld(helloworld h: ByteArray ){
  h == "Hello World!"
}
test tDs(){
  thelloworld("Hello World!")
}
# validator
validator(assets: ByteArray){
  fn contract(datum: Data, redeemer: Void, ctx: Data){
    True
  }
  fn bid(datum: Data, ctx: Data){
    True
  }
}
# Toán tử pipe
|>
test tPipe(){
  let a = add(2, add(3, add(4,5)))
  let b = 
  5
  |> add(4)
  |> add(3)
  |> add(2)
  a==b
}
...
# Function capturing
test run2()
{
  let add_one = add(1, _)
  add_one(2) == 3
}
# Hàm chung
fn list_of_two(my_value m:a)-> List<a>{
  [m,m]
}
test double_number()
{
  list_of_two(2) == [2,2]
}
# Hàm trả về kiểu dữ liệu xác định 
fn add_three_number(x: Int, y: Int, z: Int)->Int{
  x + y + z
}
test add_three(){
  let a = 
  4
  |> add(5)
  |>add(6)
  a == add_three_number(4,5,6)
}