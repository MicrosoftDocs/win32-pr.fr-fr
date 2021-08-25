---
title: Message LVM_GETTOPINDEX (commctrl. h)
description: Récupère l’index de l’élément le plus visible en mode liste ou rapport. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetTopIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- LVM_GETTOPINDEX les contrôles de Windows de message
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
ms.openlocfilehash: 6434aa2c7382a4a4d54fc3a76edd5eb4b70ccae858b8d9fcf41547590a8bc69c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920039"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





