---
title: Message LVM_GETTOPINDEX (commctrl. h)
description: Récupère l’index de l’élément le plus visible en mode liste ou rapport. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetTopIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- LVM_GETTOPINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510351"
---
# <a name="lvm_gettopindex-message"></a>\_Message GETTOPINDEX LVM

Récupère l’index de l’élément le plus visible en mode liste ou rapport. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetTopIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’index de l’élément en cas de réussite. Retourne zéro si le contrôle d’affichage de liste est en mode icône ou petite icône, ou si le contrôle de liste est en mode Détails avec les groupes activés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





