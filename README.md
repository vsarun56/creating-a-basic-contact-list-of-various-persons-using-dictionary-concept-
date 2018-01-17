# creating-a-basic-contact-list-of-various-persons-using-dictionary-concept-

i=1;  d={}

while 1:
    
    print('Enter basic details of the %dst-person: '%i)
    d[i]={'Name':None,'Age':None,'Sex':None,'Phone':None,'address':{}}
    
    while 1:
        
        d[i]['Name']=input('Enter your First Name:')
        
        if d[i]['Name'].isalpha():
            break
        else:
            print('Invalid Entry....Retry:')
    
    while 1:
        d[i]['Age']=input('Enter your Age:')
        
        if d[i]['Age'].isdigit() and 1<=int(d[i]['Age'])<=120:
            break
        else:
            print('Invalid Entry....Retry:')
    
    while 1:
        d[i]['Sex']=input('Gender- M/F:')
        
        if d[i]['Sex'].isalpha() and (d[i]['Sex']=='M' or 'm' or d[i]['Sex']=='F' or 'f') :
            break
        else:
            print('Invalid Entry....Retry:')
    while 1:
        d[i]['Phone']=input('Enter your Mobile number:')
        
        if d[i]['Phone'].isdigit() and len(d[i]['Phone'])==10:
            break
        else:
            print('Invalid Entry....Retry:')
    print('Enter your address')

    while 1:
        d[i]['address']['house no']=input('House No:')
        
        if str(d[i]['address']['house no']).isdigit():
            break
        else:
            print('House No-should be numerice value: Retry.....')
        
    d[i]['address']['street']=input('STREET:')
    
    while 1:
        d[i]['address']['zone']=input('Zone:')
        d[i]['address']['city']=input('City:')
        d[i]['address']['country']=input('Country:')
        
        if d[i]['address']['zone'].isalpha() and d[i]['address']['city'].isalpha() and d[i]['address']['country'].isalpha():
            break
        else:
            print('City , Zone, Country should be a word pls check: Retry......')
        
    while 1:
        d[i]['address']['pin']=input('Pincode:')
        
        if d[i]['address']['pin'].isdigit() and len(d[i]['address']['pin'])==6:
            break
        else:
            print('Pincode should be a numeric value and has 6 digits: Retry.....')
    
    
    con=input('Enter details of an another person ( Y/N)?: ')
    
    if con=='N':
        break
    else:
        i+=1

for k in d.keys():
    
    print('Details of the person- %d entered:'%k)
    print('Name:',d[k]['Name'].title())
    print('Age:',d[k]['Age'])
    print('Sex:',d[k]['Sex'].title())
    print('Phone: +91-',d[k]['Phone'])
    print('Address of the person:-')
    print('------------------------------------')
    print('House No:',d[k]['address']['house no'])
    print('STREET:',d[k]['address']['street'])
    print('ZONE:',d[k]['address']['zone'].title())
    print('CITY:',d[k]['address']['city'].title())
    print('COUNTRY:',d[k]['address']['country'].title())
    print('PIN:',d[k]['address']['pin'])
    print('***********************************')


