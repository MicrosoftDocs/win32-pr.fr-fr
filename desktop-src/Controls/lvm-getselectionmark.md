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
ms.openlocfilehash: ed2675550ebc4cf456b439a2e5869068e983f46c82bf6fdde99d8b92806e6cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670977"
---
# <a name="lvm_getselectionmark-message"></a>\_Message GETSELECTIONMARK LVM

Récupère la marque de sélection à partir d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la marque de sélection de base zéro ou-1 s’il n’y a aucune marque de sélection.

## <a name="remarks"></a>Remarques

La *marque de sélection* est l’index d’élément à partir duquel commence une sélection multiple.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETSELECTIONMARK LVM**](lvm-setselectionmark.md)
</dt> </dl>

 

 





