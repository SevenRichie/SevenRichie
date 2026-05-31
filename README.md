```js
const profile = {
    nick: "SevenRichieWhite",
    firstAlias: "Seven",
    secondAlias: "Richie",
    stack: ["HTML", "CSS", "JS", "PHP", "Twig"]
};

const mode = "public"; // public | friend-1 | friend-2

const displayName = document.getElementById("display-name");
const stackList = document.querySelector(".stack");

if (mode === "friend-1") {
    displayName.textContent = profile.firstAlias;
} else if (mode === "friend-2") {
    displayName.textContent = profile.secondAlias;
} else {
    displayName.textContent = profile.nick;
}

stackList.innerHTML = profile.stack
    .map(item => `<li>${item}</li>`)
    .join("");
```
