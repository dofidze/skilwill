# skilwill
///
// დავალება პირველი
///
function expo(number, quality, callback) {
  if (quality == 0) return 1;
  if (quality == 1) return number;
  else {
    return number * expo(number, quality - 1, callback);
  }
}

function printResult(result) {
  print(`The result is`, result);
}

const expoResult = expo(5, 3, printResult);

console.log(expoResult);

   
// დავალება მეორე

function displayPostTitle() {
  fetch("https://jsonplaceholder.typicode.com/posts")
    .then((res) => res.json())
    .then((data) => {
      const post = data[0];
      const postTitle = post.title;

      const postTitleElement = document.createElement("h1");
      postTitleElement.textContent = postTitle;
      document.body.appendChild(postTitleElement);
    })
    .catch((error) => {
      console.log("Error:", error);
    });
}

displayPostTitle();
   
// დავალება მესამე
//

async function deepCopyObject(obj) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      try {
        const clonedObj = JSON.parse(JSON.stringify(obj));
        resolve(clonedObj);
      } catch (error) {
        reject(error);
      }
    }, 0);
  });
}

const obj = { foo: "ობიექტი", nested: { baz: "ობიექტი" } };

deepCopyObject(obj)
  .then((clonedObj) => {
    console.log("Deep copy:", clonedObj);
  })
  .catch((error) => {
    console.log("Error:", error);
  });

async function deepCopyObject(obj) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (typeof obj !== "object" || obj === null) {
        reject(new Error("Invalid argument. Expected an object."));
      } else {
        try {
          const clonedObj = JSON.parse(JSON.stringify(obj));
          resolve(clonedObj);
        } catch (error) {
          reject(error);
        }
      }
    }, 0);
  });
}
   
   
   
   
   
   
   
   
   
   
   
   
   
   
   
    
    
