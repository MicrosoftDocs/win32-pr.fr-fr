---
title: Message LVM_GETITEMSPACING (commctrl. h)
description: Détermine l’espacement entre les éléments d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemSpacing.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- LVM_GETITEMSPACING les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942650"
---
# <a name="lvm_getitemspacing-message"></a>\_Message GETITEMSPACING LVM

Détermine l’espacement entre les éléments d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Vue pour laquelle récupérer l’espacement des éléments. Ce paramètre est **vrai** pour la vue petite icône ou **false** pour la vue icône.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la quantité d’espacement entre les éléments. L’espacement horizontal est contenu dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et l’espacement vertical est contenu dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

