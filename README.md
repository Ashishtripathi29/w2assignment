# w2assignment

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>

</body>
<script>
    const facebookProfiles = [
        {
            firstName: "Akash",
            lastName: "Agarwal",
            number: "111111111",
            likes: ["music", "movies"],
            hasDrivingLicense: false,
            address: {
                location: "rampur",
                state: "up",
            },
            emails: ["abc@outlook.com", "efg@gamil.com", "ghj@gmail.com"],
        },
        {
            firstName: "Pritesh",
            lastName: "Kumar",
            number: "222222222",
            likes: ["code", "driving"],
            hasDrivingLicense: false,
            address: {
                location: "gurgaon",
                state: "haryana",
            },
            emails: ["fgdfg@gmail.com"],
        },
        {
            firstName: "Sabiha",
            lastName: "Khan",
            number: "333333333",
            hasDrivingLicense: false,
            address: {
                location: "lucknow",
                state: "up",
            },
        },
        {
            firstName: "Suyash",
            lastName: "Kashyap",
            number: "444444444",
            likes: ["travel", "driving"],
            hasDrivingLicense: true,
            address: {
                location: "alwar",
                state: "rajasthan",
            },
            emails: ["abc@yahoo.com"],
        },
        {
            firstName: "Jay",
            likes: ["food", "mobile"],
            hasDrivingLicense: true,
            address: {
                location: "gurgaon",
                state: "haryana",
            },
            emails: ["abc@gmail.com", "efg@yahoo.com", "ghj@outlook.com"],
        },
    ];

   // IMPORTANT: SOLVE the following questions using two methods
   // 1. use for loop 
   for (let index = 0; index < facebookProfiles.length; index++) {
    const element = facebookProfiles[index];
    console.log(element)
    
   }
   // 2. USE HIGHER ORDER FUNCTIONS TO SOLVE THE ABOVE QUESTIONS(map, filter, find, forEach etc. )
   const map1=facebookProfiles.map(x=>x)
   console.log(map1)
   const filter1=facebookProfiles.filter(x=>x)
   console.log(filter1)

   facebookProfiles.forEach(element => {
    console.log(element)
  
   });
   const faceid=facebookProfiles.find(element=>element==facebookProfiles[1])
   console.log(faceid)
 


    // ==================================== 0 ==================================== //

    function profileLookup(name, property) {
        //write your code here
        if (name == undefined || typeof (name) !== "string") {
            return console.log("please pass the name")
        }
        if (property == undefined || typeof (property) !== "string") {
            return console.log("please pass the property")

        }
        console.log("Name : ", name)
        console.log("property : ", property)
    }
    profileLookup("Ashish", "teacher")

    // complete the above function such that when it is called with name and property, then it should return its value
    // ex
    // profileLookup("Pritesh", "number"), then it should return his number

    // handle edge cases like:
    //      if name is not in the list, return "person does not exist"
    //      if property is not present then return "no such property"
    // 
    // Hint: dynamically access properties using square bracket

    // ================================== 1 ====================================== //

    function getNamesFromGurgaon(facebookProfiles) {
        //write your code here
        const Profiles = [
            {
                firstName: "Akash",
                lastName: "Agarwal",
                number: "111111111",
                likes: ["music", "movies"],
                hasDrivingLicense: false,
                address: {
                    location: "rampur",
                    state: "up",
                },
                emails: ["abc@outlook.com", "efg@gamil.com", "ghj@gmail.com"],
            },
            {
                firstName: "Pritesh",
                lastName: "Kumar",
                number: "222222222",
                likes: ["code", "driving"],
                hasDrivingLicense: false,
                address: {
                    location: "gurgaon",
                    state: "haryana",
                },
                emails: ["fgdfg@gmail.com"],
            },
            {
                firstName: "Sabiha",
                lastName: "Khan",
                number: "333333333",
                hasDrivingLicense: false,
                address: {
                    location: "lucknow",
                    state: "up",
                },
            },
            {
                firstName: "Suyash",
                lastName: "Kashyap",
                number: "444444444",
                likes: ["travel", "driving"],
                hasDrivingLicense: true,
                address: {
                    location: "alwar",
                    state: "rajasthan",
                },
                emails: ["abc@yahoo.com"],
            },
            {
                firstName: "Jay",
                likes: ["food", "mobile"],
                hasDrivingLicense: true,
                address: {
                    location: "gurgaon",
                    state: "haryana",
                },
                emails: ["abc@gmail.com", "efg@yahoo.com", "ghj@outlook.com"],
            },
        ];
        return Profiles

    }
    console.log(getNamesFromGurgaon())
    //complete the above functin such that it returns the list of full names of all people of gurgaon.
    // ex = ['Jay ', 'Pritesh Kumar']

    // ==================================2 ====================================== //

    function findFullName(stateName) {
        //write your code here
        const state={
            "up": {
                state: "utter pradesh",
                residence_name: "Ashish Tripathi",
                position: "Student in programmin",
                age: "20year"
            },
            "mp":{
                state: "madhya pradesh",
                residence_name: "Ragani Tripathi",
                position: "Student in programmin",
                age: "20year"
            },
            "uk": {
                state: "uttrakhand",
                residence_name: "prince",
                position: "teacher in programmin",
                age: "25year"
            },
            "delhi":{
                state: "Delhi",
                residence_name: "kejariwal",
                position: "cheif minister of delhi",
                age: "40year"
            },
            "bihar": {
                state: "bihar",
                residence_name: "lalu yadav",
                position: "cheif ministre of bihar",
                age: "65 year"
            },
            "gujarat":{
                state: "Gujrat",
                residence_name: "jethalal",
                position: "Actor",
                age: "60 year"
            }
            
        }
     
        return state[stateName]
    }
    let state=findFullName("mp")
    console.log(state)
        
    


    // 2. complete this function, which takes state name as argument and return the name 
    // of one of its residents

    // ================================== 3 ====================================== //

    function getDLStatus(userName) {
        //write your code here
        const  name={
            "jay":{
                firstName:"Jay",
                lastName:"prakash",
                hasDrivingLicense:"Yes",
                age:"22"
            },
            "ashish":{
                firstName:"Ashish",
                lastName:"Tripathi",
                hasDrivingLicense:"Yes"
                
            },
            "pratik":{
                firstName:"Pratik",
                lastName:"Tripathi",
                hasDrivingLicense:"no"
            },
            "Umesh":{
                firstName:"Umesh",
                lastName:"Tiwari",
                hasDrivingLicense:"no"
            },
            "shivam":{
                firstName:"Shivam",
                lastName:"Tripathi",
                hasDrivingLicense:"Yes"
            },
            "prashant":{
                firstName:"prashant",
                lastName:"Tripathi",
                hasDrivingLicense:"no"
            },
            "ankit":{
                firstName:"Ankit",
                lastName:"Tripathi",
                hasDrivingLicense:"no"
            }
        }
     
        return name[userName]
    }
    let Dl=getDLStatus("jay")
    console.log(Dl)
    //3. write a function which returns full names of all people of gurgaon with their driving license status, in an array. 
    // like shown in the example below
    // ex = ['Jay - D/L', 'Pritesh Kumar - N D/L']

    // =================================== 4 ===================================== //

    function getFullName() {
        //write your code here
        const name=['Ankit Tripathi','Prabhat Tripathi','Ashish Tripati','Shivam Tripathi','Prashant Tripathi','Pratik Tripathi' ]
return name
    }
    const arrname=getFullName()
    console.log(arrname)

    // 4. write a function which returns full names in an array
    //ans = ['Akash Agarwal', 'Pritesh Kumar', 'Sabiha Khan', 'Suyash Kashyap', 'Jay' ]


    // ===================================== 5 =================================== //

    function getLikes(name) {
        //write your code here
        const likes={
            "ashish":{
                music:5,
                movies:4,
                code:5,
                podcasts:3,
                travel:4,
                driving:4,
                food:4,
                mobile:5
            },
            "mybindu":{
                music:5,
                movies:3,
                code:5,
                podcasts:4,
                travel:5,
                driving:2,
                food:4,
                mobile:4
            },
            "myab":{
                music:5,
                movies:4,
                code:5,
                podcasts:3,
                travel:4,
                driving:4,
                food:4,
                mobile:5
            },
            "bindu":{
                music:5,
                movies:4,
                code:5,
                podcasts:3,
                travel:4,
                driving:4,
                food:4,
                mobile:5
            },
            "ab":{
                music:5,
                movies:4,
                code:5,
                podcasts:3,
                travel:4,
                driving:4,
                food:4,
                mobile:5
            },
        }
        return likes[name]
    }

    const numberOfLikes=getLikes("mybindu")
    console.log(numberOfLikes)



    // 5. write a function which returns all likes of all the people in an array
    //hint: use spread syntax
    //ans = ['music', 'movies', 'code', 'podcasts', 'travel', 'driving', 'food', 'mobile']

    // ====================================== 6 ================================== //

    function getNameFromDelhiWithDL(personName) {
        //write your code here
        const Dl={
            "ashish":{name:"Ashish Tripathi",
                        hasDrivingLicense:'yes'    
        },
        "bindu":{
            name:"Bindu",
            hasDrivingLicense:"no"
        },
        "jay":{
            name:"jay",
            hasDrivingLicense:"yes"
        }
        }

        if(Dl[personName].hasDrivingLicense=="yes"){
            return personName+" has driving licence"
        }   
        
        else{
            return "no such person"
        }
        }
        const dlWithDelhi=getNameFromDelhiWithDL("jay")
        console.log(dlWithDelhi)
    

    //6. write a function which return  the name of the any one person who live in delhi and has driving license
    //ans => "no such person"

    // ======================================= 7 ================================= //

    function getNameOfDriverWithoutDL(personName2) {
        //write your code here
        const Dl={
            "ashish":{name:"Ashish Tripathi",
                        hasDrivingLicense:'yes'    
        },
        "bindu":{
            name:"Bindu",
            hasDrivingLicense:"no"
        },
        "jay":{
            name:"jay",
            hasDrivingLicense:"yes"
        }
        }

        if(Dl[personName2].hasDrivingLicense=="no"){
            return personName2+" has not driving licence"
        }   
        
        else{
            return "no such person"
        }
        }
        const dlWithoutDelhl=getNameOfDriverWithoutDL("bindu")
        console.log(dlWithoutDelhl)
    
    
//7. write a function which return the name of the any one person who like driving but doesnt have driving license
//asn => pritesh



</script>

</html>
