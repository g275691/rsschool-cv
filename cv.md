# GEORGE GORSHKOV
![George Gorshkov-developer](https://raw.githubusercontent.com/g275691/rsschool-cv/gh-pages/img/mini-gosh2.jpg)
## __JAVASCRIPT DEVELOPER__


### Contact me:
* E-mail: *g275691@gmail.com or g275691@yandex.ru*
* Telegram: *+7(961) 914-60-97*
* GitHub: *g275691*

### About me:
 I'm a junior __Javascript developer__. I love javascript and a bit of python, and i love using them in my daily life: automate all the tedious processes in my browser and on my computer.

Now I am learning to write various useful skills for Yandex Alice. I use __ExpressJS__ and __Glitch__ for this. In the future, my Alice will invite users to play a detective story and give useful tips on healthy eating.

Last year I completed courses __Full-Stack JavaScript developer__, where I gained experience working with client and server sides. My graduation project was the creation of a car sharing service. Technology stack: __ReactJS+Redux__, and __NestJS__.

### Skills:
__Client-side__:
* HTML /SCSS/JS(ES6+)
* Webpack
* React + Redux
* Websockets

__Server-side__:
* NestJS or Express
* NextJS

### Code example:
I wrote a script for chrome extensions that monitors the work schedule of doctors on egisz.orb.ru, and it will notify me when the right doctor is free:

```

const bookingDoctor = async (year, month) => {
  const pageDoctor = `https://egisz.orb.ru/group/department_2966/service/949/resource/2867/planning/${year}/${month}?_salt=1638791338834`;
  const response = await fetch(pageDoctor);
  const json = await response.json();
  let freeDate = 0, nonfreeDate = 0;
  json.planning.map(day=>{
    if(!day.intervals) return;
    day.intervals.map(time=>{
      freeDate+=1;
      if(time.free) {
        console.log(`Free day: ${day.date}. time: ${time.formattedDate}`);
        window.open('https://www.youtube.com/watch?v=3f3n4DZvaIg');
      } else {
        nonfreeDate+=1;
      }
    })
    if(freeDate == nonfreeDate) {
      console.log("Busy day")
    }
  })
}

setInterval(() => {
    bookingDoctor(2022, 4)
    .catch(err=>console.log(err))
}, 1000);

```

### Courses:
![SkillFactory-diplom](https://raw.githubusercontent.com/g275691/rsschool-cv/gh-pages/img/skillfactory.jpg)

### Languages:
* Russian - native speaker.
* English - A2 (B1 in progress)