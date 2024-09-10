# Creation of Courses

## Model

```
class Course(models.Model):
    """ course """
    name = models.CharField(max_length=200);
    description = models.CharField(max_length=300);
    fee = models.DecimalField(max_digits=10, decimal_places=2)
    created_at = models.DateTimeField(auto_now_add=True)
    updated_at = models.DateTimeField(auto_now=True)

    def __str__(self) -> str:
        return self.name
```
