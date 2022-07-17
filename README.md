Hey, I'm Michael Genson! 👋
---
```python
from models._base import Michael
from models.work import Project


class Worker(Michael):
    def __init__(self, current_project: Project = None, **kwargs) --> None:
        super().__init__(**kwargs)
        self.current_project = current_project
        
        if self.working or self.bored:
            self.start_work()

    def start_work(self) --> None:
        if not self.current_project:
            """
            If I'm not writing some custom systems integration at work,
            I'm probably tinkering with some open source software to save
            myself 5-10 seconds of manual effort
            """
            self.current_project = self.find_something_to_work_on()

        self.current_project.do_work(self)
```
