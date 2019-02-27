# NPM Truffle box

NPM Truffle box makes it easy to modularize your truffle project as an npm module.
It contains `truffle-plugin-modularizer` which exports the json files in `build/contracts/` and create `src/index.js`.

You can get following benefits:
- You can import contracts as an instance of `truffle-contract`
  ```
  import { SampleContract } from 'your-project-name'
 
  web3 = window.web3

  SampleContract(web3).new().then(
      async instance => {
        await instance.add(10)
        await instance.add(20)
        await instance.add(30)
        let values = await instance.getValues()
        console.log("Values: ", values)
      }
  )
  ```
- It saves the deployed addresses
  ```
  SampleContract(web3).deployed().then(
      async instance => {
        await instance.add(10)
        await instance.add(20)
        await instance.add(30)
        let values = await instance.getValues()
        console.log("Values: ", values)
      }
  )
  ```
- 
, so if you d
Because you can configure custom settings
Thus, when you want to make a ReactJS application, start with this truffle box and deploy 
