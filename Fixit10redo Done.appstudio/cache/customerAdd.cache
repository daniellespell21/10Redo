customerAdd.onshow=function(){
  drpAddCustomer.clear()
   txtAll_contents.style.height = "200px"
  query = "SELECT name FROM customers;"
  req = Ajax("https://ormond.creighton.edu/courses/375/ajax-connection.php", "POST", "host=ormond.creighton.edu&user=dls46032&pass=Dog123!&database=dls46032&query=" + query)
  if (req.status == 200){
   results = JSON.parse(req.responseText)
   console.log(results)
   console.log(typeof(results))
   for (i = 0; i <= results.length - 1; i++){
            drpAddCustomer.addItem(results[i])
              }
        } 
        }
    
btnAddCustomer.onclick=function(){
  query = "Insert Ignore into `customers` (`name`,`street`,`city`,`state`,`zipcode`) values ('Jesse Antiques', '1113 F St', 'Omaha', 'NE', 68178);"
  req = Ajax("https://ormond.creighton.edu/courses/375/ajax-connection.php", "POST", "host=ormond.creighton.edu&user=dls46032&pass=Dog123!&database=dls46032&query=" + query)
  if (req.status ==200){
    if(req.responseText ==500){
    lblAdded.value = `You have successfully added Jesse Antiques to the customers.` 
  query = "Select name From customers "
    req = Ajax("https://ormond.creighton.edu/courses/375/ajax-connection.php", "POST", "host=ormond.creighton.edu&user=dls46032&pass=Dog123!&database=dls46032&query=" + query)
    results = JSON.parse(req.responseText)
              for (i = 0; i <= results.length - 1; i++)
                 // message = message + results[i] + "\n"
             // txtAll.value = message
              drpAddCustomer.clear()
              for (i = 0; i <= results.length - 1; i++){
            drpAddCustomer.addItem(results[i])
            }
    }
  }
}


Button1.onclick=function(){
  ChangeForm(customerUpdate1)
}
