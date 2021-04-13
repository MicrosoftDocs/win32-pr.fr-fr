---
title: Message LVM_GETSTRINGWIDTH (commctrl. h)
description: Détermine la largeur d’une chaîne spécifiée à l’aide de la police actuelle du contrôle List-View spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetStringWidth.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- LVM_GETSTRINGWIDTH les contrôles de message Windows
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
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509158"
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

## <a name="remarks"></a>Notes

Le \_ message GETSTRINGWIDTH LVM retourne la largeur exacte, en pixels, de la chaîne spécifiée. Si vous utilisez la largeur de chaîne retournée comme largeur de colonne dans le message [**\_ SETCOLUMNWIDTH LVM**](lvm-setcolumnwidth.md) , la chaîne sera tronquée. Pour récupérer la largeur de colonne qui peut contenir la chaîne sans la tronquer, vous devez ajouter un remplissage à la largeur de chaîne retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ GETSTRINGWIDTHW** (Unicode) et **LVM \_ GETSTRINGWIDTHA** (ANSI)<br/>     |



 

 





