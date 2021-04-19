---
description: Cette sous-routine prend une chaîne à chiffrer, une chaîne de mot de passe à utiliser pour générer une clé de chiffrement et le nom d’un fichier dans lequel le message chiffré sera écrit.
ms.assetid: 9ad3199a-bca1-4990-80da-80744e349047
title: Chiffrement d’un message dans CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8039586736c09673644cacc90759e8d5f25b6e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529362"
---
# <a name="encrypting-a-message-in-capicom"></a><span data-ttu-id="a79d7-103">Chiffrement d’un message dans CAPICOM</span><span class="sxs-lookup"><span data-stu-id="a79d7-103">Encrypting a Message in CAPICOM</span></span>

<span data-ttu-id="a79d7-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a79d7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a79d7-105">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a79d7-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="a79d7-106">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="a79d7-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="a79d7-107">Cette sous-routine prend une chaîne à chiffrer, une chaîne de mot de passe à utiliser pour générer une clé de chiffrement et le nom d’un fichier dans lequel le message chiffré sera écrit.</span><span class="sxs-lookup"><span data-stu-id="a79d7-107">This subroutine takes a string to be encrypted, a password string to be used to generate an encryption key, and the name of a file where the encrypted message will be written.</span></span> <span data-ttu-id="a79d7-108">Tous les paramètres sont passés dans la sous-routine par valeurs.</span><span class="sxs-lookup"><span data-stu-id="a79d7-108">All parameters are passed into the subroutine by values.</span></span> <span data-ttu-id="a79d7-109">Pour déchiffrer le message, vous devez utiliser la même chaîne de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a79d7-109">To decrypt the message, the same password string must be used.</span></span> <span data-ttu-id="a79d7-110">Si le mot de passe est perdu, le texte ne peut pas être déchiffré.</span><span class="sxs-lookup"><span data-stu-id="a79d7-110">If the password is lost, the text cannot be decrypted.</span></span> <span data-ttu-id="a79d7-111">La confidentialité du message est perdue si un destinataire involontaire accède au mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a79d7-111">The privacy of the message is lost if an unintended recipient gains access to the password.</span></span>

> [!Note]  
> <span data-ttu-id="a79d7-112">CAPICOM ne prend pas en charge le \# type de contenu PKCS 7 EncryptedData, mais utilise une structure ASN non standard pour EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="a79d7-112">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for EncryptedData.</span></span> <span data-ttu-id="a79d7-113">Par conséquent, seul CAPICOM peut déchiffrer un objet CAPICOM EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="a79d7-113">As a result, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

 

<span data-ttu-id="a79d7-114">Sur toute erreur CAPICOM, une valeur décimale négative de la propriété **Err. Number** est retournée.</span><span class="sxs-lookup"><span data-stu-id="a79d7-114">On any CAPICOM error, a negative decimal value of the **Err.Number** property is returned.</span></span> <span data-ttu-id="a79d7-115">Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="a79d7-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="a79d7-116">Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="a79d7-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


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



 

 



