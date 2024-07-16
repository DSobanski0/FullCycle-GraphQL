# FullCycle-GraphQL

### Startar aplicação
go run cmd/server/server.go

### Exemplo de Queries
mutation createCategory {
  createCategory(input: {name: "Tecnologia", description: "Cursos de Tecnologia"}) {
    id
    name
    description
  }
}

mutation createCourse {
  createCourse(input: {name: "Full Cycle", description: "The best!", category: "f2730096-2cdd-4786-8d44-bde183792e20"}) {
    id
    name
    description
  }
}

query queryCategories {
  categories{
    id
    name
    description
  }
}

query queryCategoriesWithCourses {
  categories{
    id
    name
    description
    courses {
      id
      name
      description
    }
  }
}

query queryCourses {
  courses{
    id
    name
    description
  }
}

query queryCoursesWithCategory {
  courses{
    id
    name
    category {
      name
      description
    }
  }
}