# Zhanbolat Mukan
### Junior Frontend Developer
---
### Contact information:

* Location: Kazakhstan, Almaty
* Phone: 8 (707) 649 21 97 
* E-mail: zhanbolat.mukan2004@gmail.com
* Telegram: @ZhSherl
* [LinkedIn](https://www.linkedin.com/in/zhanbolat-mukan-44177826a/ "Link to LinkedIn")

---
### Briefly About  Myself
I am an ambitious guy from Almaty with big plans for my future. A second-year student at Suleyman Demirel University. Specialty - Information Systems.

At the university, I coded in java and wrote projects such as Kahoot, online market of my uni. Being interested in game development, I got carried away with a blender and modeled an awesome axe. Later I got hooked on frontend. I studied html css js during the summer holidays, got carried away with layout and sold a dozen adaptive layouts to other students :)

Realizing that I like the frontend and that I can earn good money in this direction, I began to study this area in depth. Signed up for the rsschool course. I plan to get a job this year, so just learn and develop!

---

### Hard Skills:

* HTML5, CSS3
* Figma
* JS(ES6), JQuery, ReactJS(Basics)
* Java, JavaFX
* SQL, SQlite, PostgreSQL, MongoDB
* Git, Github
* VS Code, IntelliJ IDEA
* Adobe Photoshop, Blender

---

### Soft Skills:

* Ease of communication
* Team worker
* Able to lead
* Responsible

---

### Code example:

*Where Will the Ball Fall* - Leetcode

You have a 2-D grid of size m x n representing a box, and you have n balls. The box is open on the top and bottom sides.

Each cell in the box has a diagonal board spanning two corners of the cell that can redirect a ball to the right or to the left.

A board that redirects the ball to the right spans the top-left corner to the bottom-right corner and is represented in the grid as 1.
A board that redirects the ball to the left spans the top-right corner to the bottom-left corner and is represented in the grid as -1.
We drop one ball at the top of each column of the box. Each ball can get stuck in the box or fall out of the bottom. A ball gets stuck if it hits a "V" shaped pattern between two boards or if a board redirects the ball into either wall of the box.

Return an array answer of size n where answer[i] is the column that the ball falls out of at the bottom after dropping the ball from the ith column at the top, or -1 if the ball gets stuck in the box.

```

var findBall = function(grid) 
{
    const rows = grid.length;
    const cols = grid[0].length;

    const getPosition = function(row, col)
    {
        if(grid[row][col] === 1)
        {
            if(col === cols-1 || grid[row][col+1] === -1) //V
                return -1;
            return col+1; //мяч переходит в след колонну
        }
        else
        {
            if(col === 0 || grid[row][col-1] === 1) //если индекс колонны 0, значит тупик |/ = -1
                return -1;
            return col-1; //значит ячейка -1 и мяч возвращается на левую конооннну
        }
    };

    let result = [];
    for(let col=0; col<cols; col++)
    {
        let pos = col;
        for(let row=0; row<rows; row++)
        {
            pos = getPosition(row, pos);
            if(pos === -1)  //застрял
                break; 
        }
        result.push(pos);
    }
    
    return result;
};

```

---

### Experience

---

### Education:
* 2021-2025 Suleyman Demirel University, Informational Systems bachelor
* Courses
  * nFactorial Incubator summer bootcamp (WEBDEV)
  * HTML and CSS course on FreeCodeCamp(completed)
  * JS course on FreeCodeCamp(in progress 80%)


---

### Languages:

* English - Intermediate/ Upper-intermediate (according to the university)
* Russian - C2
* Kazakh - Native
* Turkish - A2
