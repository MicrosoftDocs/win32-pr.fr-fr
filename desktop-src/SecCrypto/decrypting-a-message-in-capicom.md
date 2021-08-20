---
description: Cette sous-routine prend une chaîne de mot de passe à utiliser pour générer une clé de chiffrement de session, ainsi que le nom d’un fichier à partir duquel un message chiffré sera lu. Tous les paramètres sont passés dans la sous-routine par valeurs.
ms.assetid: 70f23d93-2bca-419b-9de7-e52ce4fb1350
title: Déchiffrement d’un message dans CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744878378fbe2791e66151e451029be8adde2435b451d540196a1082c4e005f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767757"
---
# <a name="decrypting-a-message-in-capicom"></a>Déchiffrement d’un message dans CAPICOM

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Cette sous-routine prend une chaîne de mot de passe à utiliser pour générer une clé de chiffrement de session, ainsi que le nom d’un fichier à partir duquel un message chiffré sera lu. Tous les paramètres sont passés dans la sous-routine par valeurs.

> [!Note]  
> CAPICOM ne prend pas en charge le \# type de contenu PKCS 7 EncryptedData, mais utilise une structure ASN non standard pour EncryptedData. Par conséquent, seul CAPICOM peut déchiffrer un objet CAPICOM EncryptedData.

 

Si le déchiffrement échoue, la valeur de **Err. Number** est vérifiée pour déterminer si l’erreur a été provoquée par l’utilisation d’un mot de passe qui ne correspondait pas au mot de passe utilisé pour chiffrer le message. Dans ce cas, l' \_ erreur de données NPD erronées \_ est retournée.

Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée. Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md). Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.


```VB
Sub DecryptMessage(ByVal hidden As String, ByVal filename As String)
On Error goto ErrorHandler

'Declare an EncryptedData object

Dim message As New EncryptedData

'Declare a string variable to hold the encrypted message.
Dim encrypted As String

' Open an input file and read in the encrypted message
Open filename For Input As #1
Input #1, encrypted
Close #1

' If a message was read in (the length of the input string is 
' greater than 0), set the password and decrypt the message.
If Len(encrypted) > 0 then
    ' Set the password used to generate the key
    ' used to decrypt the message. If the password
    ' not the same as the password used when the message
    ' was encrypted, decryption will fail.
    ' The algorithm name and key length set in the encrypting
    ' process are automatically used to decrypt the message. 
    message.SetSecret hidden
    message.Decrypt encrypted
    ' Display the decrypted message.
    MsgBox message.Content
else
    msgbox "No encrypted message was read in.
endif

' Release the EncryptedData object and exit the subroutine.
Set message = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
'    Check for a bad password error.
    If Err.Number = -2146893819 Then
        MsgBox "Error. The password may not be correct."
    Else
        MsgBox "CAPICOM error found : " & Err.Number
    End If
End If
End Sub
```



 

 



