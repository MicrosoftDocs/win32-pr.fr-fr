---
description: La \_ propriété AudioEndpoint de la \_ fonction de désactivation \_ de SysFx spécifie si les effets système sont activés dans le flux en mode partagé qui circule vers ou à partir de l’appareil de point de terminaison audio.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114878"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a>AudioEndpoint de la \_ \_ SysFx de désactivation \_

La propriété AudioEndpoint de la fonction de **\_ \_ désactivation de \_ SysFx** spécifie si les effets système sont activés dans le flux en mode partagé qui circule vers ou à partir de l’appareil de point de terminaison audio.

Les effets système sont implémentés en tant qu’objets de traitement audio (APOs) qui peuvent être insérés dans un flux audio. APOs sont des modules logiciels qui exécutent des fonctions de traitement audio, telles que le contrôle de volume et la conversion de format. La désactivation des effets système pour un appareil de point de terminaison permet au flux associé de traverser l’APOs non modifié.

pour plus d’informations sur les effets système dans Windows vista, consultez les livres blancs intitulés « effets audio personnalisés dans Windows Vista » et « réutilisation des effets de système audio Windows Vista » dans les [Technologies de périphérique audio pour Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) site web.

Cette propriété s’applique uniquement aux effets locaux et aux effets globaux APOs qui ont été installés par le fichier. inf qui a installé la carte audio à laquelle l’appareil de point de terminaison est connecté. En outre, cette propriété affecte uniquement l’appareil de point de terminaison cible. elle n’a aucun effet sur les effets système pour les autres appareils de point de terminaison, même s’ils se connectent au même adaptateur.

Le membre **VT** de la structure **PROPVARIANT** est défini sur **VT \_ UI4**.

Le membre **ulVal** de la structure **PROPVARIANT** est défini sur **Endpoint \_ SYSFX \_ activé** si les effets système sont activés ou sur le **point de terminaison \_ SYSFX \_ désactivé** s’ils sont désactivés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés du point de terminaison audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> </dl>

 

 




