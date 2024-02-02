This project is implmented inside a development container in order to use the project you will need to install:
* [Visual Studio Code](https://code.visualstudio.com/download)
* [Docker](https://docs.docker.com/engine/install/)
* [Visual Studio Code Dev Containers Extension](https://code.visualstudio.com/docs/devcontainers/containers)

We adhere to git best practice by utilizing branches and pull-requests. You will be unable to push changes directly to the `main` branch. Instead you must create a branch with a relevent name like `feature/123-description` push that branch up to github and submit a [Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)


Work is tracked via a [this kanban board](https://github.com/users/jeff-cannapress/projects/2/views/1)

## Dramatis Personae
_If all the world’s a stage these are our players_
* **Bailey** A basic application user. Bailey has not gone through the process of registering and only has access to free / offline app features.
* **Rachael** a Registered app user. Rachael has access to all Bailey’s features plus online features like coaching from Travis
* **Prima** A premium user. Prima has all Rachael’s features plus any feature that writes to /our/ storage.
* **Chad** A personal trainer / Coach. Chad has access to all Prima’s features, plus coaching specific features

## Conceptual model
#### Common Properties
All entities in the system can have the following properties
* `id`: string
* `name`: string
* `notes`: string
* `links`: {title:string, url:string}[]
* `tags`: string[]

#### Core entities
* A `Movement` is the abstract idea of an exercise: What equipment is used, How the movement is supposed to be done,  and how that movement is measured.
* An `Plan` is a group of Routines
* A `Routine` is a Collection of Exercises 
* An `Exercise` is a collection of Sets + rest time
* A `Set` is a repeated series of a movement including relevant methodology metrics (eg weight and reps)
* A `Workout` is the record of when a routine is executed including the date and...

