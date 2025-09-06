Today’s focus was Linux shell skills, Bash scripting, and system customization to build a strong foundation for penetration testing.

**1. BASH VAIRABLE CREATION**
- I Create 3 variables, VAR1, VAR2 and VAR3; initialize them to hold the values "thirteen", "13" and "Happy Birthday" respectively.
  
```bash
#!/bin/bash

VAR1="thirten"
VAR2="happy birthday"
VAR3="13"

echo "$VAR1, $VAR2 $VAR3"
```

- then Display the values of all three variables.
- Practiced displaying them with echo and different quoting methods.


**2. LOGIN CUSTOMIZATION**

- Edited /etc/profile so all users see a greeting when logging in:

```bash
# Add a welcome message for all users
echo "Welcome to this system, stay ethical!" >> /etc/profile
```

- Tested it by logging in as different users.

**3. ROOT PROMPT CUSTOMIZATION**
- Set a red warning prompt for root in /root/.bashrc:

```bash
# Change the root prompt style
PS1="\[\033[1;31m\]Danger!! root is doing stuff in \w\[\033[0m\] # "
```
- Purpose: to visually warn when operating as root.

**4. RECTANHLE SURFACE CALCULATION SCRIPT**
- I Wrote  a script in which i assigned two integer values to two variables. The script calculated the surface of a rectangle
- Added comments for clarity.
- Output is neatly formatted.

```bash
#!/bin/bash
# Calculates surface area of a rectangle

length=10   # example value
width=5     # example value
surface=$((length * width))

echo "Length: $length"
echo "Width : $width"
echo "Surface area: $surface"
```

**5.USER AND SYSTEM MANAGEMENT**
- Created a new user with sudo privileges:
- sudo adduser percie && sudo usermod -aG sudo percie
- Learned how /etc/profile (system-wide) differs from .bashrc (per-user).
- Learned how /etc/profile (system-wide) differs from .bashrc (per-user).

**Bash Skills Practiced**
- Quoting and escaping ('single', "double", and \backslash).
- Creating and removing aliases.
- Understanding environment variables.

**Takeaways**
- Shell customization improves safety and usability during penetration testing.
- Bash scripting is a core skill for automating security tasks.
- Proper system configuration ensures persistence of changes in a lab.
