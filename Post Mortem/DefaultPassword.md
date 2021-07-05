> Default Password
>
> Members of TheKeepers got their hands on one of the GDC computers. They created a memory dump of the system as they believe it might contain some juicy information. Help them find proof.

The challenge provides us a "data" file (a memory dump)

Get the profile suggestions: <br />
`$ ./volatility_2.6_lin64_standalone -f ../data imageinfo`

<p align="center">
    <img src="screenshots/DefaultPassword-1.png" style="width:70%; border: 0.8px solid black" caption="Output of the volatility" /><br/>
</p>

Since the title of the challenge is related to password, we try to dump the password stored in the memory dump.

`$ ./volatility_2.6_lin64_standalone -f ../data --profile=Win7SP1x64 lsadump`

<p align="center">
    <img src="screenshots/DefaultPassword-2.png" style="width:70%; border: 0.8px solid black" caption="Output of the volatility" /><br/>
</p>

Since the title of the challenge is "Default Password", we guess that the flag is "Th1s_i$_A_L0ng_p@s$w0rd".

> Flag: CDDC21{Th1s_i$_A_L0ng_p@s$w0rd}