Finding data:

* Example: Find a user whose id is 1:
        
  * Symfony (Doctrine)
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
  * Laravel (Eloquent)
                ```
                $user = User::find(1);
                ```
  * SQL
                ```
                select * from {user_table} where id = 1;
                ```

* Example: Find all users: (select * from user_table)
        
  * Symfony (Doctrine)
        ```
        // get repository
        $repository = $this->getDoctrine()
            ->getRepository('AppBundle:User');
        
        // return all users
        $users = $repository->findAll();
        ```
  * Laravel (Eloquent)
        ```
        $users = Users::all();
        ```
  * SQL
        ```
        select * from {user_table};
        ```
