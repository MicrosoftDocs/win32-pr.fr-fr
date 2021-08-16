---
description: Cette sous-routine prend une chaîne à chiffrer, une chaîne de mot de passe à utiliser pour générer une clé de chiffrement et le nom d’un fichier dans lequel le message chiffré sera écrit.
ms.assetid: 9ad3199a-bca1-4990-80da-80744e349047
title: Chiffrement d’un message dans CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3ef531fa75fc4d99a423ffbb6c0edd591caf6b1939f12fea439e7f9fbc80dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766191"
---
# <a name="encrypting-a-message-in-capicom"></a>Chiffrement d’un message dans CAPICOM

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Cette sous-routine prend une chaîne à chiffrer, une chaîne de mot de passe à utiliser pour générer une clé de chiffrement et le nom d’un fichier dans lequel le message chiffré sera écrit. Tous les paramètres sont passés dans la sous-routine par valeurs. Pour déchiffrer le message, vous devez utiliser la même chaîne de mot de passe. Si le mot de passe est perdu, le texte ne peut pas être déchiffré. La confidentialité du message est perdue si un destinataire involontaire accède au mot de passe.

> [!Note]  
> CAPICOM ne prend pas en charge le \# type de contenu PKCS 7 EncryptedData, mais utilise une structure ASN non standard pour EncryptedData. Par conséquent, seul CAPICOM peut déchiffrer un objet CAPICOM EncryptedData.

 

Sur toute erreur CAPICOM, une valeur décimale négative de la propriété **Err. Number** est retournée. Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md). Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.


```VB
Sub EncryptMessage(ByVal TobeEncrypted As String, ByVal hidden _
    As String, ByVal filename As String)

    On Error GoTo ErrorHandler

    ' Declare and initialize an EncryptedData object.
    ' Algorithm.Name and KeyLength do not need to be set.

    Dim message As New EncryptedData
    message.Content = Tobeencrypted
    message.SetSecret(hidden)
    ' Optionally, the encryption algorithm and key length can be set.
    ' If these properties are not set, the default algorithm and key 
    ' length are used.
    ' Information about the algorithm and key length is saved with 
    ' the encrypted string and the individual decrypting the message
    ' does not need to set these properties.

    message.Algorithm.Name = CAPICOM_ENCRYPTION_ALGORITHM_DES

    ' Declare the string that will hold the encrypted message.

    Dim encryptedmessage As String

    ' Encrypt the message storing the result in the encryptedmessage
    ' string.
    encryptedmessage = message.Encrypt

    ' Optionally, check the length of the encrypted string to 
    ' make sure that the encrypt method worked. 

    If Len(encryptedmessage) < 1 Then
        MsgBox("no message encrypted. ")
    Else
        MsgBox(" Message is " & Len(encryptedmessage) & " characters")

        ' Open an output file and write the encrypted message to the
        ' file. The file is not opened if there is no message
        ' to write.
    Open filename For Output As #1
    Write #1, encryptedmessage
    Close #1
        MsgBox("Encrypted message written to file ")
    End If

    ' Release the EncryptedData object.
    message = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 



