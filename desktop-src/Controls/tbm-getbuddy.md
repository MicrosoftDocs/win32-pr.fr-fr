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
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116481"
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

## <a name="return-value"></a>Valeur de retour

Retourne le handle de la fenêtre associée à l’emplacement spécifié par *wParam*, ou **null** si aucune fenêtre associée n’existe à cet emplacement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





