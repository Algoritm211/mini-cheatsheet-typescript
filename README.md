# mini-cheatsheet-typescript

```javascript

let name: string = 'Lesha'
let num: number = 19
let isSamurai: boolean | null = true
isSamurai = null

let sex: 'male' | 'female'
sex = 'male'


let names: Array<string> = ['Alex', 'Edward', 'Tim']

// Objects
// ? - not necessarily for property

type AddressType = {
  city: string | null,
  country: string | null,
}

type CarType = {
  mark: string | null,
  model: string | null,
}

// Returns nothing - void
type UserType = {
  sayHello?: (message: string) => void,
  name: string,
  isProgrammer: boolean,
  address: AddressType | null
}

let user: UserType = {
  name: 'Alex',
  isProgrammer: true,
  address: {
    country: 'UK',
    city: 'London'
  }
}


let initialState = {
  name: null as string | null,
  age: null as number | null,
  isProgrammer: null as boolean | null,
  address: {
    country: null,
    city: null,
  } as AddressType,
  cars: [] as Array<CarType>
}

export type InitialStateType = typeof initialState

const state: InitialStateType = {
  name: 'Alex',
  age: 19,
  isProgrammer: true,
  address: {
    country: 'Ukraine',
    city: 'Kiev'
  },
  cars: [{mark: 'Rolls-Royce', model: 'Wraith'}]
}


// Functions

const summ = (num1: number, num2: number) => {
  return num1 + num2
}

summ(19, 19)

// for actions in Redux

let GET_TASKS = 'app/GET_TASKS'

type GetTasksActionType = {
  id: number,
  type: typeof GET_TASKS
}

let action: GetTasksActionType = {
  type: GET_TASKS,
  id: 19
}

```

