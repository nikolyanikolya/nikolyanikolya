### Hi there! I am Nikolay Ignatov 
- 👨🏻‍🎓 CT ITMO Bachelor of science in applied mathematics and computer science  
- 👨‍💻 Full-stack developer at Lipt Soft  
- 📄 My CV: [CV](https://github.com/nikolyanikolya/CV/blob/main/CV_SE.pdf)   

[![Telegram Nikolay](https://img.shields.io/badge/telegram-blue)](https://t.me/nikolya_7) [![Email Nikolay](https://img.shields.io/badge/email-green?label=nickigna610@gmail.com)](mailto:nickigna610@gmail.com)
```kotlin
import TechnologyKind.*

object Me: Employee, Bachelor {

    override fun currentWorkPlace(): String = "Lipt Soft"

    override fun position(): String = "Full-stack developer"

    override fun experience(): String = "2 years"

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

    override fun specialization(): String = "Applied mathematics and computer science"

    override fun university(): String = "ITMO"
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

sealed interface Employee {
    fun currentWorkPlace(): String
    fun position(): String
    fun `technologies & tools`(): Map<TechnologyKind, List<String>>
    fun experience(): String
}

sealed interface Bachelor {
    fun specialization(): String
    fun university(): String
}
```


