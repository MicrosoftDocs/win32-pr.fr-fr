---
description: Récupère un tableau de pointeurs vers des listes d’identificateurs d’élément (PIDL) pour tous les objets sélectionnés. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_GETSELECTEDOBJECTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231210"
---
# <a name="sfvm_getselectedobjects-message"></a>\_Message SFVM GETSELECTEDOBJECTS

Récupère un tableau de pointeurs vers des listes d’identificateurs d’élément (PIDL) pour tous les objets sélectionnés. Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppidl* \[ à\]
</dt> <dd>Adresse d’un tableau de PIDL d’objets actuellement sélectionnés.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne le nombre d’éléments dans le tableau.

## <a name="remarks"></a>Notes

Lorsque vous avez terminé, vous devez appeler [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) sur chaque membre du tableau pour libérer la mémoire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




