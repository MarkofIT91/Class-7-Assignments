Homework Week 1
- Readme Instructions on how to configure the EC2 with teardown Instructions
	1. ==EC2 Creation steps==:
	2. Sign into AWS with your IAM account, NOT your Root account!
	3. Be mindful of the AWS Region you are currently operating in. This dictates what services will be available to you.
	4. In the search bar or the "Recently Visited" widget, select the EC2 Icon.
	5. At the EC2 left side navigation drop down menu, scroll down to "Network and Security" and select Security Groups.
	6. After that select, Create Security Group.
	7. Under "Basic Details", type in the Security Group name of your choice. The security group name here can only be all on word and no spaces. A naming convention is best for Professional uses.
	8. The "Description" can be whatever the purpose of this Security group will be used for, up to you as the Architect.
	9. For the purpose of this assignment, we will be using the default VPC provided to us by our IAM account.
	10. Under the "Inbound Rules" section, select "Add Rule" and set the "Type" to HTTP. This will auto select the Protocol to TCP and the Port Range to 80.
	11. Set the "Source" to Anywere-IPv4. and leave the IP Address to 0.0.0.0/0.
	12. Add a Description for what this particular rule is for if desired or need be.
	13. DO NO TOUCH OUTBOUND RULES FOR THIS ASSIGNMENT.
	14. Add any necessary tags to this Security Group to better identify what it will be allocated for.
	15. Then select "Create Security Group" at the bottom of the page.
	16. Should you get the green confirmation that the Security Group was generated, go back to the Security Group tab under Network and Security to verify the Security Group has been generated.
	17. Now go back to the left side navigation drop down menu, scroll up to "Instances" and select Instances just below it.
	18. Then select "Launch Instances"
	19. Under "Name and Tags" give the Instance a name of your choice.
	20. Under "Application and OS Images (AMI)" select Amazon Linux AWS. This should default to a Free Tier Eligible AMI, make sure.
	21. Under the "Instance Type" for simplicity, select a Free Tier Eligible option. It should be selected by default.
	22. Under "Key Pair (login)" select Create new key pair.
	23. Under Key pair name, make it something you will remember, you will need it later.
	24. For "Key pair type" select RSA and for "Private key file format" select ".pem".
	25. Now select "Create key pair" and if filled out properly, you will be prompted to save the .pem file to a folder for future use.
	26. Under "Network Settings", make sure that the "Auto-assign public IP" setting is set to "Enable".
	27. Then under "Firewall (security groups)" select "Select existing security group" and find the recently created Security Group you generated under "Common security groups" and choose it.
	28. For the purpose of this assignment we do not need to modify the "Configure Storage" so minimize that section.
	29. Expand the section of "Advanced Details" and scroll all the way to the bottom to the "User data - optional" field and paste your script/template in the empty box.
	30. Select "Launch Instance"
	31. Once you've gotten the green that the instance is being produced, await its Initialization back within the "Instances window.
	32. Every minute or so refresh the Instances window and check if the "Status checks" have all passed.
	33. Once it has, select the "Instance ID" for the now live Instance to view in depth details regarding it.
	34. Within the "Instance Summary" page, find the "Public DNS" for the instance and copy it to your clipboard.
	35. In a new window, in the search bar type "http:(paste Public DNS here)".
	36. Behold, an EC2 Webpage/Server you created!
	37. ==EC2 Teardown steps==:
	38. Back within the EC2 Instances window, select the check box off to the left for the running instance and then select "Instance State" at the top rightish and choose "Terminate (delete) instance" at the bottom.
	39. Once the Termination of the Instance has been initiated, refresh the Instance window every now and then to confirm termination.
	40. Once the "Instance State" shows as Terminated you have successfully tore down the EC2. You can reuse the security group and key pair you created for future instances should you choose to and do not need to delete them as you are not charged for having them.
	41. Congratulations on your Success!
