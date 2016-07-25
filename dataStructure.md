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

| Field                 | Unique | Description                              |
|----------------------:|:------:|:-----------------------------------------|
| userID                |   PK   | Identifier of User                       |
| username              |   X    | Unique username                          |
| yNo                   |   X    | Unique username                          |
| mail                  |   X    | Unique E-Mail address                    |
| password              |   -    | This field contains the hashed password  |
| profilePicture        |   -    | Foreign Key to ProfilePicture            |
| profilePictureBorder  |   -    | Foreign Key to ProfilePictureBorder      |
| disabledAt            |   -    | DateTime when the user was disabledAt    |
| createdAt             |   -    | DateTime of the creation                 |
| updatedAt             |   -    | DateTime of the last update              |
| updatedBy             |   -    | Foreign Key to User                      |

### Module
| Field             | Unique  | Description                                   |
|------------------:|:-------:|:----------------------------------------------|
| moduleID          |   PK    | identifier of module                          |
| name              |   X     | unique name of the trainer                    |
| Description       |   -     |                                               |
| URL               |   X     |                                               |
| releaseDate       |   -     |                                               |
| isAvailable       |   -     | a boolean flag if is the module is available  |
| inTesting         |   -     | a boolean flag if is it in an testing period  |
| logo              |   -     | Path to Logo                                  |
| version           |   -     | version of the module                         |
| createdAt         |   -     | DateTime of creation                          |
| createdBy         |   -     | Foreign Key to User                           |
| updatedAt         |   -     | DateTime of last update                       |
| updatedBy         |   -     | Foreign Key to User                           |


### Achievements
| Field             | Unique  | Description                                   |
|------------------:|:-------:|:----------------------------------------------|
| achievementID       |   PK    | identifier of achievements                  |
| name                |   X     |                                             |
| description         |   -     |                     |
| logo                |   -     |                     |
| points              |   -     |                     |
| module              |   -     |                     |
| AchievementCategory |   -     |                     |
| start               |   -     |                     |
| stop                |   -     |                     |
| inTest              |   -     |                     |

### Rewards
| Field             | Unique  | Description                                   |
|------------------:|:-------:|:----------------------------------------------|
| achievementID     |   FK    |                   |
| rewardID          |   PK    |                   |
| name              |   X     |                                             |
| description       |   -     |                     |
| logo              |   -     |                     |
| rewardCategory    |   -     |                     |

### UserAchievements
### UserRewards
### Role
###
### Session

### Group
| Field           | Unique  | Description           |
|----------------:|:-------:|:----------------------|
| groupID         |   PK    | identifier of group   |
| name            |   -     | the name of the group |
| leader          |   -     | Foreign Key to User   |
| createdAt       |   -     | DateTime of creation  |
| createdBy       |   -     | Foreign Key to User   |
| updatedAt       |   -     | DateTime of update    |
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

### Profile Picture Borders
| Field             | Unique  | Description                     |
|------------------:|:-------:|:--------------------------------|
| pictureBorderID   |   PK    | identifier                      |
| name              |   -     | the name                        |
| url               |   -     | the path                        |
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
