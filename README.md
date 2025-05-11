## Compile check? 
```rust
struct PersonalInfo<'a> {
    name: &'a str,
    description: &'a str,
    mail: &'a str,
    interests: Vec<&'a str>,
    skillset: Vec<Skills>
}
type Skills = (&'static str, Vec<&'static str>);

impl PersonalInfo<'_> {
    pub fn new() -> Self {
        PersonalInfo {
            name: "Philip Cramer",
            description: "I am a software engineering student at DTU",
            mail: "s224319@dtu.dk",
            interests: vec!["Linux", "Programming", "Cyber Security", "System Engineering"],
            skillset: PersonalInfo::my_skills()
        }
    } 
    fn my_skills() -> Vec<Skills> {
        vec![
            ("Advanced", vec!["Linux", "Rust"]),
            ("Intermediate", vec!["C", "Bash", "Java", "Kotlin", "Docker", "Git"]),
            ("Beginner", vec!["F#", "Python", "SQL", "Prolog", "OpenTofu"])
        ]
    }
}
```

