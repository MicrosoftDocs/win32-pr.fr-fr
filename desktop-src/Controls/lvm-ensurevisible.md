---
title: Message LVM_ENSUREVISIBLE (commctrl. h)
description: Garantit qu’un élément de mode liste est entièrement ou partiellement visible, en faisant défiler le contrôle de liste si nécessaire. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView EnsureVisible.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- LVM_ENSUREVISIBLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941677"
---
# <a name="lvm_ensurevisible-message"></a>\_Message ENSUREVISIBLE LVM

Garantit qu’un élément de mode liste est entièrement ou partiellement visible, en faisant défiler le contrôle de liste si nécessaire. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de l’élément de vue de liste.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur qui spécifie si l’élément doit être entièrement visible. Si ce paramètre a la **valeur true**, aucun défilement ne se produit si l’élément est au moins partiellement visible.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Le message échoue si le style de fenêtre comprend [**LVS \_ NoScroll**](list-view-window-styles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





