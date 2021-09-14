---
title: Message LVM_GETSELECTIONMARK (commctrl. h)
description: Récupère la marque de sélection à partir d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetSelectionMark.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- LVM_GETSELECTIONMARK les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999801"
---
# <a name="lvm_getselectionmark-message"></a>\_Message GETSELECTIONMARK LVM

Récupère la marque de sélection à partir d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la marque de sélection de base zéro ou-1 s’il n’y a aucune marque de sélection.

## <a name="remarks"></a>Notes

La *marque de sélection* est l’index d’élément à partir duquel commence une sélection multiple.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETSELECTIONMARK LVM**](lvm-setselectionmark.md)
</dt> </dl>

 

 





