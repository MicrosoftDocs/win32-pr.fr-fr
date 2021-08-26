---
title: Message LVM_DELETECOLUMN (commctrl. h)
description: Supprime une colonne d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView DeleteColumn.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- LVM_DELETECOLUMN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039ab92028d23a75518237bc6e9723f051f2f6f2de8732e40f2086d027a61873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920319"
---
# <a name="lvm_deletecolumn-message"></a>\_Message DELETECOLUMN LVM

Supprime une colonne d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ DeleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de la colonne à supprimer.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

La suppression de la colonne zéro d’un contrôle List-View est uniquement prise en charge dans ComCtl32.dll version 6 et versions ultérieures. La version 5 prend également en charge la suppression de la colonne zéro, mais uniquement après avoir utilisé [**CCM \_ SETVERSION**](ccm-setversion.md) pour définir la version sur 5 ou version ultérieure. Dans les versions antérieures à la version 5, si vous devez supprimer la colonne zéro, insérez une colonne factice de longueur égale à zéro et supprimez la colonne un et les autres.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





