<template>
  <router-view />
</template>

<style>
:root {
  --backgroundColor: #141414;
  --borderColor: #1c1c1c;
}

* {
  font-family: "Exo 2", sans-serif;
}
.container-fluid {
  background: rgb(0, 103, 34);
  background: radial-gradient(circle, rgb(0, 103, 34), rgba(28, 28, 28, 1) 35%);
}
.sidePanel {
  height: 100vh;
  background-color: var(--backgroundColor);
}
.mainPanel {
  height: 99.5vh;
}
.profileContainer h2 {
  font-size: 2rem;
}
.profileContainer p {
  font-size: 1rem;
}
.myProfile {
  width: 120px; /* Adjust image width */
  height: 120px; /* Adjust image height */
  border-radius: 50%; /* Make it round */
}
.featuredImg {
  width: 65%;
  height: auto;
  object-fit: cover;
  border-top: 1px solid gray;
  border-right: 1px solid gray;
  border-left: 1px solid gray;
  padding: 5px 5px 0 5px;
}
.parent {
  display: grid;
  grid-template-columns: repeat(2, 1fr) 2fr;
  grid-template-rows: repeat(2, 1fr) 4fr;
  grid-column-gap: 25px;
  grid-row-gap: 25px;
}

.div1 {
  grid-area: 1 / 1 / 2 / 2;
}
.div2 {
  grid-area: 1 / 2 / 2 / 3;
}
.div3 {
  grid-area: 2 / 1 / 3 / 2;
}
.div4 {
  grid-area: 2 / 2 / 3 / 3;
}
.div5 {
  grid-area: 1 / 3 / 3 / 4;
}
.div6 {
  grid-area: 3 / 1 / 4 / 3;
}
.div7 {
  grid-area: 3 / 3 / 4 / 4;
}
.certificateBox {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
  grid-column-gap: 20px;
  grid-row-gap: 20px;
}

.certi1 {
  grid-area: 1 / 1 / 2 / 2;
}
.certi2 {
  grid-area: 1 / 2 / 2 / 3;
}
.certi3 {
  grid-area: 1 / 3 / 2 / 4;
}
.certi4 {
  grid-area: 2 / 1 / 3 / 2;
}
.certi5 {
  grid-area: 2 / 2 / 3 / 3;
}
.certi6 {
  grid-area: 2 / 3 / 3 / 4;
}
.certificateImg {
  width: 100%;
  height: 80%;
  object-fit: cover;
  padding: 4px;
  border: 1px solid var(--borderColor);
}
.parent div {
  border: 1px solid var(--borderColor);
  background-color: var(--backgroundColor);
}
.viewAll {
  position: relative;
}
.viewAll::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 2px;
  border-radius: 4px;
  background-color: #198754;
  bottom: 0;
  left: 0;
  transform-origin: right;
  transform: scaleX(0);
  transition: transform 0.3s ease-in-out;
}
.viewAll:hover::before {
  transform-origin: left;
  transform: scaleX(1);
}
.sidePanel .navLink:hover {
  color: #198754 !important;
}
footer a:hover {
  color: #198754 !important;
}
.certificateName {
  color: #c9c9c9;
}
.card {
  width: 48rem;
  height: 23rem;
  background-color: var(--backgroundColor) !important;
}
.aboutProfile {
  width: 100%;
  height: auto;
  object-fit: cover;
}
.little {
  letter-spacing: 1px;
}
.projectImg {
  width: 100%;
  height: 240px;
  object-fit: cover;
}

.footer div {
  border: none;
}
.projectCategory {
  border: 1px solid var(--borderColor);
  color: #c9c9c9 !important;
}
.projectCards {
  border: 1px solid var(--borderColor);
}
.searchBtn {
  color: var(--borderColor);
}
.searchBoxFrame {
  border: 1px solid var(--borderColor);
}
.searchBox {
  background: transparent;
  border: none;
  color: white;
  /* background: rgba(34, 34, 34, 1) 40%; */
}
.projectCards {
  background-color: var(--backgroundColor);
}

@media (max-width: 991.98px) {
  .searchBoxFrame {
    margin-top: 10px;
  }
}
</style>
