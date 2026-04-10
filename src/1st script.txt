fn main() 
{
    let mut a=42;//mut для изменяемой переменной
    println!("Hello, world! The value: {a}");

    // SCALAR (типы)
    // Integer
    let b:u8;//i8;  //в u8 8 это 2^8 размер
    // u - unsigned (не имеет отрицательных чисел)
    // i - signed 
    let c:i128; 
    //let d:isize;//arch (зависит от архитектуры процессора)
    let hex=0xab;//16-ти ричное
    //0o - octal (8-ми ричное)
    //0b -binary (двоичное)

    //float
    // f32
    // f64

    //bool
    //char


    //COMPOUND (составной тип-храним вместе)
    // Tuple -картеж
    let myTuple: (i8,char,bool)=(42,'f',false);
    //Array
    let arr=[1,2,3];
}
