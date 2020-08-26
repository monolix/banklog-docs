# Endpoints


| **Method** | **Target**                      | **Description**                                                                 | **Notes** |
|-----------:|---------------------------------|---------------------------------------------------------------------------------|:---------:|
|        GET | `/users/{username}`             | Basic user's infos, like the list of the pages in common and if it's a vip user |           |
|        GET | `/users/me`                     | All the user's infos                                                            |    [^0]   |
|        GET | `/users/me/pages`               | The list of all the pages where the user has write permissions                  |    [^0]   |
|       POST | `/users/me/login`               | Login                                                                           |           |
|       POST | `/users/me/register`            | Register                                                                        |           |
|        PUT | `/users/me/{?}`                 | Edit some user's data                                                           |    [^0]   |
|     DELETE | `/users/me`                     | Delete user                                                                     |    [^0]   |
|        GET | `/pages/{id}`                   | Infos about the page                                                            |    [^1]   |
|        GET | `/pages/{id}/people`            | The list of people that have write permissions                                  |    [^1]   |
|       POST | `/pages/{id}/people/{id}`       | Add someone to the page                                                         |    [^3]   |
|       POST | `/pages/{id}/people/me`         | Add iteself to the page if the page is public                                   |    [^0]   |
|     DELETE | `/pages/{id}/people/{id}`       | Remove an user from the page                                                    |    [^3]   |
|     DELETE | `/pages/{id}/people/me`         | Remove itself from the page                                                     |    [^2]   |
|        GET | `/pages/{id}/transactions`      | The list of transactions, with queries for filters and limits                   |    [^1]   |
|       POST | `/pages/{id}/transactions`      | Add a transaction                                                               |    [^2]   |
|        PUT | `/pages/{id}/transactions/{id}` | Edit a transaction                                                              |    [^2]   |
|     DELETE | `/pages/{id}/transactions/{id}` | Delete the transaction                                                          |    [^2]   |
|     DELETE | `/pages/{id}`                   | Delete the page                                                                 |    [^3]   |


## Permissions
[^0]: Only if logged in
[^1]: Only if the page is public or you have write permissions
[^2]: Only if you have write permissions
[^3]: Only if you're an admin
