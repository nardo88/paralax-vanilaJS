# paralax-vanilaJS

https://nardo88.github.io/paralax-vanilaJS/


```javascript
        window.addEventListener('scroll', e => {
            const target = document.querySelectorAll('.scroll');
           
            const scrolled = window.pageYOffset;
            const rate = scrolled * -2;
            
            target.forEach(item => {
                const pos = window.pageYOffset * item.dataset.rate;
                if (item.dataset.direction === 'vertical'){
                    item.style.transform = `translate3d(0px, ${pos}px, 0px )`

                } else {
                    const posX = window.pageYOffset * item.dataset.ratex;
                    const posY = window.pageYOffset * item.dataset.ratey;
                    item.style.transform = `translate3d(${posX}px, ${posY}px, 0px )`;
                }
            })
        })
```



```html
    <section>
        <ul>
            <li class="scroll" data-rate="-2" data-direction="vertical">par</li>
            <li>al</li>
            <li class="scroll" data-rate="2" data-direction="vertical">lax</li>
        </ul>
        <span class="scroll" data-rateY="1" data-rateX="2" data-direction="horizontal"></span>
    </section>
    <section></section>
```