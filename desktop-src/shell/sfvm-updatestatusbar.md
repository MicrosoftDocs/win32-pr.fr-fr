---
description: 'Avertit l’objet de rappel que la barre d’État est en cours de mise à jour. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_UPDATESTATUSBAR (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 106782383b90af85dca82e445dfc21f77e0f3def73174da9147aadc988f2694e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883899"
---
# <a name="sfvm_updatestatusbar-message"></a>\_Message SFVM UPDATESTATUSBAR

Avertit l’objet de rappel que la barre d’État est en cours de mise à jour. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fInitialize* \[ dans\]
</dt> <dd>

Valeur **booléenne** qui a la valeur **true** si la barre d’État est en cours d’initialisation.

</dd> </dl>

## <a name="remarks"></a>Remarques

Quand vous recevez cette notification :

-   Renvoyez \_ OK si vous devez gérer la mise à jour.
-   Return MAKE \_ HRESULT (gravité \_ Success, 0, 1) pour que l’objet de la vue du dossier système définisse le texte de la barre d’État.
-   Return E \_ Fail pour que l’objet de la vue du dossier système gère la barre d’État.

Le texte de la barre d’État par défaut est le suivant.



| Statut                      | Texte de la barre d'état                         |
|-----------------------------|-----------------------------------------|
| Aucun élément sélectionné           | « \# \# objets » (dans le dossier)          |
| Un élément sélectionné           | Info-bulle de l’élément, le cas échéant. |
| Plus d’un élément sélectionné | « \# \# objets sélectionnés »                 |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
