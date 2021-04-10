---
description: Exemple de Visual Basic Scripting Edition (VBScript) qui utilise la balise OBJECT pour créer une instance de l’objet de contrôle d’inscription de certificat.
ms.assetid: 6e2a230e-81c1-4b63-9ad5-3edfc239ad7c
title: Contrôle d’inscription de certificat instancié dans VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da14c55a3c9005f820be8f8d60026bc31ac4920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951243"
---
# <a name="the-certificate-enrollment-control-instantiated-in-vbscript"></a><span data-ttu-id="9cadc-103">Contrôle d’inscription de certificat instancié dans VBScript</span><span class="sxs-lookup"><span data-stu-id="9cadc-103">The Certificate Enrollment Control Instantiated in VBScript</span></span>

<span data-ttu-id="9cadc-104">L’exemple de Visual Basic Scripting Edition suivant (VBScript) utilise la balise OBJECT pour créer une instance de l’objet de contrôle d’inscription de certificat.</span><span class="sxs-lookup"><span data-stu-id="9cadc-104">The following Visual Basic Scripting Edition (VBScript) example uses the OBJECT tag to create an instance of the Certificate Enrollment Control object.</span></span> <span data-ttu-id="9cadc-105">L’objet est libéré de la mémoire lorsqu’il est hors de portée.</span><span class="sxs-lookup"><span data-stu-id="9cadc-105">The object is freed from memory when it goes out of scope.</span></span>


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



 

 



