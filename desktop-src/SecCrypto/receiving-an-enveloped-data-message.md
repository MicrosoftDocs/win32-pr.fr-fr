---
description: Pour déchiffrer un message enveloppé, le destinataire correspond à un certificat du magasin My qui a une clé privée disponible avec un certificat dans le message enveloppé.
ms.assetid: 536f9977-102c-4df9-9d07-97b4b434b845
title: Réception d’un message de données enveloppées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d32276193e8fd03904aed1ad626cd3ed241c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868202"
---
# <a name="receiving-an-enveloped-data-message"></a>Réception d’un message de données enveloppées

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Pour déchiffrer un message enveloppé, le destinataire correspond à un [*certificat*](../secgloss/c-gly.md) du magasin My qui a une clé privée disponible avec un certificat dans le message enveloppé. Si une correspondance est trouvée, la clé chiffrée associée à ce certificat est déchiffrée et cette clé déchiffrée est utilisée pour déchiffrer le message enveloppé. Un destinataire de message qui n’a pas de certificat correspondant avec une clé privée disponible ne peut pas déchiffrer le message.

Dans l’exemple qui suit, un nom de fichier est transmis à la sous-routine, ce fichier est ouvert et un message enveloppé est lu dans. Le message enveloppé est ensuite déchiffré. Les étapes de la correspondance d’un certificat utilisateur avec un certificat dans le message enveloppé, du déchiffrement de la clé de chiffrement et enfin du déchiffrement du message sont toutes effectuées en arrière-plan. Une erreur est générée si une correspondance de certificat est introuvable ou si le déchiffrement échoue.

Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée. Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md). Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.


```VB
Sub ReceiveMessage(ByVal InFile As String)
On Error GoTo ErrorHandler

'Declare an EnvelopedData object

Dim Envmessage As New EnvelopedData

'Declare a string variable to hold the encrypted message.

Dim Encrypted As String

' Open an input file and read in the encrypted message
Open InFile For Input As #1
Input #1, Encrypted
Close #1

' If the length of the input string is greater than 0, 
' an encrypted message string is available. Decrypt the message.
' Note: to decrypt the message, a certificate with access to
' a user's private key must be available, and that certificate must
' match one of the certificates in the Recipients collection of 
' certificates.
If Len(Encrypted) > 0 Then
    ' Receive and decrypt the message
    Envmessage.Decrypt encrypted
    
    ' Display the decrypted message.
    MsgBox Envmessage.Content
Else
    MsgBox "No enveloped message was read in."
End If
' Release the EncryptedData object.
Set Envmessage = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub
```



 

 
