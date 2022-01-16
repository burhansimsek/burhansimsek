# Burhan Şimşek | Jr. Data Scientist

## Hey! 👋
I'm Burhan, a 22 years old Data Scientist from Turkey.

## Skills
- 👨‍💻 Python, SQL, Data Science

## Contact
- Linkedin: https://www.linkedin.com/in/burhansimsek/
- [burhansimsek.com](http://burhansimsek.com) on Website
- [@burhansimsekbs](https://twitter.com/burhansimsekbs) on Twitter
- [@burhansimsekbs(https://instagram.com/burhansimsekbs) on Instagram

​
from __future__ import annotations

import json
from dataclasses import asdict, dataclass


@dataclass
class Arsenal:
    languages: tuple[str, ...] = ("Python", "JS", "Go")
    databases: tuple[str, ...] = ("SQLite", "PostgreSQL", "DynamoDB", "Redis")
    misc     : tuple[str, ...] = ("Docker", "Celery", "RabbitMQ", "Arq", "SQS")
    ongoing  : tuple[str, ...] = ("Django", "DRF", "Asyncio")

    def jsonify(self) -> str:
        return json.dumps(asdict(self), indent=4)


arsenal = Arsenal()
print(arsenal.jsonify())
​
