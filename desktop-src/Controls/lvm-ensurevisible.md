---
title: Message LVM_ENSUREVISIBLE (commctrl. h)
description: Garantit qu’un élément de mode liste est entièrement ou partiellement visible, en faisant défiler le contrôle de liste si nécessaire. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView EnsureVisible.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- LVM_ENSUREVISIBLE les contrôles de Windows de message
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
ms.openlocfilehash: baeefaf90f0a4562fb187024b2c6f8676c68fb9d46377a4ced900bda6cfd3dfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920299"
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

## <a name="remarks"></a>Remarques

Le message échoue si le style de fenêtre comprend [**LVS \_ NoScroll**](list-view-window-styles.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





