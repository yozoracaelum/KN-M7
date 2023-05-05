# KN-M7

![1](https://user-images.githubusercontent.com/86104516/236393692-699638ea-8456-47cc-befd-75a91c4dfa8c.png)

![3](https://user-images.githubusercontent.com/86104516/236393995-95ec1f72-843a-4769-8fe6-b5c01ad20237.png)

## Metode Trapesium

```mermaid
graph TD;
    A([Mulai])-->B[/Input a, b, n/];
    B-->C("Definisi f(x)<br>h = (b-a)/n<br>I = f(a)+f(b)");
    C-->D{{for i = 1 to n-1, do}};
    D-->E("j = a+(i*h)<br>I += 2*f(j)");
    E-->D;
    D-->F(I *= h/2);
    F-->G([Tampil I]);
    G-->I([Selesai]);
```

![2](https://user-images.githubusercontent.com/86104516/236393718-66e9d7b1-49b9-4401-a61e-8f5ff52fa97a.png)

## Metode 1/3 Simpson

```mermaid
graph TD;
    A([Mulai])-->B[/Input a, b, n/];
    B-->C("Definisi f(x)<br>h = (b-a)/n<br>I = f(a)+f(b");
    C-->D{{for i = 1 to n-1, do}};
    D-->E("j = a+(i*h)");
    E-->F{if i mod 2 = 0};
    F--Y-->G("I += 2*f(j)");
    F--N-->H("I += 4*f(j)");
    G-->D;
    H-->D;
    D-->I(I *= h/3);
    I-->J([Tampil I]);
    J-->K([Selesai]);
```

![4](https://user-images.githubusercontent.com/86104516/236393973-9d434b5e-485b-450c-8eb5-66b857df55c9.png)

## Metode 3/8 Simpson

```mermaid
graph TD;
    A([Mulai])-->B[/Input a, b, n/];
    B-->C("Definisi f(x)<br>h = (b-a)/n<br>I = f(a)+f(b");
    C-->D{{for i = 1 to n-1, do}};
    D-->E("j = a+(i*h)");
    E-->F{if i mod 3 = 0};
    F--Y-->G("I += 2*f(j)");
    F--N-->H("I += 3*f(j)");
    G-->D;
    H-->D;
    D-->I("I *= (3/8)*h");
    I-->J([Tampil I]);
    J-->K([Selesai]);
```
