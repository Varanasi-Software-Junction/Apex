FIND {"Champak or Changed"}   
RETURNING Account(name, phone), contact(name, phone)

![image](https://user-images.githubusercontent.com/68769644/212906585-3d702626-f8a3-422f-9821-8b5d001a0ded.png)



FIND {"Champak" or "Changed"}   
RETURNING Account(name, phone), contact(name, phone)

![image](https://user-images.githubusercontent.com/68769644/212906350-04a4b3bb-d85b-4552-abfc-d19df6c4e8ef.png)



FIND {champak} RETURNING account(name, phone)

![image](https://user-images.githubusercontent.com/68769644/212905673-f1e2770c-de9d-4d0f-93d0-53bea4008747.png)




List<List<SObject>> s = [FIND 'Champak' IN ALL FIELDS 
                                      RETURNING Account(Name), Contact(FirstName,LastName)];

system.debug(s);
List<Account> accounts=s[0];
for(Account account:accounts)
{
    system.debug(account);
    system.debug(account.name);
    
}
  
  ![image](https://user-images.githubusercontent.com/68769644/212905137-fe907f40-eb8c-42bf-88e5-a3d67b1ed3b9.png)
