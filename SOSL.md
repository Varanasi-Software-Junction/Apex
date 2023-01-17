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
