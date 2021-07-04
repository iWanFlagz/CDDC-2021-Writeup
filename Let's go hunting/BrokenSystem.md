> Broken System
>
> The CryptIT Banking and Consulting company suspects that the GlobalDominationCorporation is attacking its email systems. They need your help to fix the misconfiguration.

Since the challenge is about email, we look into SPF, DKIM and DMARC (email security protocols) misconfigurations.

We look into SPF: <br />
`$ dig TXT cryptit.biz`

<p align="center">
    <img src="screenshots/BrokenSystem-1.png" style="width:70%; border: 0.8px solid black" caption="Output of the command" /><br/>
</p>

Next, we look into DMARC:<br />
`$ dig TXT _dmarc.cryptit.biz`

<p align="center">
    <img src="screenshots/BrokenSystem-2.png" style="width:70%; border: 0.8px solid black" caption="Output of the command" /><br/>
</p>

> Flag: CDDC21{_10x_f0r_yOur_Serv!ce_}
