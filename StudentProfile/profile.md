# User Profile

### Model
    the user profile inherits from the defualt user model provided by django

```
class Profile(models.Model):
    user = models.OneToOneField(User, on_delete=models.CASCADE)
    profile_picture = models.ImageField(upload_to='profile_pictures/', null=True, blank=True)
    Phone_number = models.CharField(max_length=20)
    address = models.TextField(max_length=200)
    registerd_courses = models.ManyToManyField(Course)
    created_at = models.DateTimeField(auto_now_add=True)
    updated_at = models.DateTimeField(auto_now=True)

    def __str__(self):
        return self.Phone_number
```
