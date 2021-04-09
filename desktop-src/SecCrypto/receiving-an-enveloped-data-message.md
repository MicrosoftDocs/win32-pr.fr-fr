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
# <a name="receiving-an-enveloped-data-message"></a><span data-ttu-id="ed23e-103">Réception d’un message de données enveloppées</span><span class="sxs-lookup"><span data-stu-id="ed23e-103">Receiving an Enveloped Data Message</span></span>

<span data-ttu-id="ed23e-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ed23e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ed23e-105">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ed23e-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="ed23e-106">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="ed23e-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="ed23e-107">Pour déchiffrer un message enveloppé, le destinataire correspond à un [*certificat*](../secgloss/c-gly.md) du magasin My qui a une clé privée disponible avec un certificat dans le message enveloppé.</span><span class="sxs-lookup"><span data-stu-id="ed23e-107">To decrypt an enveloped message, the recipient matches a [*certificate*](../secgloss/c-gly.md) from the My store that has an available private key with a certificate in the enveloped message.</span></span> <span data-ttu-id="ed23e-108">Si une correspondance est trouvée, la clé chiffrée associée à ce certificat est déchiffrée et cette clé déchiffrée est utilisée pour déchiffrer le message enveloppé.</span><span class="sxs-lookup"><span data-stu-id="ed23e-108">If a match is found, the encrypted key associated with that certificate is decrypted and that decrypted key is used to decrypt the enveloped message.</span></span> <span data-ttu-id="ed23e-109">Un destinataire de message qui n’a pas de certificat correspondant avec une clé privée disponible ne peut pas déchiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="ed23e-109">A message recipient that does not have a matching certificate with an available private key cannot decrypt the message.</span></span>

<span data-ttu-id="ed23e-110">Dans l’exemple qui suit, un nom de fichier est transmis à la sous-routine, ce fichier est ouvert et un message enveloppé est lu dans.</span><span class="sxs-lookup"><span data-stu-id="ed23e-110">In the example that follows, a file name is passed into the subroutine, that file is opened and an enveloped message is read in.</span></span> <span data-ttu-id="ed23e-111">Le message enveloppé est ensuite déchiffré.</span><span class="sxs-lookup"><span data-stu-id="ed23e-111">The enveloped message is then decrypted.</span></span> <span data-ttu-id="ed23e-112">Les étapes de la correspondance d’un certificat utilisateur avec un certificat dans le message enveloppé, du déchiffrement de la clé de chiffrement et enfin du déchiffrement du message sont toutes effectuées en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ed23e-112">The steps of matching a user certificate with a certificate in the enveloped message, of decrypting the encryption key, and finally of decrypting the message are all done behind the scenes.</span></span> <span data-ttu-id="ed23e-113">Une erreur est générée si une correspondance de certificat est introuvable ou si le déchiffrement échoue.</span><span class="sxs-lookup"><span data-stu-id="ed23e-113">An error is raised if a certificate match is not found or if the decryption fails.</span></span>

<span data-ttu-id="ed23e-114">Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée.</span><span class="sxs-lookup"><span data-stu-id="ed23e-114">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="ed23e-115">Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="ed23e-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="ed23e-116">Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="ed23e-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


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



 

 
