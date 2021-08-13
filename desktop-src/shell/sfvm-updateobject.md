---
description: Met à jour un objet en passant un pointeur vers un tableau de deux pointeurs vers des listes d’identificateurs d’élément (PIDL). Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_UPDATEOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e3c4ee64583710e84af0d377999c389f6fe1bfa6876bb150789a5fd118f79f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452843"
---
# <a name="sfvm_updateobject-message"></a>\_Message SFVM UPDATEOBJECT

Met à jour un objet en passant un pointeur vers un tableau de deux pointeurs vers des listes d’identificateurs d’élément (PIDL). Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppidl* \[ dans\]
</dt> <dd>

Adresse d’un tableau de deux PIDL. Le premier PIDL est l’ancien PIDL. Le deuxième est une copie de l’ancien PIDL avec des informations mises à jour. Le contrôle de la durée de vie de la copie appartient à la vue après l’achèvement réussi de cet appel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’ID ListView de l’objet mis à jour si la mise à jour a réussi ; Sinon, elle retourne-1.

## <a name="remarks"></a>Remarques

Si la mise à jour a échoué, l’appelant doit libérer la mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




