---
title: Message TBM_SETBUDDY (commctrl. h)
description: Assigne une fenêtre comme fenêtre associée pour un contrôle TrackBar. Les fenêtres de l’ami TrackBar s’affichent automatiquement à un emplacement relatif à l’orientation du contrôle (horizontale ou verticale).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- TBM_SETBUDDY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f2586c84740cb2d5e8b1f1aadfb910cd241270d3e18363accf1f166c3c35ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167185"
---
# <a name="tbm_setbuddy-message"></a>\_Message TBM SETBUDDY

Assigne une fenêtre comme fenêtre associée pour un contrôle TrackBar. Les fenêtres de l’ami TrackBar s’affichent automatiquement à un emplacement relatif à l’orientation du contrôle (horizontale ou verticale).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur spécifiant l’emplacement d’affichage de la fenêtre associée. Cette valeur peut être l'une des suivantes :



| Valeur                                                                                                                                | Signification                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**:**</dt> </dl>    | L’ami s’affiche à gauche du TrackBar si le contrôle TrackBar utilise le style de ligne de commande [**tbs \_**](trackbar-control-styles.md) . Si le TrackBar utilise le style [**tbs \_ vert**](trackbar-control-styles.md) , l’ami s’affiche au-dessus du contrôle TrackBar.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**FAUSSES**</dt> </dl> | L’ami s’affiche à droite du TrackBar si le contrôle TrackBar utilise le style de ligne de commande [**tbs \_**](trackbar-control-styles.md) . Si le TrackBar utilise le style [**tbs \_ vert**](trackbar-control-styles.md) , l’ami apparaît sous le contrôle TrackBar.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la fenêtre qui sera définie en tant que Buddy du contrôle TrackBar.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la fenêtre précédemment assignée au contrôle à cet emplacement.

## <a name="remarks"></a>Remarques

> [!Note]  
> Les contrôles TrackBar prennent en charge jusqu’à deux fenêtres d’amis. Cela peut être utile lorsque vous devez afficher du texte ou des images à chaque extrémité du contrôle.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





