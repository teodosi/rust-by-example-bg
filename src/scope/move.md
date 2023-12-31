# Владение и премествания

Понеже променливите сами се грижат за освобождаване на заетата от тях част от
паметта, **данните могат да имат само един владелец (собственик)**. Това също
предотвратява възможността дадено парче данни да бъде освободено повече от веднъж.
Обърнете внимание, че не всички променливи владеят данни (препратките са
такива променливи).

Когато присвояваме стойност на променлива (`let x = y`) или подаваме аргументи
като стойност (не като препратка) (`foo(x)`), *владението* на данните бива
предадено на функцията. Казано по ръждьовски, това е *преместване*[^move].

След преместването предишният владелец (променлива) повече не може да бъде
ползван. Това предотвратява създаването на *висящи указатели*[^dangling].

```rust,editable
// Тази функция овладява заделената памет от купа
fn destroy_box(c: Box<i32>) {
    println!("Унищожаваме кутия, която съдържа {}", c);

    // `c` е унищожена и паметта е освободена
}

fn main() {
    // Паметта за това число е заделена в стълпа.
    let x = 5u32;

    // *Копираме* `x` в `y` – няма преместване на данни.
    let y = x;

    // И двете стойности могат да се ползват независимо една от друга.
    println!("x е {}, а y е {}", x, y);

    // `a` е указател към цяло число от купа̀.
    let a = Box::new(5i32);

    println!("a съдържа: {}", a);

    // *Местим* `a` в `b`
    let b = a;
    // Адресът на указателя на `a` е копиран (не самите данни) в `b`.
    // И двете променливи сега са указатели към едни и същи данни, заделени в
    // купа, но сега `b` *владее* данните.
    
    // Грешка! `a` повече няма достъп до данните, понеже вече не владее тези
    // данни от купа.
    //println!("a съдържа: {}", a);
    // ЗАДАЧА ^ Разкоментирайте този ред

    // Тази функция овладява заделената в купа памет, преди владяна от `b`
    destroy_box(b);

    // Понеже паметта от купа е освободена вече, следващото действие би
    // осъществило пряк достъп до вече освободена памет. Това е забранено от
    // компилатора.
    // Грешка! Поради същата причина като предишната грешка.
    //println!("b contains: {}", b);
    // ЗАДАЧА ^ Разкоментирайте този ред
}
```
## Б. пр.

[^move]: местене, преместване на данни (от една променлива в друга) – move

[^dangling]: висящ указател – dangling pointer

[references]: ../flow_control/match/destructuring/destructure_pointers.md
