## DAY 3
1. A junior developer structure student name, skills and score in array of arrays which may not easy to read. Destruction the following array name to name, skills array to skills, scores array to scores, JavaScript score to jsScore and React score to reactScore variable.
   ```js
     const student = ['David', ['HTM', 'CSS', 'JS', 'React'], [98, 85, 90, 95]]
     console.log(name, skills, scores)
     console.log(jsScore, reactScore)
const student = ['David', ['HTM', 'CSS', 'JS', 'React'], [98, 85, 90, 95]]
const [
  name,
  [html, css, js, react],
  [htmlScore, cssScore, jsScore, reactScore]
] = student
console.log(
  name,
  html,
  css,
  js,
  react,
  htmlScore,
  cssScore,
  jsScore,
  reactScore
)
   ```
	Write a function called convertArrayToObject which can convert the array to a structured object.

	```js
			const students = [
					['David', ['HTM', 'CSS', 'JS', 'React'], [98, 85, 90, 95]],
					['John', ['HTM', 'CSS', 'JS', 'React'], [85, 80, 85, 80]]
				]

const convertArrayToObject = arr =>
  arr.map(([name, skills, scores]) => {
    return { name, skills, scores }
  })

console.log(convertArrayToObject(students))
			[
				{
					name: 'David',
					skills: ['HTM','CSS','JS','React'],
					scores: [98,85,90,95]
				},
				{
					name: 'John',
					skills: ['HTM','CSS','JS','React'],
					scores: [85, 80,85,80]
				}
			]
	```
	Copy the student object to newStudent without mutating the original object. In the new object add the following ?

	1. Add Bootstrap with level 8 to the front end skill sets
	2. Add Express with level 9 to the back end skill sets
	3. Add SQL with level 8 to the data base skill sets
	4. Add SQL without level to the data science skill sets

	```js
			const student = {
				name: 'David',
				age: 25,
				skills: {
					frontEnd: [
						{ skill: 'HTML', level: 10 },
						{ skill: 'CSS', level: 8 },
						{ skill: 'JS', level: 8 },
						{ skill: 'React', level: 9 }
					],
					backEnd: [
						{ skill: 'Node',level: 7 },
						{ skill: 'GraphQL', level: 8 },
					],
					dataBase:[
						{ skill: 'MongoDB', level: 7.5 },
					],
					dataScience:['Python', 'R', 'D3.js']
				}
			}

	```
		
	The copied object output should look like this:
		
	```js
			{
			name: 'David',
			age: 25,
			skills: {
				frontEnd: [
					{skill: 'HTML',level: 10},
					{skill: 'CSS',level: 8},
					{skill: 'JS',level: 8},
					{skill: 'React',level: 9},
					{skill: 'BootStrap',level: 8}
				],
				backEnd: [
					{skill: 'Node',level: 7},
					{skill: 'GraphQL',level: 8},
					{skill: 'Express',level: 9}
				],
				dataBase: [
					{ skill: 'MongoDB',level: 7.5},
					{ skill: 'SQL',level: 8}
				],
				dataScience: ['Python','R','D3.js','SQL']
			}
		}

	```
	Use the student object to solve the following questions:
   a. Find the length of student object keys
   b. Find the length of the student object values
   c. Find the length of skills object keys
   d. check if the student object has graphicDesign property
   e. Iterate the keys of the student object

   const studentObj = {
  name: 'David',
  age: 25,
  skills: {
    frontEnd: [
      { skill: 'HTML', level: 10 },
      { skill: 'CSS', level: 8 },
      { skill: 'JS', level: 8 },
      { skill: 'React', level: 9 }
    ],
    backEnd: [
      { skill: 'Node', level: 7 },
      { skill: 'GraphQL', level: 8 }
    ],
    dataBase: [{ skill: 'MongoDB', level: 7.5 }],
    dataScience: ['Python', 'R', 'D3.js']
  }
}
const devOps = [
  { skill: 'AWS', level: 7 },
  { skill: 'Jenkin', level: 7 },
  { skill: 'Git', level: 8 }
]
const copiedStudentObj = {
  ...studentObj,
  skills: {
    ...studentObj.skills,
    frontEnd: [...studentObj.skills.frontEnd, { skill: 'Bootstrap', level: 8 }],
    backEnd: [...studentObj.skills.backEnd, { skill: 'Express', level: 8 }],
    dataBase: [...studentObj.skills.dataBase, { skill: 'SQL', level: 8 }],
    dataScience: [...studentObj.skills.dataScience, 'SQL'],
    devOps: [...devOps]
  }
}
console.log(copiedStudentObj)

2.  Questions:a, b and c are based on the following two arrays:users and products
	```js
			const users = [
			{
					_id: 'ab12ex',
					username: 'Alex',
					email: 'alex@alex.com',
					password: '123123',
					createdAt:'17/05/2019 9:00 AM',
					isLoggedIn: false
			},
			{
					_id: 'fg12cy',
					username: 'Asab',
					email: 'asab@asab.com',
					password: '123456',
					createdAt:'17/05/2019 9:30 AM',
					isLoggedIn: true
			},
			{
					_id: 'zwf8md',
					username: 'Brook',
					email: 'brook@brook.com',
					password: '123111',
					createdAt:'17/05/2019 9:45 AM',
					isLoggedIn: true
			},
			{
					_id: 'eefamr',
					username: 'Martha',
					email: 'martha@martha.com',
					password: '123222',
					createdAt:'17/05/2019 9:50 AM',
					isLoggedIn: false
			},
			{
					_id: 'ghderc',
					username: 'Thomas',
					email: 'thomas@thomas.com',
					password: '123333',
					createdAt:'17/05/2019 10:00 AM',
					isLoggedIn: false
			}
			];

			const products = [
		{
			_id: 'eedfcf',
			name: 'mobile phone',
			description: 'Huawei Honor',
			price: 200,
			ratings: [
				{ userId: 'fg12cy', rate: 5 },
				{ userId: 'zwf8md', rate: 4.5 }
			],
			likes: []
		},
		{
			_id: 'aegfal',
			name: 'Laptop',
			description: 'MacPro: System Darwin',
			price: 2500,
			ratings: [],
			likes: ['fg12cy']
		},
		{
			_id: 'hedfcg',
			name: 'TV',
			description: 'Smart TV:Procaster',
			price: 400,
			ratings: [{ userId: 'fg12cy', rate: 5 }],
			likes: ['fg12cy']
		}
	];
	```
	
	a. Imagine you are getting the above users collection from a MongoDB database. 

		a. Create a function called ***signUp*** which allows user to add to the collection. If user exists, inform the user that he has already an account.
		b. Create a function called ***signIn*** which allows user to sign in to the application

        const randomId = () => {
  const numbersLetters = '0123456789abcdefghijklmnopqrstuvwzyzABCDEFGHIJKLMNOPQRSTUVWXYZ'.split(
    ''
  );
  let randId = '';
  let randIndex;
  for (let i = 0; i < 6; i++) {
    randIndex = Math.floor(Math.random() * numbersLetters.length);
    randId += numbersLetters[randIndex];
  }
  return randId;
};
const newUser = {
  _id: randomId(),
  username: 'Asabeneh',
  email: 'asabeneh@asabeneh.com',
  password: '123123123',
  createdAt: new Date(),
  isLoggedIn: false
};
const signUp = () => {
  const { email } = newUser;
  for (const user of users) {
    if (user['email'] == email) {
      return 'An email has already exist. Please log in!';
    }
  }
  users.push(newUser);
  return 'You have successfully signed up!';
};
console.log(users);
console.log(signUp(newUser));
console.log(signUp(newUser));
console.log(users);
const currentUser = {
  email: 'asabeneh@asabeneh.com',
  password: '123123123'
};
const signIn = user => {
  let found = false;
  const { email, password } = user;
  for (let i = 0; i < users.length; i++) {
    if (users[i]['email'] === email && users[i]['password'] === password) {
      users[i].isLoggedIn = true;
      return 'Successfully logged in';
    }
  }
  if (!found) {
    return 'Use does not exist';
  }
};
console.log(signIn(currentUser));
console.log(users);
console.log(signIn({ email: 'asab@asab.com', password: '123456' }));


	b. The products array has  three elements and each of them has six properties. 

		a. Create a function called ***rateProduct*** which rates the product
		b. Create a function called ***averageRating*** which calculate the average rating of a product

     //a
const rateProduct = (productId, userId, ratingPoint) => {
  let found = false;
  for (let i = 0; i < products.length; i++) {
    if (products[i]._id === productId) {
      for (let j = 0; j < products[i].ratings.length; j++) {
        if (products[i].ratings[j].userId === userId) {
          const rate = { userId, rate: ratingPoint };
          products[i].ratings[j].rate = ratingPoint;
          found = true;
          break;
        }
      }
      if (!found) {
        products[i].ratings.push({ userId, rate: ratingPoint });
      }
    }
  }
};
console.log(products);
rateProduct('eedfcf', 'fg12cy', 5);
rateProduct('aegfal', 'fg12cy', 2.5);
rateProduct('aegfal', 'fg12cy', 2.0);
console.log(products);
//b
const averageRating = productId => {
  let sum = 0;
  let len; // number of ratings
  for (let i = 0; i < products.length; i++) {
    if (products[i]._id === productId) {
      len = products[i].ratings.length;
      for (let j = 0; j < len; j++) {
        if (len === 0) {
          return 0;
        } else {
          sum += products[i].ratings[j].rate;
        }
      }
    }
  }
  console.log(len);
  return sum / len;
};
console.log(averageRating('eedfcf'));

		

	c. Create a function called ***likeProduct***. This function will helps to like to the product if it is not liked and remove like if it was liked.

	const likeProduct = (productId, userId) => {
  for (let i = 0; i < products.length; i++) {
    if (products[i]._id === productId) {
      const likes = products[i].likes;
      const index = products[i].likes.indexOf(userId);
      if (index !== -1) {
        products[i].likes.splice(index, 1);
      } else {
        products[i].likes.push(userId);
      }
    }
  }
};
console.log(likeProduct('aegfal', 'fg12cy'));
console.log(likeProduct('eedfcf', 'fg12cy'));
© 2021 GitHub, Inc.
