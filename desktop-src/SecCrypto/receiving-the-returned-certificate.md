---
description: Explique comment une application reçoit un certificat.
ms.assetid: 7f87dcf5-b434-4f63-abcd-6873831d22bc
title: Réception du certificat retourné
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73853250c581e460360f5490defc0c94e76e5be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524445"
---
# <a name="receiving-the-returned-certificate"></a><span data-ttu-id="65675-103">Réception du certificat retourné</span><span class="sxs-lookup"><span data-stu-id="65675-103">Receiving the Returned Certificate</span></span>

<span data-ttu-id="65675-104">Lorsque l’autorité de certification a vérifié les informations d’identité du demandeur et s’est assuré que le demandeur est le propriétaire de la clé privée et que les données sur ce demandeur sont exactes, l’autorité de certification construit un certificat X. 509, le signe, l’empaquette avec les autres certificats nécessaires (tels que le propre certificat de l’autorité de certification) dans un message, puis envoie le message au demandeur.</span><span class="sxs-lookup"><span data-stu-id="65675-104">When the certification authority (CA) has verified the requester's identity information and is satisfied that the requester is the owner of the private key and that the data about that requester is accurate, the CA constructs an X.509 certificate, signs it, packages it with any other needed certificates (such as the CA's own certificate) in a message, and sends the message to the requester.</span></span> <span data-ttu-id="65675-105">Le message peut être un \# message PKCS 7 ou une réponse CMC (les modèles v2 génèrent une réponse CMC).</span><span class="sxs-lookup"><span data-stu-id="65675-105">The message can be a PKCS \#7 message or a CMC response (V2 templates result in a CMC response).</span></span>

<span data-ttu-id="65675-106">L’application réceptrice transmet le message au contrôle d’inscription de certificat.</span><span class="sxs-lookup"><span data-stu-id="65675-106">The receiving application passes the message to the Certificate Enrollment Control.</span></span> <span data-ttu-id="65675-107">Le contrôle d’inscription de certificat ouvre ensuite le message et extrait les certificats.</span><span class="sxs-lookup"><span data-stu-id="65675-107">The Certificate Enrollment Control then opens the message and extracts the certificates.</span></span> <span data-ttu-id="65675-108">L’utilisateur est invité à entrer une boîte de dialogue qui lui demande si l’utilisateur accepte les certificats auto-signés dans le magasin « racine ».</span><span class="sxs-lookup"><span data-stu-id="65675-108">The user is prompted with a dialog box asking whether the user will accept self-signed certificates in the "Root" store.</span></span> <span data-ttu-id="65675-109">Si l’utilisateur accepte le certificat racine, le reste des certificats (à l’exception du certificat du demandeur) est placé dans le magasin « CA ».</span><span class="sxs-lookup"><span data-stu-id="65675-109">If the user accepts the root certificate, the rest of the certificates (except for the requester's certificate) are placed in the "CA" store.</span></span> <span data-ttu-id="65675-110">Le certificat du demandeur est placé dans le magasin de certificats spécifié par le demandeur dans la propriété [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) .</span><span class="sxs-lookup"><span data-stu-id="65675-110">The requester's certificate is placed in the certificate store specified by the requester in the [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) property.</span></span>

<span data-ttu-id="65675-111">L’exemple suivant montre comment utiliser les Visual Basic Scripting Edition (VBScript) et HTML dans une page Web pour recevoir et stocker les certificats renvoyés.</span><span class="sxs-lookup"><span data-stu-id="65675-111">The following example shows how to use the Visual Basic Scripting Edition (VBScript) and HTML in a webpage to receive and store the returned certificates.</span></span>


```VB
<HTML>
<TITLE>Certificate Enrollment Acceptance HTML Page
</TITLE>

<OBJECT  classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    CODEBASE="xenroll.dll"
    id=IControl >
</OBJECT>

<SCRIPT language="VBScript">

<!--

Option Explicit 

'Accept the certificate subroutine.

Sub AcceptCertSub

On Error Resume Next

' Get the issued certificate.
' The following value, "PKCS7", represents the received message. 
' Actually, this value must be supplied through the design of
' the receiving application.
' A possible implementation is as follows: after using 
' ICertRequest.Submit to submit the PKCS #10, call 
' ICertRequest.GetLastStatus to confirm successful certificate 
' creation, and then call ICertRequest.GetCertificate to retrieve 
' the certificate.

document.result.result.value = "PKCS7"

    Call IControl.AcceptPKCS7(document.result.result.value)

    If err.Number = 0 Then
        navigate "..\done.htm"
    Else
        Alert "Error: " & Hex(err)
    End If

    End sub

    ' Decline the certificate sub-routine.
    Sub NoAcceptCertSub
    navigate "..\notdone.htm"
    End sub
-->
</SCRIPT>
</BODY>
</HTML>
```



 

 
