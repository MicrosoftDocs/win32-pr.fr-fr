---
title: Extension d’ADSI
description: Avec le modèle d’extension ADSI, vous pouvez associer une classe de répertoire à votre propre objet COM.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e9f5bd316fc4703cf522e2c5facfd6c32c5236da191668f6ba38ae6a904f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428452"
---
# <a name="extending-adsi"></a>Extension d’ADSI

Avec le modèle d’extension ADSI, vous pouvez associer une classe de répertoire à votre propre objet COM. Du point de vue d’un programmeur ou d’un scripteur ADSI, l’extension fait partie intégrante d’ADSI. Par exemple, lorsqu’un nouvel employé rejoint Fabrikam, le Windows administrateur NT crée un objet utilisateur dans l’annuaire et l’administrateur de la paie devra configurer des entrées dans les systèmes de ressources humaines pour cet utilisateur. Avec une extension ADSI, ce processus peut être rationalisé en un seul script.


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

 

 




