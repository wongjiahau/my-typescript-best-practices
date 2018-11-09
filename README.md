# My TypeScript Best Practices

1. Create an `index.js` files that calls the transpiled JavaScript code.

2. Enable all strict checking in `tsconfig.json`. 

    - This will saves you a lot of time from debugging runtime errors (such as null pointer exceptions)

3. Use TSLint.

    - `npm i -g tslint && tslint init`

4. Use Jest for running unit tests

    - Use `ts-jest` [Refer here](https://www.npmjs.com/package/ts-jest)

5. Specify the output directory in `tsconfig.json`.

6. Run the TypeScript compiler using `--watch` options.

    - `tsc --watch`


## Code related guidelines

- Don't use OOP even though you can 

    - They are hard to test against

    - Use [interface](https://www.typescriptlang.org/docs/handbook/interfaces.html) instead

- Use FP style instead

    - Use [discriminated unions](https://basarat.gitbooks.io/typescript/docs/types/discriminated-unions.html)

    - Use [spread operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

    - Use filter, map, reduce 
    
        - You can convert them to for loop later if you are very sure that the micro-optimization will help to improve performance
    
- Function should never modifies the input

- Function should never modifies the input 

- Function should never modifies the input (unless you are very very very very very very very clear about what you do)


    

## Problems you might faced

1. Deleting a file during `--watch` mode will not causes its corresponding JS file to be deleted

    - Refer https://github.com/Microsoft/TypeScript/issues/16057

2. Unit test might take a bit longer to run (if your laptop is slow)

3. A lot of compiler errors 

    - This is actually good, because its better to fix compile-time errors than to fix runtime errors (that's why Haskell is so strict)
    

### P/S: This is only my opinion, it may not necessarily fits your development, so contemplate at your own risk.
