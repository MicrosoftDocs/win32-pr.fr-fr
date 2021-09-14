---
title: Message LVM_GETNUMBEROFWORKAREAS (commctrl. h)
description: Récupère le nombre de zones de travail dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetNumberOfWorkAreas.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- LVM_GETNUMBEROFWORKAREAS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999805"
---
# <a name="lvm_getnumberofworkareas-message"></a>\_Message GETNUMBEROFWORKAREAS LVM

Récupère le nombre de zones de travail dans un contrôle List-View. Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une valeur UINT qui reçoit le nombre de zones de travail dans le contrôle List-View. Si la valeur zéro est placée dans cette variable, aucune zone de travail n’est actuellement définie. Cette valeur ne peut pas être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour de ce message n’est pas utilisée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de contrôles List-View](using-list-view-controls.md)
</dt> </dl>

 

 





