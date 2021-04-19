---
description: Cette sous-routine prend une chaîne de mot de passe à utiliser pour générer une clé de chiffrement de session, ainsi que le nom d’un fichier à partir duquel un message chiffré sera lu. Tous les paramètres sont passés dans la sous-routine par valeurs.
ms.assetid: 70f23d93-2bca-419b-9de7-e52ce4fb1350
title: Déchiffrement d’un message dans CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba984bad7d9289eaf89725e9598a4330f16b49ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524214"
---
# <a name="decrypting-a-message-in-capicom"></a><span data-ttu-id="9a119-104">Déchiffrement d’un message dans CAPICOM</span><span class="sxs-lookup"><span data-stu-id="9a119-104">Decrypting a Message in CAPICOM</span></span>

<span data-ttu-id="9a119-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9a119-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9a119-106">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9a119-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="9a119-107">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="9a119-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="9a119-108">Cette sous-routine prend une chaîne de mot de passe à utiliser pour générer une clé de chiffrement de session, ainsi que le nom d’un fichier à partir duquel un message chiffré sera lu.</span><span class="sxs-lookup"><span data-stu-id="9a119-108">This subroutine take a password string to be used to generate a session encryption key, and the name of a file from which an encrypted message will be read.</span></span> <span data-ttu-id="9a119-109">Tous les paramètres sont passés dans la sous-routine par valeurs.</span><span class="sxs-lookup"><span data-stu-id="9a119-109">All parameters are passed into the subroutine by values.</span></span>

> [!Note]  
> <span data-ttu-id="9a119-110">CAPICOM ne prend pas en charge le \# type de contenu PKCS 7 EncryptedData, mais utilise une structure ASN non standard pour EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="9a119-110">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for EncryptedData.</span></span> <span data-ttu-id="9a119-111">Par conséquent, seul CAPICOM peut déchiffrer un objet CAPICOM EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="9a119-111">Therefore, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

 

<span data-ttu-id="9a119-112">Si le déchiffrement échoue, la valeur de **Err. Number** est vérifiée pour déterminer si l’erreur a été provoquée par l’utilisation d’un mot de passe qui ne correspondait pas au mot de passe utilisé pour chiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="9a119-112">If decryption fails, the **Err.Number** value is checked to determine whether the error was caused by the use of a password that did not match the password used to encrypt the message.</span></span> <span data-ttu-id="9a119-113">Dans ce cas, l' \_ erreur de données NPD erronées \_ est retournée.</span><span class="sxs-lookup"><span data-stu-id="9a119-113">In this case, the NTE\_BAD\_DATA error is returned.</span></span>

<span data-ttu-id="9a119-114">Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée.</span><span class="sxs-lookup"><span data-stu-id="9a119-114">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="9a119-115">Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="9a119-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="9a119-116">Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="9a119-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


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



 

 



