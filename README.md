props-tracker

# ideas

###### May 7th, 1:09 AM

So I want a few things with this app, and I think if I structure it well it'll be easy to achieve.

	- Some visual representation of the stage to be the main canvas of the app.
		- Now we have two options for this. Either (A) I, the developer, custom makes a
		new canvas for every show/theater that uses the app, OR, (B) we have some sort of
		"stage editor".
		- It would have to be super barebones, like drawing/erasing lines on a grid, with
		multiple layers perhaps for different stories.
		- It's complex, but honestly I like the complexity and functionality that a stage
		editor adds. It would enable you to be able to easily customize changes in the set
		for different acts or scenes, and it would take the middle man out of the app, which
		is what we would want, ideally.
		
	- An overall **object** class, but with a better name than **object**. What I really mean
	is some sort of encapsulation for an actor, a prop, a setpiece, a *whatever* that needed to
	be tracked over time, with metadata such as name, color, position, and time.
	
		- So within that right you'd need a few subclasses, namely:
		
		- Actor with:
			- Position
			- Name
			- Picture
			- Role
			- Prop/Setpiece
			
		- Prop with:
			- Position
			- Name
			- Carrier
		
		- **Importantly**, each of these would need to be arbitrarily expandable vectors with all this information,
		so that it could vary with arbitrary timesteps.
			
	- A way to catergorize each object in useful ways. Some that stand out are:
		
		- See all the props that have no actor assigned to them (basically props that aren't assigned to a mover)
		
		- See all actors with no tasks at that time-step (task being a prop or setpiece)
		
		- And any combinations of these things
		
	- An easy way to see the total movement of a prop or actor or setpiece throughout the course of the show.
	