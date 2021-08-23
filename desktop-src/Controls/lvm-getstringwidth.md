---
title: Message LVM_GETSTRINGWIDTH (commctrl. h)
description: Détermine la largeur d’une chaîne spécifiée à l’aide de la police actuelle du contrôle List-View spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetStringWidth.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- LVM_GETSTRINGWIDTH les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9024cab94f59e543351e06d49ec058435ae369b6b746b1dc3fb2cd0472e3d57e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019307"
---
# <a name="lvm_getstringwidth-message"></a>\_Message GETSTRINGWIDTH LVM

Détermine la largeur d’une chaîne spécifiée à l’aide de la police actuelle du contrôle List-View spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une chaîne se terminant par null.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la largeur de la chaîne en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Le \_ message GETSTRINGWIDTH LVM retourne la largeur exacte, en pixels, de la chaîne spécifiée. Si vous utilisez la largeur de chaîne retournée comme largeur de colonne dans le message [**\_ SETCOLUMNWIDTH LVM**](lvm-setcolumnwidth.md) , la chaîne sera tronquée. Pour récupérer la largeur de colonne qui peut contenir la chaîne sans la tronquer, vous devez ajouter un remplissage à la largeur de chaîne retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ GETSTRINGWIDTHW** (Unicode) et **LVM \_ GETSTRINGWIDTHA** (ANSI)<br/>     |



 

 





