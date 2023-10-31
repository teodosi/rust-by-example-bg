# Rust в примери

[![Build Status][travis-badge]][travis-repo]

[travis-badge]: https://travis-ci.com/rust-lang/rust-by-example.svg?branch=master
[travis-repo]: https://travis-ci.com/rust-lang/rust-by-example

Да научим Ръст чрез примери (с включен редактор наживо)

## Употреба

Ако желаете да четете „Rust by Example” (първоизточника), посетете
<https://doc.rust-lang.org/rust-by-example/>, за да я прочетете в мрежата.

Ако искате да прочетете този превод на книгата на вашето сметало,
[инсталирайте Ръст], и после изпълнете:

```bash
git clone https://github.com/kberov/rust-by-example-bg
cd rust-by-example-bg
cargo install mdbook
mdbook build
mdbook serve
```

[инсталирайте Ръст]: https://www.rust-lang.org/tools/install

За да изпълните примерите, трябва да сте свързани към интернет, но можете и да
четете на собственoто си сметало.

## Принос

Моля, вижте файла [CONTRIBUTING.md] за повече подробности.

[CONTRIBUTING.md]: https://github.com/kberov/rust-by-example-bg/blob/master/CONTRIBUTING.md

## Преводи на други езици

* [Chinese](https://github.com/rust-lang-cn/rust-by-example-cn)
* [Japanese](https://github.com/rust-lang-ja/rust-by-example-ja)
* [French](https://github.com/Songbird0/FR_RBE)
* [Russian](https://github.com/ruRust/rust-by-example)
* [Vietnamese](https://github.com/EyesCrypto-Insights/rust-by-example-vn)
* [Portuguese](https://github.com/nazarepiedady/rust-com-exemplos)

## За този превод

Започнах този превод на единадесети април 2023 г. в болница „Св. Иван Рилски” в
Козлодуй. Днес първи ноември 2023 г., Ден на народните будители – по старому
денят на св. Иван Рилски, пускам превода „както е” за свободно четене.

Посвещавам този превод на свети Иван Рилски и всички негови духовни чѧда –
народни будители.

Благодаря на благовѣрната си съпруга за помощта с поправянето на безбройните ми
правописни грешки. Има още.

Докато работех по превода, намирах грешки и пропуски в първоизточника и правех
заявки за сливане там. Благодарение на този превод "Rust by example" също бе
подобрен.

Тази книга е непълноценна, освен че е написана доста пестеливо. Често ми се
налагаше да разследвам и дообяснявам, понеже не се разбираше достатъчно добре
от самия словоплет. Липсва ѝ един пример – истинско приложение на дадените
примери. Пример, показващ взаимодействието между отделните части на езика. След
като добавя една глава, описваща пълноценна програма, ще издам цялото на хартия.
Описанието на програмата ще е пълно с препратки към отделните примери в
книгата. Така читателят ще може да види Ръждьо в действие.

Раздел „22.1 Вписан асемблер” е доникъде. Не разбирам от асемблер. Ако вие
разбирате, помогнете в духа на превода. Багодаря.

Красимир Беров, 2023-10-01

## Лиценз

Българският превод на „Ръст в примери“ © 2023 от [Красимир Беров](https://github.com/kberov)
е лицензиран по CC BY-NC-SA 4.0 – [Признание-Некомерсиално-Споделяне на споделеното 4.0
Международен](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.bg).

Първоизточникът на „Ръст в примери” е лицензиран по ваш избор:

* Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) или
  <http://www.apache.org/licenses/LICENSE-2.0>)
* MIT license ([LICENSE-MIT](LICENSE-MIT) или
  <http://opensource.org/licenses/MIT>).

Освен ако кажете изрично нещо различно, всеки съзнателен принос към
„Ръст в примери”, както е определен в лиценза Apache-2.0, се лицензира двуяко
както по-горе, без никакви допълнителни правила и условия.

