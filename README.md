# jetweb-search
Google search wrapper. Asychronously retrieves multiple pages of searches and returns them as a simple array of result objects. 
It uses the google-this package under the hood so if you need finer control of your search check out that package.
the googleSearch method takes to parameters. First the term which can be any syntax allowed by google, second the number of pages you want
returned.

## Example usage
npm install jet-search<br>
const googleSearch = require('jet-search');


const myterm = 'yamaha xt 600';<br>
const mypages = 3;

const myFunction = (term, pages) => {<br>
  const results = await googleSearch(term, pages);<br>
  console.log(results);<br>
}

myFunction(myTerm, myPages);


## Example return: <br>
[<br>
OrganicResult {
      title: 'XT 600 - Barkbusters Moto',
      description: 'You have selected Yamaha XT 600. SABRE. Single Point Mount. JET. Single Point Mount. Two Point Mount. EGO. Will not fit this model.',
      url: 'https://barkbusters.net/what-fits-my/yamaha/xt600/',
      favicons: [Object]
    },<br><br>
    OrganicResult {
      title: 'yamaha xt600',
      description: 'Front Brake Clutch Levers Replacement for Yamaha YZ80 YZ100 YZ125 TW200 XT225 250 XT250 TTR250 IT125 IT200 XT350 XT600 TT600 MX100 BW200 TT250 TT350,Silver.',
      url: 'https://www.amazon.com/yamaha-xt600/s?k=yamaha+xt600',
      favicons: [Object]
    }<br>
  ]

