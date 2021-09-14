---
title: Message LVM_GETCOLUMNORDERARRAY (commctrl. h)
description: Obtient l’ordre de gauche à droite actuel des colonnes dans un contrôle de vue de liste. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetColumnOrderArray.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- LVM_GETCOLUMNORDERARRAY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999839"
---
# <a name="lvm_getcolumnorderarray-message"></a>\_Message GETCOLUMNORDERARRAY LVM

Obtient l’ordre de gauche à droite actuel des colonnes dans un contrôle de vue de liste. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre de colonnes dans le contrôle d’affichage de liste.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau d’entiers qui reçoit les valeurs d’index des colonnes dans le contrôle de vue de liste. Le tableau doit être suffisamment grand pour contenir les éléments *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

En cas de réussite, retourne une valeur différente de zéro et la mémoire tampon au niveau de *lParam* reçoit l’index de colonne de chaque colonne dans le contrôle dans l’ordre dans lequel elles apparaissent de gauche à droite. Sinon, la valeur de retour est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





