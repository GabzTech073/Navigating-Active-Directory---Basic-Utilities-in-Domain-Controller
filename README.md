# Navigating-Active-Directory---Basic-Utilities-in-Domain-Controller
In this part of the Tier 1 Project, I will be navigating Active Directory using my Domain Controller, and explaining how Users, OUs and Groups function within an AD Domain.

In this domain, I will be using my branch1 organisational unit to showcase the different functional utilities that can be explored in Active Directory. 

Now, let's say one of these users within the organisation "adeptuser" had forgotten their password, and made a request to have their password reset on their account, I would go inside branch1, locate the OU titled "Users" with all of the user accounts I made, and find "adeptuser" to reset the password.
<img width="892" height="847" alt="image" src="https://github.com/user-attachments/assets/e7054933-caea-4dbf-b84f-06833ca38181" />

To do so, I right-click on the "adeptuser" and navigate to "Reset Password"
<img width="868" height="840" alt="image" src="https://github.com/user-attachments/assets/f80cacb3-a33f-4022-b503-30031f9d72f9" />

Next a windows pop-up will show for the password reset. 
<img width="896" height="846" alt="image" src="https://github.com/user-attachments/assets/54ebe19b-d596-4ab3-9577-167907541edc" />
Notice we also have this account lockout status on the domain controller. It's unlocked. If the users account was locked out, but they still knew the password, I could just unlock the user's account as opposed to actually resetting it.

I created a Groups OU to talk about Groups. I then create a Group within the "Groups" OU and title it "IT Workers"

<img width="882" height="830" alt="image" src="https://github.com/user-attachments/assets/5a8b809e-d808-4069-86e4-2e45ad62752a" />

Groups are a good way of organizing people. When we're giving people permissions to things, when we're granting people the ability to do certain things, we generally want to do it with a group as opposed to a user, even if only one user is in the group. Because when you have more users and you become a bigger
organization, you're not going to want to have to put individual users permissions to different things. It gets messy and it also gets dangerous from a security perspective. 

You would rather give the group a permission to a certain thing or apply a GPO to the group or give them permission to some certain app or something like that access and then you'd rather put people in this group. It's a granular way of controlling access.

So let's say "adeptuser" is an IT Worker, and we wanted to add him into the IT Workers group, I would right-click the "IT Workers" name in the dashboard, navigate to "Properties" on the drop-down list,

<img width="815" height="792" alt="image" src="https://github.com/user-attachments/assets/aee04dca-7915-4d41-884b-7af54660c8ce" />

From there the Properties window will pop-up, and I will click on the "Members" tab to add a user from my "Users" OU into this IT Workers Group. 

<img width="835" height="820" alt="image" src="https://github.com/user-attachments/assets/b5ec22d2-e9fa-4bfd-8e29-7f0b10370273" />

From here another window pops up, I enter a name in the textbox to find the user (located in my lab.local domain) that I want to add into the Group, in this case I just type the letter "a" as all of the users currently created start with the letter "a", and then search for the users existing by clicking "Check Names"

<img width="822" height="798" alt="image" src="https://github.com/user-attachments/assets/0a3290e0-2915-450e-b0b6-6d83f76ce52c" />

The users show up in the next window, and I select "adeptuser" to add him into the "IT Workers" group. 

<img width="815" height="802" alt="image" src="https://github.com/user-attachments/assets/d0da2973-229d-495b-86fe-701fb1276198" />

<img width="832" height="803" alt="image" src="https://github.com/user-attachments/assets/b31deca0-a5e8-4162-8ad0-1dcf82b94f0b" />

Now when we look at the "Members" tab of the "IT Workers" group, we can see that "adeptuser" has been added as a member.
<img width="818" height="778" alt="image" src="https://github.com/user-attachments/assets/2261f9d9-d2d1-400d-ac00-2a4ffc1a0e8e" />

I will make a couple more users for the next demonstration of this lab. "tom brady" and "joe brady". I've added "tom brady" into the IT Workers Group, and so now there are two users in that Group. (adeptuser and tom brady).

So say if Tom Brady's account is locked, and he calls in to IT Support to have his account unlocked, I would double-click on his username within the Domain's dashboard, navigate to the "Account" tab, and then toggle on the "Unlock Account" radio button.

<img width="932" height="828" alt="image" src="https://github.com/user-attachments/assets/c37ea7ef-ccdb-48cb-b293-be929e556191" />

Let's say I have another branch in my domain, "branch2", set up similarly to "branch1" and I wanted to move existing users into "branch2", like "tom brady" for instance. This user, Tom, is in "branch1", but he actually got moved to "branch2". And so now he's going to have these policies that are applying to him that have to do with "branch2", that are linked to "branch2". I can just grab Tom and I can move him over to the proper OU that I have to. 

<img width="892" height="837" alt="image" src="https://github.com/user-attachments/assets/32e7fd9e-43bf-4978-b2e1-d57ab0d9970d" />

Let's say I wanted to create more Groups within branch1, like a HR group, a Security group etc. I can also create something known as a "Distribution Group"  Basically, a distribution list is a group of people who when an email is sent to that list, a copy of that email is sent to all people. So if you're in an organization, say an IT organization and you have a group that is ittier one domain.com right and you're a part of that group and you receive all those emails for it tier1dommain.com it might be true that this is a distribution list and every other tier one is also getting a copy of that email; that's a distribution list.









