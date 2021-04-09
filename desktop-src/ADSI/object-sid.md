---
title: SID de l’objet (fournisseur WinNT)
description: L’identificateur de sécurité (SID) de l’utilisateur peut être récupéré à l’aide de l’attribut objectSID. L’objectSID est retourné sous la forme d’un tableau de caractères VARIANT qui forment la chaîne SID.
ms.assetid: 15845e6d-ea30-4d6c-9f35-b2abc1a564ba
ms.tgt_platform: multiple
keywords:
- ADSI Provider ADSI, exemples de gestion des utilisateurs, SID d’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5d47e939770b9584a85e4e628c5c168901fc1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028558"
---
# <a name="object-sid-winnt-provider"></a><span data-ttu-id="f53f6-105">SID de l’objet (fournisseur WinNT)</span><span class="sxs-lookup"><span data-stu-id="f53f6-105">Object SID (WinNT Provider)</span></span>

<span data-ttu-id="f53f6-106">L’identificateur de sécurité (SID) de l’utilisateur peut être récupéré à l’aide de l’attribut **objectSID** .</span><span class="sxs-lookup"><span data-stu-id="f53f6-106">The user security identifier (SID) can be retrieved using the **objectSID** attribute.</span></span> <span data-ttu-id="f53f6-107">L' **objectSID** est retourné sous la forme d’un tableau de caractères **Variant** qui forment la chaîne sid.</span><span class="sxs-lookup"><span data-stu-id="f53f6-107">The **objectSID** is returned as a **VARIANT** array of characters that form the SID string.</span></span>

## <a name="example-code"></a><span data-ttu-id="f53f6-108">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="f53f6-108">Example Code</span></span>


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




