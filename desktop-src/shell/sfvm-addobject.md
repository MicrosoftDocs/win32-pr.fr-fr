---
description: Ajoute un objet à la vue de l’interpréteur de commandes. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_ADDOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 441ddac74e1640b2f836686c171d6fc896cbccee2dd6325c31041903ba610b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661059"
---
# <a name="sfvm_addobject-message"></a>\_Message SFVM ADDOBJECT

Ajoute un objet à la vue de l’interpréteur de commandes. Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PIDL* \[ dans\]
</dt> <dd>Pointeur vers l’objet d’intérêt à ajouter.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nouvel ID d’élément ListView de l’objet ajouté si le processus a réussi ; Sinon, retourne-1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




