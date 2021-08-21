---
title: Message TBM_GETBUDDY (commctrl. h)
description: Récupère le handle d’une fenêtre associée du contrôle TrackBar à un emplacement donné. L’emplacement spécifié est relatif à l’orientation du contrôle (horizontale ou verticale).
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- TBM_GETBUDDY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e03053981ed16b97d68d5b2f0c77db64062d64fd2df7b5a347e4757736d4844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829613"
---
# <a name="tbm_getbuddy-message"></a>\_Message TBM GETBUDDY

Récupère le handle d’une fenêtre associée du contrôle TrackBar à un emplacement donné. L’emplacement spécifié est relatif à l’orientation du contrôle (horizontale ou verticale).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur indiquant le descripteur de fenêtre associée qui sera récupéré, par emplacement relatif. Cette valeur peut être l'une des suivantes :



| Valeur                                                                                                                                    | Signification                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>VRAI * * * * *</dt> </dl>    | Récupère le handle de l’ami à gauche du TrackBar. Si le contrôle TrackBar utilise le style [**tbs \_ vert**](trackbar-control-styles.md) , le message récupère l’ami au-dessus du TrackBar.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSe * * * * *</dt> </dl> | Récupère le handle de l’ami à droite du TrackBar. Si le contrôle TrackBar utilise le style [**tbs \_ vert**](trackbar-control-styles.md) , le message récupère l’ami sous le TrackBar.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la fenêtre associée à l’emplacement spécifié par *wParam*, ou **null** si aucune fenêtre associée n’existe à cet emplacement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





