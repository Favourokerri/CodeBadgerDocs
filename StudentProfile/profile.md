# User Profile

### Model
    the user profile inherits from the defualt user model provided by django

```
class Profile(models.Model):
    user = models.OneToOneField(User, on_delete=models.CASCADE)
    profile_picture = models.ImageField(upload_to='profile_pictures/', null=True, blank=True)
    Phone Number = models.TextField(max_length=20)
    courses = models.ManyToManyField(Course)
    address = models.CharField(max_length=200)
```
