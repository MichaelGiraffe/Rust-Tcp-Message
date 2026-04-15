//проверка стиля кода
//#![warn(clippy::all, clippy::pedantic)]
//потом в консоли можно написать cargo flippy

//бинарный поиск
//работает только со сортированными массивами!!!!

//для строк 41-47 подключить модуль
//use std::cmp::Ordering;

fn main()
{
    let arr:[i32;10]=[-1,3,5,7,8,10,24,37,42,135];

    let result = bin_search(&arr, 23);

    match result
    {
        Some((found_value,found_index))=>println!("found value {found_value} at {found_index}"),
        None=>println!("Not found")
    }

        
}

//&-это заимствование
fn bin_search(arr: &[i32], desired_value: i32)->Option <(i32,usize)>
{
    let mut low_bound: usize=0;
    let up_bound: usize=arr.len()-1;
    let mut i: usize=0;

    while low_bound <= up_bound{
        i+=1;
        let mid:usize=(up_bound+low_bound)/2;

        let mid_value:i32=arr[mid];
        if mid_value ==desired_value{
            return Some((mid_value,mid));
        } else if desired_value>mid_value{
            low_bound=mid+1;
        }
        //альтернатива
        /*
        match mid_value.cmp(&desired_value)
        {
            Ordering::Equal => return Some((mid_value,mid)),
            Ordering::Greater => up_bound= mid - 1,
            Ordering::Less => low_bound = mid + 1,
        }
        */
        println!("Step {i}");
    }

    None
}



#[cfg(test)]
//модуль 
mod tests
{
    use super::*;

    const ARR:[i32;10]=[-1,3,5,7,8,10,24,37,42,135];

    #[test]
    fn element_found()
    {
        assert_eq!((-1,0),bin_search(&ARR,-1).unwrap());
    }
}

