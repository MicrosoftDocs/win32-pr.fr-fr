---
title: Message LVM_SETSELECTIONMARK (commctrl. h)
description: Définit la marque de sélection dans un contrôle de vue de liste. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetSelectionMark.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- LVM_SETSELECTIONMARK les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c80f1392b5bb8b8ae49eaefb639a60213b5d4a7deaf153b99262bf608a770e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217359"
---
# <a name="lvm_setselectionmark-message"></a>\_Message SETSELECTIONMARK LVM

Définit la marque de sélection dans un contrôle de vue de liste. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ SetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Index de base zéro de la nouvelle marque de sélection. Si la valeur est-1, la marque de sélection est supprimée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la marque de sélection précédente, ou-1 s’il n’y a aucune marque de sélection précédente.

## <a name="remarks"></a>Remarques

La *marque de sélection* est l’index d’élément à partir duquel commence une sélection multiple. Ce message n’affecte pas l’état de sélection de l’élément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETSELECTIONMARK LVM**](lvm-getselectionmark.md)
</dt> </dl>

 

 





