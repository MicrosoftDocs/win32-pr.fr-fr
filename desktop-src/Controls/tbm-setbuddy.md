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
ms.openlocfilehash: ab33e53117933390d7a34ec75a49724003255108
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116410"
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

## <a name="return-value"></a>Valeur de retour

Retourne le handle de la fenêtre précédemment assignée au contrôle à cet emplacement.

## <a name="remarks"></a>Notes

> [!Note]  
> Les contrôles TrackBar prennent en charge jusqu’à deux fenêtres d’amis. Cela peut être utile lorsque vous devez afficher du texte ou des images à chaque extrémité du contrôle.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





