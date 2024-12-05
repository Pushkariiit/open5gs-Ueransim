Navigate to ueransim -> 

```cd ueransim```

Clone the most popular RLS-wireshark-dissector

```sudo git clone https://github.com/nextmn/RLS-wireshark-dissector.git```

open the wireshark and go to plugins section

``` cd /usr/lib/x86_64-linux-gnu/wireshark ```

``` cd plugins ```

```cp -R ~/ueransim/RLS-wireshark-dissector/ RLS-wireshark-dissector```

![image](https://github.com/user-attachments/assets/92616efe-f722-49d0-9bdf-80c082fe70c2)

Go to open5gs port -> 9999

Add the subscriber using the MSI numbers ->

![image](https://github.com/user-attachments/assets/e3575cfe-a0dd-469d-98e8-121cfb0a7db3)

Now I build UERANSIM using the commands -> 

``` ../build/nr-ue -c ue2.yaml```

Since I am interrupting, there are some errors messages receiving.

So I am using the commands as an administrator -> 
```sudo ../build/nr-ue -c ue2.yaml```

![image](https://github.com/user-attachments/assets/33f9d753-bae4-4f95-b5a4-d86819c15f90)

Now we can see the errors are resolved.
