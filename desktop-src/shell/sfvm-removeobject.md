---
description: Supprime un objet de la vue de l’interpréteur de commandes. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_REMOVEOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973815"
---
# <a name="sfvm_removeobject-message"></a>\_Message SFVM REMOVEOBJECT

Supprime un objet de la vue de l’interpréteur de commandes. Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PIDL* \[ dans\]
</dt> <dd>PIDL de l’objet à supprimer.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de l’élément qui a été supprimé si un élément correspondant au PIDL spécifié a été trouvé ; Sinon, retourne-1.

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




