---
description: exemple VBScript (Visual Basic scripting Edition) qui utilise la balise object pour créer une instance de l’objet de contrôle d’inscription de certificat.
ms.assetid: 6e2a230e-81c1-4b63-9ad5-3edfc239ad7c
title: Contrôle d’inscription de certificat instancié dans VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 68de4532e00f95156b0016a55d4ae7b6374936e82ef26ee04cfbf4dc0e4c72c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897310"
---
# <a name="the-certificate-enrollment-control-instantiated-in-vbscript"></a>Contrôle d’inscription de certificat instancié dans VBScript

l’exemple VBScript (Visual Basic scripting Edition) suivant utilise la balise object pour créer une instance de l’objet de contrôle d’inscription de certificat. L’objet est libéré de la mémoire lorsqu’il est hors de portée.


```VB
<HTML>
<HEAD>
<TITLE>VBScript Certificate Enrollment Control Sample
</TITLE>
<OBJECT classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    codebase="xenroll.dll"
    id=Enroll >
</OBJECT>
<BR>
Certificate Enrollment Control Instantiation Sample
<BR>
<BR>

<SCRIPT language="VBScript">
<!--
' Declare a local variable.
Dim varName
' Enable error handling.
On Error Resume Next
' Attempt to use the control, in this case to retrieve a property.
varName = Enroll.MyStoreName
' If above line failed, Err.Number will not be 0.
if ( Err.Number <> 0 ) then
    MsgBox("Error!")
    Err.clear
else
    ' The control property was successfully retrieved,
    ' display the property value.
    varName = "MyStoreName is " & varName
    MsgBox( varName )
end if
-->
</SCRIPT>
<BR>
</HEAD>
</HTML>
```



 

 



