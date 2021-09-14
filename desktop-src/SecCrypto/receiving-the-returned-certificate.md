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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416389"
---
# <a name="receiving-the-returned-certificate"></a>Réception du certificat retourné

Lorsque l’autorité de certification a vérifié les informations d’identité du demandeur et s’est assuré que le demandeur est le propriétaire de la clé privée et que les données sur ce demandeur sont exactes, l’autorité de certification construit un certificat X. 509, le signe et l’empaquette avec les autres certificats nécessaires (tels que le propre certificat de l’autorité de certification) dans un message.  et envoie le message au demandeur. Le message peut être un \# message PKCS 7 ou une réponse CMC (les modèles v2 génèrent une réponse CMC).

L’application réceptrice transmet le message au contrôle d’inscription de certificat. Le contrôle d’inscription de certificat ouvre ensuite le message et extrait les certificats. L’utilisateur est invité à entrer une boîte de dialogue qui lui demande si l’utilisateur accepte les certificats auto-signés dans le magasin « racine ». Si l’utilisateur accepte le certificat racine, le reste des certificats (à l’exception du certificat du demandeur) est placé dans le magasin « CA ». Le certificat du demandeur est placé dans le magasin de certificats spécifié par le demandeur dans la propriété [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) .

l’exemple suivant montre comment utiliser le Visual Basic scripting Edition (VBScript) et HTML dans une page web pour recevoir et stocker les certificats renvoyés.


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



 

 
