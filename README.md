# jetweb-search
Google and Bing search wrapper. Asychronously retrieves multiple pages of either a Bing or Google search and returns them as a simple array of result objects<br>.

The googleSearch method takes two parameters. First the term which can be any syntax allowed by Google or Bing depending on which search you are doing. Second is the number of pages you want returned. You do a Microsoft Bing search (bingSearch(term, pages)) with the same parameters.<br>

The search methods return a promise, so either async await or val.then() must be used.
 


## Example usage
npm install jet-search<br><br>

const googleSearch = require('jet-search');<br>
const bingSearch = require('jet-search');<br><br>

const googleResults = await googleSearch('yamaha xt500', 2);<br>
console.log(results);<br><br>

const bingResults = await bingSearch('yamaha xt600', 3);<br>
console.log(bingResults);<br><br>



## Example return: <br>
[<br>
    OrganicResult {
      title: 'XT 600 - Barkbusters Moto',
      description: 'You have selected Yamaha XT 600. SABRE. Single Point Mount. JET. Single Point Mount. Two Point Mount. EGO. Will not fit this model.',
      url: 'https://barkbusters.net/what-fits-my/yamaha/xt600/',
      favicons: [Object]
    },<br>
    OrganicResult {
      title: 'yamaha xt600',
      description: 'Front Brake Clutch Levers Replacement for Yamaha YZ80 YZ100 YZ125 TW200 XT225 250 XT250 TTR250 IT125 IT200 XT350 XT600 TT600 MX100 BW200 TT250 TT350,Silver.',
      url: 'https://www.amazon.com/yamaha-xt600/s?k=yamaha+xt600',
      favicons: [Object]
    }<br>
  ]

