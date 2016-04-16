# Datastructure

- UserManagment System
  - User
  - Application
  - Group
  - UserGroupRelation
- History


## UserManagment System

### User
| Field           | Unique | Description                              |
|----------------:|:------:|:-----------------------------------------|
| userID          |   PK   | Identifier of User                       |
| username        |   X    | Unique username                          |
| mail            |   X    | Unique E-Mail address                    |
| password        |   -    | This field contains the hashed password  |
| profilePicture  |   -    | Foreign Key to ProfilePicture            |
| firstname       |   -    |                                          |
| lastname        |   -    |                                          |
| language        |   -    | Language Key                             |
| createdAt       |   -    | DateTime of the creation                 |
| updatedAt       |   -    | DateTime of the last update              |
| updatedBy       |   -    | Foreign Key to User                      |

### Application
| Field             | Unique | Description               
|------------------:|:------:|:---------------------------|
| applicationID     |   PK   | identifier of application  |
| name              |   X    | unique name of the trainer |
| descriptionShort  |   -    | foreign key to dictionary  |
| descriptionLong   |   -    | foreign key to dictionary  |
| URL               |   X    |
| releaseDate       |   -    |
| logo              |   -    |
| version           |   -    | version of the application
| createdAt         |   -    |
| createdBy         |   -    |
| updatedAt         |   -    |
| updatedBy         |   -    |

### Group
| Field           | Unique |
|----------------:|:------:|
| groupID
| name


### UserGroupRelation
| Field           | Unique |
|----------------:|:------:|
| userID          |   PK   |
| groupID         |   PK   |
| createdAt       |   -    |
| createdBy       |   -    |
| updatedAt       |   -    |
| updatedBy       |   -    |






## History

| Version |    Date    |      Name     |               Description             |
|--------:|:-----------|--------------:|:--------------------------------------|
| v0.1    | 04.14.2016 | Fabio Mazzone | Created Document                      |
