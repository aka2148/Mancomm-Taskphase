# Question Title
- IP restriction bypass

## Question Description
Dear colleagues,

We’re now managing connections to the intranet using private IP addresses, so it’s no longer necessary to login with a username / password when you are already connected to the internal company network.

Regards,

The network admin

## Solution
So I had to learn how to bypass IP requirements
This is best done by using a proxy and adding a X-Forwarded-For header
**Syntax: X-Forwarded-For: <client>,<proxy1>,<proxy2>,<proxy3>**

Add this to your get request
We still have to decide which ip to use. 
In the reference sheet they gave, it mentions the following as private adresses 
- 10.0.0.0
- 172.16.0.0
- 192.168.0.0

Using X-Forwarded-For:10.0.0.0 in the request gives the password
