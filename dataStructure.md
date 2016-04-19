# Datastructure

- UserManagment System
  - User
  - Module
  - Group
  - UserGroupRelation
- History


## UserManagment System

### User
This entity represents a user.

| Field           | Unique | Description                              |
|----------------:|:------:|:-----------------------------------------|
| userID          |   PK   | Identifier of User                       |
| username        |   X    | Unique username                          |
| mail            |   X    | Unique E-Mail address                    |
| password        |   -    | This field contains the hashed password  |
| profilePicture  |   -    | Foreign Key to ProfilePicture            |
| disabledAt      |        | DateTime when the user was disabledAt    |
| createdAt       |   -    | DateTime of the creation                 |
| updatedAt       |   -    | DateTime of the last update              |
| updatedBy       |   -    | Foreign Key to User                      |

### Module
| Field             | Unique  | Description                                   |
|------------------:|:-------:|:----------------------------------------------|
| moduleID          |   PK    | identifier of module                          |
| name              |   X     | unique name of the trainer                    |
| URL               |   X     |                                               |
| releaseDate       |   -     |                                               |
| isAvailable       |   -     | a boolean flag if is the module is available  |
| inTestingPeriod   |   -     | a boolean flag if is it in an testing period  |
| logo              |   -     | Path to Logo                                  |
| version           |   -     | version of the module                         |
| createdAt         |   -     | DateTime of creation                          |
| createdBy         |   -     | Foreign Key to User                           |
| updatedAt         |   -     | DateTime of last update                       |
| updatedBy         |   -     | Foreign Key to User                           |

### ModuleUserAccess
This entity regulate the access to the modules from the users.
So selected users can test and try out some modules which are not ready to be available to public access.

| Field             | Unique  | Description |
|------------------:|:-------:|:------------|
| userID            |   PK    |
| moduleID          |   PK    |

### Activity
| Field             | Unique  | Description |
|------------------:|:-------:|:------------|
|

### Group
| Field           | Unique  | Description           |
|----------------:|:-------:|:----------------------|
| groupID         |   PK    | identifier of group   |
| name            |   -     | the name of the group |
| leader          |   -     | Foreign Key to User   |
| createdAt       |   -     | DateTime of creation  |
| createdBy       |   -     | Foreign Key to User   |
| updatedAt       |   -     | DateTime of creation  |
| updatedBy       |   -     | Foreign Key to User   |



### UserGroupRelation
| Field           | Unique |
|----------------:|:------:|
| userID          |   PK   |
| groupID         |   PK   |
| createdAt       |   -    |
| createdBy       |   -    |
| updatedAt       |   -    |
| updatedBy       |   -    |

### Permissions
| Field           | Unique  | Description     |
|----------------:|:-------:|:----------------|
|


### Profile Pictures
| Field             | Unique  | Description                     |
|------------------:|:-------:|:--------------------------------|
| profilePictureID  |   PK    | identifier of profile picture   |
| name              |   -     | the name of the profile picture |
| url               |   -     | the path to the profile picture |
| cssAttributes     |   -     | additional css attributes       |
| createdAt         |   -     | DateTime of creation            |
| createdBy         |   -     | Foreign Key to User             |
| updatedAt         |   -     | DateTie of last update          |
| updatedBy         |   -     | Foreign Key to User             |

### Settings



## Changelog

| Version |    Date    |      Name     |               Description             |
|--------:|:-----------|--------------:|:--------------------------------------|
| v0.1    | 04.14.2016 | Fabio Mazzone | Created Document                      |
