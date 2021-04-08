---
title: Message LVM_SETSELECTIONMARK (commctrl. h)
description: Définit la marque de sélection dans un contrôle de vue de liste. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView SetSelectionMark.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- LVM_SETSELECTIONMARK les contrôles de message Windows
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
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739933"
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

## <a name="remarks"></a>Notes

La *marque de sélection* est l’index d’élément à partir duquel commence une sélection multiple. Ce message n’affecte pas l’état de sélection de l’élément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETSELECTIONMARK LVM**](lvm-getselectionmark.md)
</dt> </dl>

 

 





