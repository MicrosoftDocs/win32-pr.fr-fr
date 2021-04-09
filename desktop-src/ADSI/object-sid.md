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
# <a name="object-sid-winnt-provider"></a>SID de l’objet (fournisseur WinNT)

L’identificateur de sécurité (SID) de l’utilisateur peut être récupéré à l’aide de l’attribut **objectSID** . L' **objectSID** est retourné sous la forme d’un tableau de caractères **Variant** qui forment la chaîne sid.

## <a name="example-code"></a>Exemple de code


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




