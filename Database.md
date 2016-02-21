Finding data:

Example: Find User whose id is 1: (select * from user_table where id=1)

Symfony (Doctrine):
```
$user = $this->getDoctrine()
        ->getRepository('AppBundle:User')
        ->find(1);
```
or

```
// get repository
$repository = $this->getDoctrine()
    ->getRepository('AppBundle:User');

// return user model
$user = $repository->find(1);
```



Laravel (Eloquent)

```
$user = User::find(1);
```

Produces the equivalent of:

```
select * from {user_table} where id = 1
```
