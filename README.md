from dataclasses import dataclass, field


@dataclass
class Developer:
    name: str = "Henok Kebede"
    role: str = "Full-Stack Software Engineer"
    motto: str = "The best code is self-documenting code."
    languages: list = field(default_factory=lambda: [
        "Python", "JavaScript", "SQL", "HTML5", "CSS3"
    ])
    frameworks: list = field(default_factory=lambda: [
        "Django", "FastAPI", "Node.js", "React"
    ])
    databases: list = field(default_factory=lambda: [
        "PostgreSQL", "MySQL", "MongoDB", "Redis"
    ])
    currently_building: str = "Scalable full-stack web applications"
    currently_learning: list = field(default_factory=lambda: [
        "Advanced system architecture", "Cloud services"
    ])

    def solve(self, problem: str) -> str:
        """Turn complex logic into clean code."""
        return f"Broke '{problem}' into small, readable pieces ✅"

    def open_to(self) -> list:
        return ["Collaboration", "Open source", "Interesting problems"]


if __name__ == "__main__":
    me = Developer()
    print(f"Hi, I'm {me.name} — {me.role}")
