---
title: Message MM_MCINOTIFY (mmsystem. h)
description: Le \_ message mm MCINOTIFY avertit une application qu’un périphérique MCI a terminé une opération. Les appareils MCI envoient ce message uniquement lorsque l' \_ indicateur de notification MCI est utilisé.
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- Message MM_MCINOTIFY Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104710"
---
# <a name="mm_mcinotify-message"></a>MM \_ message MCINOTIFY

Le message **mm \_ MCINOTIFY** avertit une application qu’un périphérique MCI a terminé une opération. Les appareils MCI envoient ce message uniquement lorsque l' \_ indicateur de notification MCI est utilisé.


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Raison de la notification. Les valeurs suivantes sont définies :



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_notification MCI \_ abandonnée    | L’appareil a reçu une commande qui empêchait la satisfaction des conditions actuelles de lancement de la fonction de rappel. Si une nouvelle commande interrompt la commande active et qu’elle demande également une notification, l’appareil envoie ce message uniquement et n’émet pas de notification MCI \_ \_ remplacée |
| échec de la \_ notification MCI \_    | Une erreur d’appareil s’est produite lors de l’exécution de la commande par l’appareil.                                                                                                                                                                                                            |
| \_notification MCI \_ réussie | Les conditions qui initialisent la fonction de rappel ont été remplies.                                                                                                                                                                                                                 |
| \_notification MCI \_ remplacée | L’appareil a reçu une autre commande avec l’indicateur « Notify » défini et les conditions actuelles pour l’initialisation de la fonction de rappel ont été remplacées.                                                                                                                           |



 

</dd> <dt>

<span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*
</dt> <dd>

Identificateur de l’appareil initialisant la fonction de rappel.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="remarks"></a>Notes

Pour plus d’informations sur l' \_ indicateur de notification MCI, consultez [l’indicateur Notify](the-notify-flag.md).

Un appareil retourne l' \_ indicateur MCI Notify \_ réussis avec **mm \_ MCINOTIFY** quand l’action pour une commande se termine. Par exemple, un périphérique CD audio utilise cet indicateur pour la notification de la commande [**Play**](play.md) ( [**\_ lecture MCI**](mci-play.md)) à la fin de la lecture de l’appareil. La commande de **lecture** est réussie uniquement lorsqu’elle atteint la position de fin spécifiée ou atteint la fin du média. De même, les commandes [**Seek**](seek.md) ( [**MCI \_ Seek**](mci-seek.md)) et [**Record**](record.md) ( [**\_ enregistrement MCI**](mci-record.md)) ne retournent pas la \_ notification MCI \_ correctement tant qu’elles n’atteignent pas la position de fin spécifiée ou n’atteignent la fin du support.

Un appareil retourne l' \_ \_ indicateur de notification abandonnée MCI avec **mm \_ MCINOTIFY** uniquement lorsqu’il reçoit une commande qui l’empêche de respecter les conditions de notification. Par exemple, la commande de [**lecture**](play.md) n’interrompt pas la notification pour une commande de **lecture** précédente, à condition que la nouvelle commande ne change pas le sens de lecture ou ne change pas la position de fin. Les commandes [**Seek**](seek.md) et [**Record**](record.md) se comportent de la même façon. En outre, MCI n’envoie \_ pas \_ de notification MCI abandonnée lorsque la lecture ou l’enregistrement est suspendu avec la commande [**Pause**](pause.md) ( [**\_ Pause MCI**](mci-pause.md)). L’envoi de la commande [**Resume**](resume.md) ( [**\_ reprise MCI**](mci-resume.md)) leur permet de continuer à respecter les conditions de rappel.

Lorsque votre application demande une notification pour une commande, vérifiez le retour d’erreur des fonctions [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ou [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Si ces fonctions rencontrent une erreur et retournent une valeur différente de zéro, MCI ne définit pas la notification pour la commande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>MMSYSTEM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Messages MCI](mci-messages.md)
</dt> <dt>

[**suspen**](pause.md)
</dt> <dt>

[**répétition**](play.md)
</dt> <dt>

[**enregistrement**](record.md)
</dt> <dt>

[**sort**](resume.md)
</dt> <dt>

[**Demandez**](seek.md)
</dt> </dl>

 

