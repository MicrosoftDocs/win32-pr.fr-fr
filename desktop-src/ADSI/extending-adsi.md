---
title: Extension d’ADSI
description: Avec le modèle d’extension ADSI, vous pouvez associer une classe de répertoire à votre propre objet COM.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e597d4b2dd2cf6a3b4a81f1fff3515289418b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671150"
---
# <a name="extending-adsi"></a>Extension d’ADSI

Avec le modèle d’extension ADSI, vous pouvez associer une classe de répertoire à votre propre objet COM. Du point de vue d’un programmeur ou d’un scripteur ADSI, l’extension fait partie intégrante d’ADSI. Par exemple, lorsqu’un nouvel employé rejoint Fabrikam, l’administrateur Windows NT crée un objet utilisateur dans l’annuaire et l’administrateur de la paie doit configurer des entrées dans les systèmes de ressources humaines pour cet utilisateur. Avec une extension ADSI, ce processus peut être rationalisé en un seul script.


```VB
Dim usr
Dim sUserName

On Error Resume Next

sUserName = InputBox ("Enter the name of the user to add:")

Set usr = ou.Create("user", "CN=" & sUserName)

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

// Insert code to set some attributes

usr.SetInfo

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

usr.AddToPayroll  'this is a custom method from an ADSI Extension

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

Debug.Print "User: " & usr.Name & "has been created"
```



Pour plus d’informations, consultez [Extensions ADSI](adsi-extensions.md).

 

 




