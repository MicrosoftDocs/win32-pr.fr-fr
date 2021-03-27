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
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210829"
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

## <a name="remarks"></a>Notes

Si la mise à jour a échoué, l’appelant doit libérer la mémoire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




