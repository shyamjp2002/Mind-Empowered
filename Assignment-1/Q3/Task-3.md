# Task 3: Password Policy

- Install the "libpam-pwquality" package if not already installed.
- Configure the system to require passwords with at least 10 characters, including at least 
one uppercase letter, one lowercase letter, and one digit.

<img width="608" alt="task6_1" src="https://github.com/shyamjp2002/Mind-Empowered/assets/75899937/d618a1c5-1f90-4262-8ef6-39baedf14184">

<b>We write ``password   requisite   pam_pwquality.so retry=3 minlen=10 ucredit=-1 lcredit=-1 dcredit=-1`` inside <i>/etc/pam.d/common-password</i> file after the `nano` comand.</b><br /><br />


 - Configure the system to remember the last 5 passwords and prevent users from reusing 
them.

<img width="600" alt="task6_2" src="https://github.com/shyamjp2002/Mind-Empowered/assets/75899937/662ac098-63db-44f6-934c-111e6881e2bb">

<b>We write ``password   required   pam_unix.so obscure sha512 remember=5`` inside <i>/etc/pam.d/common-password</i> file after the `nano` comand.</b>
<br /><br />

- Take a screenshot of the "pam-config --get-parameters" command output and submit it.

<img width="416" alt="task6_3" src="https://github.com/shyamjp2002/Mind-Empowered/assets/75899937/ccebf1f2-a816-4a29-a045-57a5f484f805">
