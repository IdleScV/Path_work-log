<!-- !Timeline Data -->
let timeline_data = {
	title: 'Life of Nikola Tesla',
	user: <!--? INSTANCE -->,
	person: <!--? INSTANCE -->,
    <!--* BELONGS TO: USER, PERSON -->
	events: [ 
        <!--? INSTANCE -->, 
        <!--? INSTANCE -->,
        <!--? INSTANCE -->,
        ]
    <!--* HAS MANY: EVENTS -->
	created_at: '2020-04-22 13:36:22.459149334 +0000',
	updated_at: '2020-04-22 13:36:22.459149334 +0000'
};

<!-- ! User Data -->
let user1 = {
	username: 'IdleScV',
	firebase_id: '123456123456'
};

<!-- ! Person Data -->
let nikola_tesla = {
	name: 'Nikola Tesla',
	birthday: '10/7/1856',
	deathday: '7/1/1943',
	initial_state: { 
        location: <!--? INSTANCE -->, aka city
        <!--* RELATION: CITY -->
        age: 0 }
};

<!--  ! Event Data  -->
let event_data1 = {
	user: <!--? INSTANCE -->,
	reference: {
		type: 'Person', "Country", "City", "World"
		instance: <!--? INSTANCE -->, null if type=="World"
	},
	snippet: 'Move to the United States',
	details:
		"In June 1884, Tesla emigrated to the United States. He began working almost immediately at the Machine Works on Manhattan's Lower East Side, an overcrowded shop with a workforce of several hundred machinists, laborers, managing staff, and 20 'field engineers' struggling with the task of building the large electric utility in that city. As in Paris, Tesla was working on troubleshooting installations and improving generators. Historian W. Bernard Carlson notes Tesla may have met company founder Thomas Edison only a couple of times.",
	date: '0/07/1884',
	location: <!--? INSTANCE -->,
    <!--* BELONGS TO: CITY OR COUNTRY -->
	types: [ 'Major', 'Personal' ],
	link: {
		url: 'https://en.wikipedia.org/wiki/Nikola_Tesla#Move_to_the_United_States'
	},
	image: {
		url:
			'https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/Edison_machine_works_goerck_street_new_york_1881.png/220px-Edison_machine_works_goerck_street_new_york_1881.png',
		text: 'Edison Machine Works on Goerck Street, New York.'
	}
};

<!-- ! Country Data  -->
let united_states = {
	name: 'United States'
};

<!--  ! City Data -->
smijan = {
	country: <!--? INSTANCE -->,
    <!--* BELONGS TO: City>
	state: null( or ""),
	name: 'Smijan'
};