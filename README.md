## Compile check? 
```rust
struct PersonalInfo<'dynamic> {
    name: &'static str,
    description: &'dynamic str,
    mail: &'static str,
    interests: Vec<&'dynamic str>,
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
            ("Intermediate", vec!["C", "Java", "Kotlin", "Docker", "Git"]),
            ("Beginner", vec!["F#", "Python", "Bash", "SQL", "Prolog", "Terraform"])
        ]
    }
}
```

