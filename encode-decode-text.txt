




echo " FILE ----ENCODER/DECODER------"

echo " 1) Encode "
echo " 2) Decode "
read opt
case $opt in

	1) 
		echo " YOu have selected encryption of the file"
		echo " please enter name or path of the file to encrypt"
		read file
		gpg -c $file
		echo " the file has been encrypted "
		echo " would you want to see the file "
		read ch
		if [ $ch=='y' ];then
			vim $file
		else

		echo"Oops"

		fi
	
		break;;

	2) 	echo " you have entered decryption"
		echo " please enter file name or path  to decrypt"
		read file
		gpg -d $file
		echo " your file has been decrypted"

		echo " would ypu like to view the file"
		read ch
		if [ $ch =='y' ];then
			vim $file
		fi
esac




