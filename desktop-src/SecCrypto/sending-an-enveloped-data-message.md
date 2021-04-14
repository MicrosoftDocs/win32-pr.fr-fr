---
description: Dans l’exemple suivant, un message en texte en clair est lu à partir d’un fichier et un magasin de certificats qui contient les certificats des destinataires de messages prévus est ouvert.
ms.assetid: 7ae672d3-e11d-453c-b9c0-354d21830ae4
title: Envoi d’un message de données enveloppées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c04418a2f1d0186ddc0d88c30e7cc790c715b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393632"
---
# <a name="sending-an-enveloped-data-message"></a><span data-ttu-id="c7465-103">Envoi d’un message de données enveloppées</span><span class="sxs-lookup"><span data-stu-id="c7465-103">Sending an Enveloped Data Message</span></span>

<span data-ttu-id="c7465-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c7465-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c7465-105">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c7465-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="c7465-106">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="c7465-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="c7465-107">Dans l’exemple suivant, un message en texte en clair est lu à partir d’un fichier et un magasin de certificats qui contient les certificats des destinataires de messages prévus est ouvert.</span><span class="sxs-lookup"><span data-stu-id="c7465-107">In the following example, a plaintext message is read in from a file, and a certificate store that contains the certificates of the intended message recipients is opened.</span></span> <span data-ttu-id="c7465-108">Tous les certificats du magasin sont ajoutés en tant que destinataires du message, le message est enveloppé et le message enveloppé est écrit dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="c7465-108">All of the certificates in the store are added as recipients of the message, the message is enveloped, and the enveloped message is written to a file.</span></span>

<span data-ttu-id="c7465-109">Du code supplémentaire peut être ajouté pour afficher les certificats ajoutés en tant que destinataires du message, pour vérifier ces certificats avant d’être ajoutés en tant que destinataires prévus, ou pour choisir ceux qui doivent être ajoutés.</span><span class="sxs-lookup"><span data-stu-id="c7465-109">Additional code can be added to display the certificates being added as message recipients, to verify those certificates before they are added as intended recipients, or to otherwise choose those that are to be added.</span></span>

<span data-ttu-id="c7465-110">Sur toute erreur CAPICOM, une valeur décimale négative de **Err. Number** est retournée.</span><span class="sxs-lookup"><span data-stu-id="c7465-110">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="c7465-111">Pour plus d’informations, consultez [**code d' \_ erreur \_ CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="c7465-111">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="c7465-112">Pour plus d’informations sur les valeurs décimales positives de **Err. Number**, consultez winerror. h.</span><span class="sxs-lookup"><span data-stu-id="c7465-112">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


```VB
Sub Envelope(ByVal InFile As String, ByVal OutFile As String, _
             ByVal StoreName As String)

On Error GoTo ErrorHandler

'Open the input file and read the message to be enveloped.

Dim Text As String
Open InFile For Input As #1
Input #1, Text
Close #1
If Len(Text) < 1 Then
    MsgBox "No message to be enveloped."
    Exit Sub
End If

'Open the store containing the certificates of
'the message recipients.

Dim CertStore As New Store
CertStore.Open CAPICOM_CURRENT_USER_STORE, StoreName, _
    CAPICOM_STORE_OPEN_READ_ONLY

' Check for an empty certificate store.

If CertStore.Certificates.Count < 1 Then
    MsgBox "There are no recipient certificates available."
    Set CertStore = Nothing
    Exit Sub
End If

' Declare and initialize an EnvelopedData object

Dim EnvMessage As New EnvelopedData
EnvMessage.Content = Text
Dim I As Integer
For I = 1 To CertStore.Certificates.Count
    EnvMessage.Recipients.Add CertStore.Certificates.Item(I)
    ' The following line can be uncommented to see a prompt
    ' for each certificate in the store.
    ' CertStore.Certificates.Item(I).Display
Next I

'  Set the encryption algorithm and key length. Comment out
'  or remove the following lines to use the default algorithm
'  and key length. The triple DES algorithm and 128 bit key
'  length may not be supported.
Envmessage.Algorithm.Name = ENCRYPTION_ALGORITHM_RC4
Envmessage.Algorithm.KeyLength = KEY_LENGTH_128_BITS

'Declare the string that will hold the enveloped message.

Dim EnvelopedMessage As String

'Encrypt the message into EnvelopedMessage. The enveloped message
'string contains everything that an intended recipient will need to
'decrypt the message, including information on the 
'encryption algorithm key length.
EnvelopedMessage = EnvMessage.Encrypt

' Optionally, check the length of the encrypted string to make sure 
' that the encrypt method worked.

If Len(EnvelopedMessage) < 1 Then
    MsgBox "no message encrypted. "
Else
    MsgBox " Message is " & Len(EnvelopedMessage) & " characters"

    ' Open an output file and write the encrypted message to the 
    ' file. The file is not opened if there is no message to write.
    Open OutFile For Output As #2
    Write #2, EnvelopedMessage
    Close #2
    MsgBox "The message written to file "
End If

' Release the EncryptedData object and the Store object.
Set Envmessage = Nothing
Set CertStore = Nothing

Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found : " & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub
```



 

 



