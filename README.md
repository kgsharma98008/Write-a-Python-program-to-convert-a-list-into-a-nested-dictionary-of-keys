# Write-a-Python-program-to-convert-a-list-into-a-nested-dictionary-of-keys 
def list_to_nested_dict(lst):
 # Initialize an empty dictionary
 result = {}
 # Iterate over each item in the list
 for item in lst:
 # Get the keys and the value
 keys = item[:-1]
 value = item[-1]
 # Create the nested dictionary using the keys
 d = result
 for key in keys:
 d = d.setdefault(key, {})
 # Set the value at the final nested dictionary
 d.setdefault('value', []).append(value)
 return resul
