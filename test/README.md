# This is a test
Example text

## List
1. A
2. B

---

```css
.user-profile-modal-v2 ._9c3bea41fd465666-profile {
  anchor-name: --profile-anchor;
  --tooltip-bg: color-mix(in oklab, var(--neutral-79) 100%, var(--custom-theme-base-color, #000) var(--custom-theme-base-color-amount, 0%));
  --tooltip-border: color-mix(in oklab,hsl(var(--opacity-12-hsl)/0.12156862745098039) 100%,hsl(var(--custom-theme-base-color-hsl,0 0% 0%)/0.12156862745098039) var(--custom-theme-border-color-amount,var(--custom-theme-base-color-amount,0%)));
    /* Edit fill (for bg) and color (for border) to be the same as above. %23 is # */
  --arrow-svg: url("data:image/svg+xml,%3Csvg fill='%2328242c' color='%23353139' width='16' height='10' viewBox='0 0 16 10' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath  d='M10.3426 7.0715C9.14163 8.57272 6.85837 8.57272 5.65739 7.0715L0 -0.000244141L16 -0.000244141L10.3426 7.0715Z'%3E%3C/path%3E%3Cpath stroke='currentColor' d='M9.93457 6.84546C8.93433 8.06766 7.06567 8.06766 6.06543 6.84546L0.0546875 -0.500244L15.9453 -0.500244L9.93457 6.84546Z'%3E%3C/path%3E%3C/svg%3E");
  
  ._9c3bea41fd465666-profileButtons {
    position: fixed; 
    top: calc(anchor(--profile-anchor start) + 12px);
    right: calc(anchor(--profile-anchor end) + 12px);

    button {
      background: var(--redesign-button-overlay-alpha-background) !important;
      border: 1px solid var(--opacity-white-8) !important;
      border-radius: 50%;
      &:hover, &:active {
        background: var(--redesign-button-overlay-alpha-pressed-background) !important;
      }
    }
    >button {
      min-width: 32px !important;

      >.a22cb0c66246f5d3-buttonChildrenWrapper {
        overflow: visible;
        padding: 0 !important;
        >.a22cb0c66246f5d3-buttonChildren {
          overflow: visible;
          justify-content: center;
        }
      }
      ._4bd5201c86a2042b-lineClamp1 {
        align-items: center;
        position: absolute;
        top: -52px;
        
        background-color: var(--tooltip-bg);
        border-radius: var(--radius-sm);
        box-shadow: inset 0 0 0 1px var(--tooltip-border), var(--shadow-high);
        color: var(--text-default);
        padding: var(--space-8) var(--space-12);
        pointer-events: none;
        
        display: flex;
        justify-content: center;
        overflow: visible;

        will-change: opacity, transform;
        opacity: 0;
        transform: scale(0.95);
        transform-origin: 50% 100%;
        transition: opacity 0.1s ease, transform 0.1s ease;
        &::after {
          content: var(--arrow-svg);
          position: absolute;
          bottom: -13px;
        }
      }
      &:hover ._4bd5201c86a2042b-lineClamp1 {
        opacity: 1;
        transform: scale(1);
      }
    }
  }
}
```

```js
((input = prompt("Enter number as a word: ").replace("config", "")) => {
    const smallValues = {
        hundred: 100n, ninety: 90n, eighty: 80n, seventy: 70n, sixty: 60n,
        fifty: 50n, forty: 40n, thirty: 30n, twenty: 20n, nineteen: 19n,
        eighteen: 18n, seventeen: 17n, sixteen: 16n, fifteen: 15n,
        fourteen: 14n, thirteen: 13n, twelve: 12n, eleven: 11n, ten: 10n,
        nine: 9n, eight: 8n, seven: 7n, six: 6n, five: 5n, four: 4n,
        three: 3n, two: 2n, one: 1n, zero: 0n, "": null, 
    };
    const bigValues = [
        "thousand", "million", "billion", "trillion", "quadrillion",
        "quintillion", "billion", "trillion", "quadrillion", "quintillion",
        "sextillion", "septillion", "octillion", "nonillion", "decillion",
        "undecillion", "duodecillion", "tredecillion", "quattuordecillion",
        "quindecillion", "sexdecillion", "septendecillion", "octodecillion",
        "novemdecillion", "vigintillion",
    ];
    function parseNumberWord(inputStr) {
        let tempInput = inputStr.toLowerCase().replaceAll(/[^a-z]/g, "");
        console.log(tempInput);
        let lastTempInput = null;
        let total = 0n;
        while (tempInput != "") {
            lastTempInput = tempInput;
            let smallMultiplier = 0n;
            SmallMultLoop: for (let i = 0; i < 4; i++) {
                for (const small in smallValues) {
                    if (small == "") break SmallMultLoop;
                    if (!tempInput.startsWith(small)) continue;
                    tempInput = tempInput.replace(small, "").trim();
                    if (small == "hundred") {
                        smallMultiplier *= 100n;
                    } else {
                        smallMultiplier += smallValues[small];
                    }
                    break;
                }
            }
            let bigMultiplier = 1n;
            for (const i in bigValues) {
                if (!tempInput.startsWith(bigValues[i])) continue;
                tempInput = tempInput.replace(bigValues[i], "").trim();
                bigMultiplier = 10n ** BigInt(3 * (parseInt(i) + 1));
                break;
            }
            total += smallMultiplier * bigMultiplier;
            if (tempInput == lastTempInput) return;
        }
        return total;
    }
    const formatter = new Intl.NumberFormat("en-US");
    console.log(formatter.format(parseNumberWord(input)));
})();
```

```excel
=let(num,(width-5-1)/(height-5),input,{"#fff";array_constrain(filter(flatten(color), not(isblank(flatten(color)))),num,1)}, sparkline({mod(num,1)*if(centered,0.5,0);sequence(rows(input) - 1,1,1,0);mod(num,1)*if(centered,0.5,1)},{"charttype","bar";map(sequence(rows(input)),lambda(i, {"color"&i,index(input,i)}))}))
```
```cpp
=let(num,(width-5-1)/(height-5),input,{"#fff";array_constrain(filter(flatten(color), not(isblank(flatten(color)))),num,1)}, sparkline({mod(num,1)*if(centered,0.5,0);sequence(rows(input) - 1,1,1,0);mod(num,1)*if(centered,0.5,1)},{"charttype","bar";map(sequence(rows(input)),lambda(i, {"color"&i,index(input,i)}))}))
```