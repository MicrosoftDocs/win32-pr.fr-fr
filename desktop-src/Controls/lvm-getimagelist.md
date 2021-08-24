---
title: Message LVM_GETIMAGELIST (commctrl. h)
description: Récupère le handle d’une liste d’images utilisée pour dessiner des éléments de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetImageList.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- LVM_GETIMAGELIST les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339de36c85b4a5d39476a93cde71cbc6db23d1bc08946d3ce2d1ab1b5a4cb926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540809"
---
# <a name="lvm_getimagelist-message"></a>\_Message GETIMAGELIST LVM

Récupère le handle d’une liste d’images utilisée pour dessiner des éléments de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Liste d’images à récupérer. Ce paramètre peut prendre l’une des valeurs suivantes :



| Valeur                                                                                                                                                                     | Signification                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ normal**</dt> </dl>                | Liste d’images avec grandes icônes.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ petit**</dt> </dl>                   | Liste d’images avec petites icônes.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**État de LVSIL \_**</dt> </dl>                   | Liste d’images avec images d’État.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**LVSIL \_ GROUPHEADER**</dt> </dl> | Liste d’images pour l’en-tête de groupe.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la liste d’images spécifiée en cas de réussite, ou **null** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





