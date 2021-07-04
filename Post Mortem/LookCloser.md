> Look Closer
>
> The resistance managed to find a suspicious file. They believe it contains some useful data. Unfortunately, they weren't able to retrieve it. Help them find what they are looking for.

The challenge provides us a "data.txt" file.

<p align="center">
    <img src="screenshots/LookCloser-1.png" style="width:70%; border: 0.8px solid black" caption="Output of the command" /><br/>
</p>

The content looks like base64 encoded text.

`$ cat data.txt | base64 -d > 1`

After base64 decode the file, we got a hexdump.

<p align="center">
    <img src="screenshots/LookCloser-2.png" style="width:70%; border: 0.8px solid black" caption="Output of the command" /><br/>
</p>

Next, we convert the hexdump into binary.

`$ xxd -r 1 > 2`

<p align="center">
    <img src="screenshots/LookCloser-3.png" style="width:70%; border: 0.8px solid black" caption="Output of the command" /><br/>
</p>

It seems like the file signature is not correct.

Modify the file signature:<br>
`$ hexeditor 2`

We change the file signature to .ELF instead of CDDC

<p align="center">
    <img src="screenshots/LookCloser-4.png" style="width:70%; border: 0.8px solid black" caption="Output of the command" /><br/>
</p>

We got the flag when we execute the binary.

<p align="center">
    <img src="screenshots/LookCloser-5.png" style="width:70%; border: 0.8px solid black" caption="Output of the command" /><br/>
</p>

> Flag: CDDC21{C@n_Y0u_F1nD_mE?}