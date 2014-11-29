erlang_cc
=========

a simple 101 in how to make a otp erlang app

Game Analytics programming challenge
 
Your mission, should you choose to accept it, is to write a program to count unique users. Your program must process Apache log lines and

 extract the user ids from the URL. 

 -user will call your API to query how many unique user ids was seen between timestamp A and timestamp B.
 
- Your program must accept input on UDP, port 4263. You will receive one datagram per log line.

 -Each log line looks like this example “127.0.0.1 - hostname [1371731248] "GET /123/foo/bar HTTP/1.1" 200 2326”.

 Where “123” is the user id and “1371731248” is the timestamp of when the event happened.
 

Your program must answer queries over HTTP.

A user will do a GET request to the “/users” URL with the following parameters: start=1371731248&end=1371731248.

The start and end are arbitrary unix timestamps. Your program must return the number of unique users in that timeframe as a ASCII encoded integer.

WEBSOCKETS -> update in real time when no start or no end is specified.

cowboy server rocking on

listen on tcp 8080, udp 4263, parse


APP
	SUP
		gen_udp
		inets
		



