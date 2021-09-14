---
title: Indicateurs de message de pointeur
description: Valeurs utilisées dans différentes macros de pointeur (consultez macros).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519949"
---
# <a name="pointer-message-flags"></a>Indicateurs de message de pointeur

Valeurs utilisées dans différentes macros de pointeur (consultez [macros](macros.md)).

<dl> <dt>

<span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Indique l’arrivée d’un nouveau pointeur.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Indique que ce pointeur continue à exister. Lorsque cet indicateur n’est pas défini, il indique que le pointeur a quitté la plage de détection.

En règle générale, cet indicateur n’est défini que lorsqu’un pointeur de survol quitte la plage de détection (**POINTER_FLAG_UPDATE** est défini) ou lorsqu’un pointeur en contact avec une surface de la fenêtre quitte la plage de détection (**POINTER_FLAG_UP** est définie).


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Indique que ce pointeur est en contact avec la surface du digitaliseur. Lorsque cet indicateur n’est pas défini, il indique un pointeur de pointage.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Indique une action principale, similaire à un bouton gauche de la souris.

Un pointeur tactile a cet indicateur défini lorsqu’il est en contact avec la surface du digitaliseur.

Un pointeur de stylet a cet indicateur défini lorsqu’il est en contact avec la surface du digitaliseur sans bouton enfoncé.

Cet indicateur est défini pour le pointeur de la souris lorsque le bouton gauche de la souris est enfoncé.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indique une action secondaire, similaire à un bouton droit de la souris.

Un pointeur tactile n’utilise pas cet indicateur.

Un pointeur de stylet a cet indicateur défini lorsqu’il est en contact avec la surface du digitaliseur avec le bouton du stylet du stylet enfoncé.

Cet indicateur est défini pour le pointeur de la souris lorsque le bouton droit de la souris est enfoncé.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Similaire à un bouton de roulette de la souris.

Un pointeur tactile n’utilise pas cet indicateur.

Un pointeur de stylet n’utilise pas cet indicateur.

Cet indicateur est défini pour le pointeur de la souris lorsque le bouton roulette de la souris est enfoncé.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Analogue à un premier bouton étendu de la souris (le bouton XButton1).

Un pointeur tactile n’utilise pas cet indicateur.

Un pointeur de stylet n’utilise pas cet indicateur.

Cet indicateur est défini pour le pointeur de la souris lorsque le bouton de la première souris étendue (le bouton XButton1) est enfoncé.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Similaire à un second bouton de la souris étendue (XButton2).

Un pointeur tactile n’utilise pas cet indicateur.

Un pointeur de stylet n’utilise pas cet indicateur.

Cet indicateur est défini pour le pointeur de la souris lorsque le bouton de la souris (XBUTTON2) est enfoncé.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indique que ce pointeur a été désigné comme pointeur principal. Un pointeur principal est un pointeur unique qui peut effectuer des actions au-delà de celles qui sont disponibles pour les pointeurs non principaux. Par exemple, lorsqu’un pointeur principal effectue un contact avec une surface de fenêtre, il peut fournir à la fenêtre la possibilité de l’activer en lui envoyant un message de WM_POINTERACTIVATE.

Le pointeur principal est identifié à partir de toutes les interactions de l’utilisateur actuel sur le système (souris, toucher, stylet, etc.). Par conséquent, le pointeur principal peut ne pas être associé à votre application. Le premier contact dans une interaction tactile multipoint est défini comme pointeur principal. Une fois qu’un pointeur principal est identifié, tous les contacts doivent être levés avant qu’un nouveau contact puisse être identifié comme pointeur principal. Pour les applications qui ne traitent pas l’entrée de pointeur, seuls les événements du pointeur principal sont promus en événements de souris.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



La confiance est une suggestion de l’appareil source indiquant si le pointeur représente une interaction prévue ou accidentelle, qui est particulièrement pertinente pour les pointeurs de PT_TOUCH où une interaction accidentelle (comme avec la paume de la main) peut déclencher l’entrée. La présence de cet indicateur indique que l’appareil source a une confiance élevée que cette entrée fait partie d’une interaction prévue.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Indique que le pointeur se met anormalement en mode, par exemple lorsque le système reçoit une entrée non valide pour le pointeur ou lorsqu’un appareil avec des pointeurs actifs se met brusquement à part. Si l’application recevant l’entrée est en mesure de le faire, elle doit traiter l’interaction comme non terminée et inverser les effets du pointeur concerné.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

LE bouton XButton1 et XBUTTON2 sont des boutons supplémentaires utilisés sur de nombreux périphériques de souris. Elles retournent les mêmes données que les boutons de la souris standard.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes](constants.md)
</dt> <dt>

[Macros](macros.md)
</dt> </dl>

 

 





