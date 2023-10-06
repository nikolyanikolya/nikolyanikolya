### Hi there 👋
[![Telegram Nikolay](https://img.shields.io/badge/telegram-blue)](https://t.me/nikolya_7) [![Email Nikolay](https://img.shields.io/badge/email-green?label=nickigna610@gmail.com)](mailto:nickigna610@gmail.com)
```kotlin
import CourseKind.*
import TechnologyKind.*

object Me: Employee, Student {
    override fun currentWorkPlace(): String = "Lipt Soft"

    override fun position(): String = "Full-stack developer"

    override fun experience(): String = "1.25 years"

    override fun `technologies & tools`(): Map<TechnologyKind, List<String>> = mapOf(
        LANGUAGE to listOf("Kotlin/Java", "HTML", "CSS", "Javascript"),
        TESTING to listOf("Mockito", "JUnit5", "Selenide", "Jasmine", "SonarQube"),
        DATABASE to listOf("Oracle", "H2", "PostgreSQL"),
        FRAMEWORK to listOf("Spring", "Hibernate", "Play", "Koin", "Ktor", "Spark", "Slf4j"),
        DEPLOY to listOf("Docker", "Portainer"),
        CI to listOf("Jenkins"),
        METHODOLOGY to listOf("Agile", "Jira", "Pivotal"),
        COMMUNICATION to listOf("English B2", "Russian native"),
        SOFT_SKILLS to listOf("communicative", "responsible"),
        OTHER to listOf("Kafka", "Git", "Bash")
    )

    override fun currentUniversity(): String = "ITMO university"

    override fun year(): Int = 4

    override fun relevantCourses() = mapOf(
        PROGRAMMING to listOf(
            "C++ advanced", "Rust", "Git", "Algorithms and Data Structures",
            "Unix", "Computer Architecture and Operating Systems",
            "Functional Programming (Haskell)", "Bioinformatics",
            "Translation methods", "Python", "Java advanced", "Databases",
            "Networks", "Machine learning",
        ),
        MATH to listOf(
            "Calculus", "Analysis", "Linear Algebra",
            "Group Theory", "Graph Theory", "Combinatorics",
            "Mathematical Logic", "Coding theory"
        ))
}

enum class TechnologyKind {
    TESTING,
    LANGUAGE,
    DATABASE,
    FRAMEWORK,
    METHODOLOGY,
    DEPLOY,
    CI,
    SOFT_SKILLS,
    COMMUNICATION,
    OTHER
}

enum class CourseKind {
    MATH,
    PROGRAMMING
}

sealed interface Employee {
    fun currentWorkPlace(): String
    fun position(): String
    fun `technologies & tools`(): Map<TechnologyKind, List<String>>
    fun experience(): String
}

sealed interface Student {
    fun currentUniversity(): String
    fun year(): Int
    fun relevantCourses(): Map<CourseKind, List<String>>
}
```


