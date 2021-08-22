---
title: Message MCM_GETCALENDARBORDER (commctrl. h)
description: Obtient la taille de la bordure, en pixels. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCurrentView.
ms.assetid: 68366ee1-7511-46a5-aab0-a42fb80c265f
keywords:
- MCM_GETCALENDARBORDER les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_GETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c0755a516334b0e01827c37c6e26ebcfe270bedb2b2b089bb19ea8517aafca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319799"
---
# <a name="mcm_getcalendarborder-message"></a>\_Message GETCALENDARBORDER MCM

Obtient la taille de la bordure, en pixels. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Taille de la bordure, en pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





