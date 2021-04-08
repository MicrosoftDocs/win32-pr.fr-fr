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
# <a name="extending-adsi"></a><span data-ttu-id="190f0-103">Extension d’ADSI</span><span class="sxs-lookup"><span data-stu-id="190f0-103">Extending ADSI</span></span>

<span data-ttu-id="190f0-104">Avec le modèle d’extension ADSI, vous pouvez associer une classe de répertoire à votre propre objet COM.</span><span class="sxs-lookup"><span data-stu-id="190f0-104">With the ADSI extension model, you can associate a directory class with your own COM object.</span></span> <span data-ttu-id="190f0-105">Du point de vue d’un programmeur ou d’un scripteur ADSI, l’extension fait partie intégrante d’ADSI.</span><span class="sxs-lookup"><span data-stu-id="190f0-105">From an ADSI programmer or script writer's perspective, the extension becomes an integral part of ADSI.</span></span> <span data-ttu-id="190f0-106">Par exemple, lorsqu’un nouvel employé rejoint Fabrikam, l’administrateur Windows NT crée un objet utilisateur dans l’annuaire et l’administrateur de la paie doit configurer des entrées dans les systèmes de ressources humaines pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="190f0-106">For example, when a new employee joins Fabrikam, the Windows NT administrator will create a user object in the directory and the payroll administrator will need to set up some entries in the human resource systems for this user.</span></span> <span data-ttu-id="190f0-107">Avec une extension ADSI, ce processus peut être rationalisé en un seul script.</span><span class="sxs-lookup"><span data-stu-id="190f0-107">With an ADSI extension, this process can be streamlined into one single script.</span></span>


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



<span data-ttu-id="190f0-108">Pour plus d’informations, consultez [Extensions ADSI](adsi-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="190f0-108">For more information, see [ADSI Extensions](adsi-extensions.md).</span></span>

 

 




