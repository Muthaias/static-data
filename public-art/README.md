# The REST-API description
The data structures will be described using a Typescript type description. The data itself should conform to standard JSON but Typescript is a very strong language for describing the structure.

## Entries endpoint (`entries.json`)
The endpoint is accessed via a `GET` call to `ROOT_URL/entries.json`. A standard JSON file is returned. The format description is as follows:
```
{
    artwork: string,
    installation: string,
    creator: string,
    yearOfDeath: number,
    lat: number,
    long: number,
    description: string,
    groupId: string
}[]
```
The property `groupId` is a reference to the property `id` in a group in `groups.json`

## Groups endpoint (`groups.json`)
The endpoint is accessed via a `GET` call to `ROOT_URL/groups.json`. A standard JSON file is returned. The format description is as follows:
```
{
    name: string,
    position: {
        lat: number,
        long: number
    },
    id: string
}[]
```
The system expects the values of the property `id` to unique within the list of groups.