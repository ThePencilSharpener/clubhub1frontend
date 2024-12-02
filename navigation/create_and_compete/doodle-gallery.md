---
layout: post
title: Voting for Doodles 
description: Vote for your favorite doodles 
menu: nav/doodle.html
permalink: /moderation/gallery_doodle/
author: Arshia, Prajna, Mirabelle, Alex
---

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Voting Page</title>
    <style>
        /* Styling for the page background and layout */
        body {
            background-color: #f2e6ff;
            font-family: Arial, sans-serif;
            color: #4d004d;
            display: flex;
            justify-content: center;
            flex-direction: column;
            align-items: center;
            margin: 0;
            padding: 20px;
        }
        /* Container for each image */
        .image-container {
            border: 2px solid #a64dff;
            border-radius: 10px;
            padding: 15px;
            margin: 20px;
            background-color: #e0b3ff;
            text-align: center;
            width: 250px;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
        }
        /* Styling for images */
        .image-container img {
            max-width: 100%;
            border-radius: 10px;
        }
        /* Vote button styling */
        .vote-button {
            background-color: #d966ff;
            color: #fff;
            border: none;
            padding: 10px 15px;
            border-radius: 8px;
            margin-top: 10px;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        /* Vote button hover effect */
        .vote-button:hover {
            background-color: #9900cc;
        }
        /* Vote count styling */
        .vote-count {
            margin-top: 10px;
            font-weight: bold;
            font-size: 1.2rem;
        }
    </style>
</head>
<body>
    <h1>Vote for Your Favorite Image!</h1>
    <!-- Example of an image container -->
    <div class="image-container">
        <img src="data:image/jpeg;base64,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" alt="Sample Image 1">
        <div class="vote-count">Votes: <span id="voteCount1">0</span></div>
        <button class="vote-button" onclick="addVote('voteCount1')">Vote</button>
    </div>
    <!-- Add more images like the one above, with unique IDs -->
    <div class="image-container">
        <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOEAAADhCAMAAAAJbSJIAAABklBMVEX////+5Wb+5WT+5WcAAAD9yjD/97b/+LT+zjD95mXL4Nn+zTL/9rP/97gAABMXChv9sY0AAAkWCxkAAAf+5mwAAA4AABT/42b95WD+6X3/7Gn/0jL+53ERABgQABULABH19fX//7j+6Hfl5eXa2tr/7Wb/7nDR49+qqarDwsP//78MAA/v7+//8Xagn6D//Km4t7j88In479j9+uT+3Vb7+fKEg4WYlpdycHLQz9CsnVX710PzxU66pWL6tob5u4EuJDWdqKEvIyM9Oz5fXkyAf2S/vY+xrInt56ooHR4uKi+EgWTv33laVlrm0nP15cHT0p399ZtlXEL13Jj3rgDvvVmpm1/21IH7wjk5Lyr13a9OTT3Yx3L3zGr60k779sR2bEf3vUPw1Zr++9b3uxT+/OloZWiZmXL3583wxGBVSzf2uUP7sADLvG9nXUJANiwEACQuIDbby2SRhEx6Xjazjz1lXDerijk6JiFpTy83NTqckE1NNymTcz/Op02vqVj6xXr83HR8bzyVfTfVs0iDjYZNGGfiAAAYTElEQVR4nO1dDVsT17ZmZjZJpoHMyWQmmSSTCYwmCoiABsSGqhVrhYKtrVXsAepVpKcevdwjVVts/e7/vmutvfdkEgJIaxLufeZ9KgTIJPvN+l577WlfX4QIESJEiBAhQoQIESJEiBAhQoQIESJEiBAhQoQIESJEiBAhQoQIESJEiBDh/yuGJmfnF+dnJ3u9jk5haIaxTNkrZxg73eu1dAQjjBmGWbZThumxnaFeL+fj4zTzgBm78sUVm5nGGDvW6wV9bJxkppm5fHV0eHg49iUrA9lTvV7Sx8V5Zpjsi+Hh+MBAPD58baFsji32ek0fFUOgouwr5DeAFCeWFjyDzfZ6VR8Ty2nTvjI8MCAZOtfB67CRXi/r42GSGaWxeEwSBIaVz+BX6cO8xtedWtzHAOiowb4ZDgjGbzhO9duUwWY+/DW+u3mUKc4yM/3FKIowRgTjU47jLGVAT49/6EtM929838kl/j0cZ4bHdTQWi8cHBMPKLWaWdz70NW6vJDemO7nIv4XFssmuDseAHzCMAdN43lEdZ/wO6O7JD3uJMxtztY0fOrvMvw6I9al/jqIFgo4OxDAiuiowdFYxRg590GusrUzl1n/u7Dr/MsjNXKNI+OODB/eBZHxCUZFi9e7BzuaH22s/r33/Xytv4m5u5Ux3VnxYzDIj8xX50Rga0mAMXSkxdJbSIMR989Ppm482VubW1r67P2D56ytr9/519IzxGIVCChM/4s8/kqNREeBsMubY8r6Xf72x/uN9xFTOddf7NzY2jpwkl8cMcDPE8Cz8OA0ijPucoOP4C6WDMpszGyuD94Gkm8vlarVafeOoxcURZpS3RongIP58FjMaXZUUH0MgWdj/Fc5sbAzcvz9R49jY6AHBfS3DLJnsG66k9/FnVNIbqq7pOnc2D8vGQQX/9MrG4H2f+NV7oqNrc/v88Rwz7S94uhZ/AD9PU0ajKrouKK5iBj60/zt8/ejGlJDgXHcdDb3b7Y2VvZ9xCiPeNQyCcc7wPj6wNJ2gAcXqXfvAMuq7jZrU0XsfcfkHY/rmxtoPtzdq+2RTm2mT/cQjRTz+4zRY4QApKdJTUIoQMdhBEaNvDhmurKwDwy7npmtr9+DNcxt7mgYmpAvDJEDMSOMxSkp9lesoZ/gBEeNREl3oys2VevJml7X0Jvyr1frn9qK4QwkpLyjwCz2aUBSFGCo8s/Gx3N8vYpx5tN7/6Pvpvq9Xbm7c/FcniOyNn+/1PajXasmNubZJ8SQlpKKcCDClohlqGmcIYf8xMz1zn3e5B2H+B/HoUXcNse/2d31n67VcrbjR1hYzEM6/icdIQTnAHIc1FU1QR37cnY4fEDHWHgUedPp2d2U4ffNB3yA4gf72dc0MM9JfjYYJorKCCBWgCHJUVBH4r4O57hMxzvSuarq31vegH5S0vYM7xkyTDTbzA2iKQoao6fiNGBbu2uaRbbxN/3uj1t/eNpYh0H05PLhLhIpOnoagBDXGIRoa3cbPK+0zRUxI74zGWpQUKkMuQgGenmLEKM93e+UfjJVHbYMF+Ef2TSvDWF5tx9AZvwNO6cjuuU23bS5AQpq+MjoYJhiLx26oyFBrZihrjHK3V/63cAoT6muxQITwFR+5OQwSYYoY+bHG+O+UeZjuae+xPAYJaZMIsc0GbgZlpmh6sxAxPc2A5z2yzmYXTm2C0pGbGRQtYBLmDSCokCHqejNH7myMnf8TGxnHJ2fmmW2YPJuJxRsEJ6ycCPIhhoo0xfEtY8djbPb0yJHdVxw6Pnluc5ExVioZZgmKppikSLKMYXdGUXnCjZbIUzdFkXp6/ZKxaHrGJXiF+dlzk8eHek0ohFPnT84sm7AyZnsGIsXsq8PELxbjAuRGqGgqpygUVcHozyk6Sn7p4f/8xyubpumNZfDFxpZnTo/0ei98CLjN42oy5RJSK5VtWNzWV1dHhzm/2IAgSl4GREeORuGpG/HkYlRU33UKT259O8bsVMozCWP4ymxh81xveA6dP725QNyAGXzudhpXc+WrL78ZHB0dlcLj/EBHb6gQKDRNE9k2ylFvUASOrgthsZD3n7x68fZhlqVtWxD18IXZ8rnu2ufxc/OBTpaI250rP10FbsPDXCsHpXbi4wZBVQ1cjSocDdVRmmspeUtzfR+eoheq7tLqp9t37zCWBoEaUp6LM+e7RG8G3q1sGqZRtuHR1hc/Xb02itxoWylkeQG/OCeocFfDFTVQUyBr5f183vLzvpUXTwFxFgTRh2WWSWVLqCfwbjOdV9jzywzKIrMEBle+8hXKbRTkNkA9inBwGGxIMD6Vy6nCCAWaGOp5S1X9PFFXhdKqouxwKpXq0uMXzy4zO1uC92Vss8PaOsvGTLOcYQtfXL0WE3ILNq/DDDlFlOBwPpcLkQsiIkqVGILkgJTvq4K0+BI0xh0HFHfp1fZlliqZRuZD9xz/Ek4tgvzK7J9fXuOCGxgQDrORuXD9hMeDyA6+QKDPiZ6MCq6GRKSI6hAsE77qeY2HEF1KlntbHltkJ8CpVJ98upX2zENt/x8SQ2NjYAxXvhnlwU4wlD0YaXgBU2RIGsr5CQ3UtEBUuHzL9103rxwAIc1K9fEWJrAdo7iTBoJXR+MDMphLcgMoxYGQDIEdiHAwNuE2NFQwVISb4cHeyrvwn5vX9L3IaSR4VQeGyNLdxu5IhxLYGSjbF64ND0gJiTavZBprBiroFHmYEENpajxMaKqbt3Rdy6uu1oZZg6Gm6UGkqd5ikBR2hCDVfEsTIEGysCBpiTcxHCTE4shPzVmaogQybMgvEKbvYlzM61K8ukwBiJkImURRmC6g+kvqgyccDofTzLA/dXL5G/HBwYao4kHka/BDihN5MkA3HCO4xmkkHk4VNFSHQMEFJeXLiXCCQoYUSvnPtcRc2uhMV2fZNmxXzeVy1hQnGdbLQSk8/B6fmLLUHLlO1dJaGILCaUKYKlEEI9RCDDlJ/gxJUM3/ePbBDWToJPv7k79kjY6o6ZiXelZVlRyu1cpPTVBECLRVii8ev5HH+MAJoS9RGmmMLqWoS3eD+QyR0RRZGEtLlcoKsnNpZ87R9Xo/IPEUGHYit2FG6m1B4SoDyFn+1NSNiYlQq3DixpRvqU6QmfEHlozxgWfUlEZ9ofJ4L4p/rp1hV4MWqObx/eMOChAIFl/anWmvEkNcn0qOm8finJrTLNd1LaGNOeE2c7mGdtKfhIC4nkoRqviXkBpLhyPFzW0WAsXg/YG8UwOCCWKY6gxD0lI0iqWzDwZ0FS1S6KwAsIVf5LgBaorSRFGRzjBgKO0u9AqQr8JHIdgHoYI2GnMqaGgCrTBRfN4hLZ0vlxZc/ERx5ODsFNAAMjngmCOIFcMjrWnZKA5LC3WfyAwVoah6M8OAmcjguFJTsKj3JwBAMFHslKeZYSZ7gsUODVWcdWAZOYW4BUYTXmvwCJsVVri7xi0t/JSwgmrECz5IPXClKMc6cgMZwtf1cqkz0eI8M7LPqsAwT0J01NaCoVkUDZngVlqYoqbrLcqpcsUOQ+cbxS0EkyjCl7bZoSMpi57BruN+Ue7G/fticksSaSZIZqjJEE85WpMUG+lLiKDeQpG2phT+kKtoEhkW67+WzA4dZZhkhrdVlQ3OPQWoBgmXHigZpi/BzmEj4DVfsoth8FogQQR4GvQzHdxt3PHMzIsKf+cWYwvLM2RwkqC+OyXlxZN4meBpTXoKf0KVxjif6KdQCDo6lzI7JUKaHiFng1pFAY88n+SqhPgVmkQoHaOyC/xaPbgmLET6q04EOT9iWP8t28k9HHCnZdBT/HR5NhyKaVwk+JkXquO+P14Nr1cKTtMb6ZjOOfBN/UIVLhkvhCkqgnstmRQE0c08TZvlQ51iOCQWPTO9XcBNeJHvqy1RG1ZUvb69lWZ3tq9XlGaRyGQFlTJ8FVwzvnp3gWW2XvghQYo/OZIfirA453Wu/iWQnj4uiDUjSRG8xT4ZLvYWSzO2wxh70UaMiuxB8ZSMX1Pw7zKblRcZsx9Xgku4/jrFgGBS6OhmBwlikWh69pLeWLYu163yEq66DYkB1qezjL2tKsouiryk1TURFVEPxx9mSDBDyyz4+JAhfhr1RCKko8+xj9JRgnSCKfWw2qAoGQqNKzwWBLGeZK8KuxkqofxbuJhbQJDv4u+UGf/4qIHMjTAZ0lG7wzqKwFNome1qk/rROjlDmjngzxyBZ1bDphiKFZIhXuvkmWFk+DUnWepuQRohMHQSDR1NJtZ/9bqxF34ee12PK42Fy+hHiQCdSeNPPM7MzGr4k9Bkvt18XeGztFEy+DWToAEuTb2p9MnV+8Nu5g+7O6cWTyPF66HghfmJyhkWPrOD4Z/TUFC+KIQYCjfDjTDEcDtlyGpoNmNmnnCGJML+ZMPNFF9iq7QrG22bEBUX3CABkS1sFGHhFqyWJ/7HQJrZ7RBD3sYggkLoCn0yeLDEKNOIKepHerXAGcIziiEJJsgIO9nRD2GhbNrfBqGA+0Mxt40yNNILp0fOMc8w7U/DDDXZrdcsSswVCvlchibbOTkyA7EIkyaN94D1WjhQrP/e8UDRwDE887odmGJIhmSHfB8Md/0adqgEnobU29Jk6q3olc8ywTWGaaRdnbsaCIXSjya5EXY0mWnGCPqTwNvQpgqvONTqlmcYpkBpIfClSuBqeEruikFhJOJnjMY1Nu924cdW6w8FipddHrg5hyOh16UKhqoMOl4glwvxUGuG6E/AIxdJ8DqscqtxjZfxdeG99GIyZIRYUXT1TgzLkNss+LJhG9TAOvgaXC6tl203hUMpS+GiXC59uMQZv5sRDEtslWff4YwbszU0wv3n3T86FscgtxnXsUIgbsL76Wr1M2aXYK0pyEt3ERT5AT2y5LaS6kCqlyoZnmebTyq6ZFjvbzJCr3tGyHGKlUhIwDGoY0Vt6G9v2fbW9lKBaiW54FDI0FX6jcV7UqipFahH7LFvX1UrumQI6UxCEuy2EXLQXRI+rTQSNmoxFQpU7AGaar1wOUwSx98UrOBnla6pVApVq1rgzaq6ZJhMzGW9LhshB89tCoIiRUXrzeuLFy5cuPh6zeKyEIqoV1efiA0B7nrxye6qb3Gh8taAuPjCxdtUJRYTiR4aIccseBvPl0IERq//EeDCa0sXObmCyRxjr3Tuk0SrEVIZxpYs2RvXtTcXGle/dgsONkcbRpjpBUGodcYMrKQ4RV0PEQRctBQ3n/eJAaQt2WeFgCEFCd/20qu6kKKirzVdfMGvE0HQ0eLLdO9GT/EQc/qtoKi7/2jGGytvaXmXEvJbdmmrqonOB3V0nCVWyjzRsI9KzudC88WvizzcgxGWemOEHMfRFD8tUGNCt1oZ+q6ed30KI5CYpV1ZM6g0dgD5HVa7RBG88MUWhoER/pbqnhFO7z76c1JWUrg9dLt5jarvggTzxPC62PPQA4aVx2mT+dTwp3jxplnFed0ERviuC32LAD+0OVgB3qa0YAlLfNMQxIXblmblXc33qTmeZ54diizIcDvl3alSIUWbb7obuvi16JFiyQQxqUsDe319bU9VzZfNDOopX7m79vrixYuvX79x8ziIB//o+JZafZjyuE/SaSyRjlhkccMVf2Fh5q47Fl188fUby3Gwj49V7y+HuwPK38OZtqd/oNDFtcv5Zt3BJTtqXlGAoeyi0u1o2GpFlvU6KGnGZKu6QuWwZvGg4uDFDk0GFftpJ60O8Wi/k3sfE/9au93+/OZyGYokXW1s+uI3y1fyrusHDB3f9EqmH1CsXLc98K5ywE2xZHEi9pSRYQKkuJ7p3pmv23udbZzNGGPjqhokJ/DVhSjhu+Bp5EaiQ+coy5eXCqDPBacy/jhVIhEKgpiGUwMgOH+Bu0wgxblMF5X0hz0oEsNgwJkI5S3Vz0O4591tqoydwl2gyLaXxsfH848fUtpekXsyRJEfuJRCp+3sRGIdokz3jtKcaa+lm+nSwriihTfvMUJYfKCrcaACsjSo4Jm5dTmTzkIhuF2Qh7x4B9UK7X6QDGnT1zbsbvVm9sR8GQwqNMPt+o7v8+xMD+bUaa75MxsKR88rGUY2c/lJRew6BXM2VohhLUkUk/WFUrknOXcYix74Ui0YX7Py8AhzNdGSCY5UgC36L+4w27YzGSgEHb4XLhniYYyG63Vq/XzXt/h7qdTzO9fhmE1BEXURzouCACFSNI7+yC1GmoBdevzq1RO3qtNMSmPQlENSdNRaP7UwksnfsqWen9pjZuotVLskMxXTUGTXMmcoPQ4sHgIezlrysji0k8EpalJLiSHoaadGZw6BIWC4XaCxCQgTGOVBgEpo360BindyXqYN8FxCg6HYqgCGPT7qdYyZ9gvOEAhiLqqqvhw0VBqzF4rclpHdDL2JG+19KHLMz6E+G20YdmjA6xA4z7B3z+siHGm28sHkDPelDSZ6Y2C0VYa0gUFCtgItpemgp5CXdi3xbo8RZtiviKGCkR4FqQajW2pjAKOlqdiwQelxhMyJou4kk3L+qec3kJxkRvoxqqJKh0LgX14NXCS5lGA/ps1+sNyQ4mcwuDPC7IYiPo4Hvbd7fsj7JDNwxw97Mnh0Ke/T2ReuoTgKFJqMbR7NaAzIhk7JCEXVnaIY8YL6sNe3VT7Nq3cwPxX7MpoaCEgNQ1Hb9L+5aIOho+AqS3XqPKkpzqUNdi78ft2/X9s5YPhG1ylRQy+jtOPXll6IqBpQFImRUxeDiOt2S+r987+7zXEmgzvvCq8FLXn0rHV0dF9+AcPGBVYtQfVTYt0z7KYC8d4eZWrnsAlq5LuuaBuqu+Wn683jau1ZtpDUnATHrtT7DN1arE1TrGNYHvPMKdfPW4Jii/z2F1+rpjaOn9SSguGvJa95HnifW4t1iuGleRftUPPVNtiboNIi2bDodb2W4BTrrcXFXoV457BTuoTTilYzPzmSqbRsQGETQ0DXWtWXh0W6UEc7xGnSIhQXRujtprt8KyzAgncJ24S+q+6GTiWuIAdFRa1Wr9dxjAtjHTysOeouGxWHZ+oJQXFXcTF9r8t3VRorZb+d0vkp3hYFFZuGKDqnVk82pihDSNad3Y4It0eTnGKbkwfTa91lmDZKz8bzrRJUuApyIUL4bkcuAJBsZVgTrpSXTy1vuUfDqFNgRvZtoVlHqWSSU121+r7sGhz1JhEGDN9lD7xzZDcY6hZPvWQVQdu/qJwHSK+tHMMEgWGq1yUwZ9hodVIUID9JJ7E+GMmAY6GWTB4hhkMMx/MaDPVADm20U2xbt3c54GHBuTrgk/qT/ckmhj0t8iVDnY8NydDQhh+PEUl+8gW+t/8AJAKGz3vN8JRkGOQvZH7tZMRXXIQ4WCzyIzB7k0weKYYpwVAkaO35CXpzT3/5deG3d+8lyb0s9Qgx5FqKhyB5Cd/W/volvYd4lxIvm00vvJurQxmfaK+u/SFPAwxTvW22MZO0lNhBnK+1X22xuP7yN7ynjmGOjeFNbVKZ35+vF4ucRqskk80MjZ4zfCsZFpz2ay3W3/9RsrM4PcrY8qbJ0nizrFT6F9RWzjHZfFXYl14yehsPx7zsM7G1u0tBpfE9v5NOmXhTFLb5+ScnPjkxMnOJ4bR01jaFtpKH3ZNhTwn27eBuNY0kNgV4HhikdpZoyHn5808kTkzOplkZtDWbfviUayv3O0mBgOEv2Us93nyazRjpcWeXAIldsf79HyZpZ4Yt/gnSC+HEic+XWcYzTM+234K2JrjfaZAUNf4d7z893kDEfulqpckCg9DwfCud5do5O9JET3D8ZGaR2SZoa/ry85C2higW59Kmd+7gVXQSxyAgPqvUQ2bUrJ0maedufoLk5CZjHvrW9G8vG9qaCBj+ker9DSPnyyZ7X6RsTLpO9J2gnQb6zoU/96InSZ7bYXYJ74rm/YG+lUQpdBRb3l7P94DxnIs9VxQdXKQ39+5yoJ2T+/PjHEdmPeaRtlImIFjCt/VfP/x/ttNBbDLTK7+khaH03m2l8W55wnceyE+wPLmMQRJ96++U0/HXupw17aNwf+HFDDjLrXfv379/+naBGx/5zkPhxPk/FylIAsmFt0/hxZ4/zHigB0fhZp9DO6CoXsq27VQWlM1LM3Omje88mOTIrIm3KoTX4i9mmulMr29+KTDDjznRmRdmzk6e+Av8OMlJIJnxxJGUDFse6jU1ieOzjGN+ZvIvkpMcT0zyG4ba5fJsj/e3W3Ds/Mj540NDQ6cAJ46d+Cs4dgwvPjU03Xf8/Mjxo2CAESJEiBAhQoQIESJEiBAhQoQIESJEiBAhQoQIESJEiBAhQoQIESJEiBAhwkfG/wIhDFCOBO80fwAAAABJRU5ErkJggg==" alt="Sample Image 2">
        <div class="vote-count">Votes: <span id="voteCount2">0</span></div>
        <button class="vote-button" onclick="addVote('voteCount2')">Vote</button>
    </div>
    <!-- JavaScript to handle vote counting -->
    <script>
        function addVote(voteId) {
            const voteElement = document.getElementById(voteId);
            let currentVotes = parseInt(voteElement.innerText);
            voteElement.innerText = currentVotes + 1;
        }
    </script>
</body>