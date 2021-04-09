---
title: Exemple de code pour déplacer un objet
description: Cette rubrique contient des exemples de code utilisés pour déplacer un objet dans le domaine.
ms.assetid: 6a54543b-c6e7-486f-afd1-5380e8a8b727
ms.tgt_platform: multiple
keywords:
- Exemple de code pour déplacer un objet AD
- Active Directory exemples Active Directory, déplacement d’un objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800147a4093712d71a56547ba1eabc592b715b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839329"
---
# <a name="example-code-for-moving-an-object"></a><span data-ttu-id="46eae-105">Exemple de code pour déplacer un objet</span><span class="sxs-lookup"><span data-stu-id="46eae-105">Example Code for Moving an Object</span></span>

<span data-ttu-id="46eae-106">Cette rubrique contient des exemples de code utilisés pour déplacer un objet dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="46eae-106">This topic includes code examples used to move an object in the domain.</span></span>

<span data-ttu-id="46eae-107">L’exemple de code C++ suivant montre comment utiliser ADSI pour déplacer un objet dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="46eae-107">The following C++ code example shows how to use ADSI to move an object in the domain.</span></span>


```C++
#include <stdio.h>
#include <atlbase.h>
#include <activeds.h>
#include <ntldap.h>

/***************************************************************************

    MoveObject()

    Moves an object in the directory.

    Parameters:

    padsToMove - Contains an IADs interface pointer that represents the 
    object to move.
    
    padsDestination - Contains an IADs interface pointer that represents the 
    container to move the object to.

***************************************************************************/

HRESULT MoveObject(IADs *padsToMove, IADs *padsDestination)
{
    _ASSERT(padsToMove);
    _ASSERT(padsDestination);
    
    HRESULT hr;
 
    // Get the ADsPath of the object to move.
    CComBSTR sbstrPathToMove;
    hr = padsToMove->get_ADsPath(&sbstrPathToMove); 
    if(FAILED(hr))
    {
        return hr;
    }
    
    // Get an IADsContainer instance from the destination.
    CComPtr<IADsContainer> spContainerDestination;
    hr = padsDestination->QueryInterface(IID_IADsContainer, (void**)&spContainerDestination);
    if(FAILED(hr))
    {
        return hr;
    }

    // Move the object.
    CComPtr<IDispatch> spDispNewObject;
    hr = spContainerDestination->MoveHere(sbstrPathToMove, NULL, &spDispNewObject);

    return hr;
}
```



<span data-ttu-id="46eae-108">L’exemple de code Visual Basic suivant montre comment utiliser ADSI pour déplacer un objet dans le domaine.</span><span class="sxs-lookup"><span data-stu-id="46eae-108">The following Visual Basic code example shows how to use ADSI to move an object in the domain.</span></span>


```VB
''''''''''''''''''''''''''''''''''''''''
'
'   MoveObject
'
'   Moves an object in the directory.
'
'   Parameters:
'
'   DNToMove - Contains the distinguished name of the object to move.
'
'   DNDestination - Contains the distinguished name of the destination
'   container.
'
''''''''''''''''''''''''''''''''''''''''
Public Sub MoveObject(DNToMove As String, DNDestination As String)
    Dim oContainer As IADsContainer
    
    ' Bind to the destination container.
    Set oContainer = GetObject("LDAP://" & DNDestination)
    
    oContainer.MoveHere "LDAP://" & DNToMove, vbNullString
End Sub
```



 

 




