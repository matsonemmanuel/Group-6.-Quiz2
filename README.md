def is_valid_password(password):# Function to check password validity
    if len(password) < 8:# Check for minimum length
        return False

    has_upper = False# Check for uppercase letters
    has_number = False# Check for digits
    has_special = False# Check for special characters
    special_chars = "!@#$%^&*"# List of special characters

    for char in password:
        if char.isupper():
            has_upper = True
        elif char.isdigit():
            has_number = True
        elif char in special_chars:
            has_special = True

    return has_upper and has_number and has_special
print(is_valid_password("Hello123!"))  
print(is_valid_password("hello123"))   
print(is_valid_password("HELLO!@#")) 
