---
title: Message ACM_ISPLAYING (commctrl. h)
description: Vérifie si un clip Audio-Video entrelacé (AVI) est lu. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro animer \_ IsPlaying.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- ACM_ISPLAYING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db85d2b25b0f8498c020a78b3e43cfe48877b0cb0b8b77fe33cbb4caa2a3f311
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079413"
---
# <a name="acm_isplaying-message"></a>\_Message ISPLAYING ACM

Vérifie si un clip Audio-Video entrelacé (AVI) est lu. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**animer \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .

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

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





