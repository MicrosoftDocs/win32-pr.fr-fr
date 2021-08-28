---
title: Message LVM_SETIMAGELIST (commctrl. h)
description: Affecte une liste d’images à un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetImageList.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- LVM_SETIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4151f7d6e3736e6fe28faa28bc258fb4f85bfb57622b1ec77c02ed83ea187941
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919959"
---
# <a name="lvm_setimagelist-message"></a>\_Message SETIMAGELIST LVM

Affecte une liste d’images à un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Type de liste d’images. Ce paramètre peut prendre l’une des valeurs suivantes :



| Valeur                                                                                                                                                                     | Signification                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ normal**</dt> </dl>                | Liste d’images avec grandes icônes.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ petit**</dt> </dl>                   | Liste d’images avec petites icônes.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**État de LVSIL \_**</dt> </dl>                   | Liste d’images avec images d’État.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**LVSIL \_ GROUPHEADER**</dt> </dl> | Liste d’images pour l’en-tête de groupe.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la liste d’images à assigner.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la liste d’images précédemment associée au contrôle en cas de réussite, ou **null** dans le cas contraire.

## <a name="remarks"></a>Remarques

La liste d’images actuelle sera détruite quand le contrôle de liste est détruit, sauf si le style [**LVS \_ SHAREIMAGELISTS**](list-view-window-styles.md) est défini. Si vous utilisez ce message pour remplacer une liste d’images par une autre, votre application doit détruire explicitement toutes les listes d’images autres que la liste actuelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





