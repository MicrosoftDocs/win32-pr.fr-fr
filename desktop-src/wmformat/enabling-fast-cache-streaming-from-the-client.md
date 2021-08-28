---
title: Activation de la diffusion en continu du cache rapide à partir du client
description: Activation de la diffusion en continu du cache rapide à partir du client
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Windows Media Format SDK, activation de la diffusion en continu du cache rapide
- Windows Media Format SDK, Fast cache streaming
- ASF (Advanced Systems Format), activation de la diffusion en continu du cache rapide
- ASF (format avancé des systèmes), activation de la diffusion en continu du cache rapide
- ASF (Advanced Systems Format), diffusion en continu du cache rapide
- ASF (format de systèmes avancés), diffusion en continu de cache rapide
- flux, activation de la diffusion en continu du cache rapide
- Streaming de cache rapide, activation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0f02a571d5fac456d4dbc743e5fb936f98342a0ed8e8739d653b659ab7c6f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447619"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a>Activation de la diffusion en continu du cache rapide à partir du client

Fast cache est une technologie de diffusion en continu dans laquelle le serveur associer façon opportuniste diffuse du contenu à un débit plus élevé que ce qui est nécessaire pour la lecture.

Si la bande passante disponible est supérieure à la vitesse de transmission du contenu, le cache rapide diffuse à la vitesse supérieure et met en mémoire tampon le contenu. Cela permet de réduire les interruptions ultérieurement si le réseau est encombré. Si la bande passante réseau est inférieure à la vitesse de transmission du contenu, le cache rapide met en mémoire tampon une partie des données avant le démarrage de la lecture. Le cache rapide est recommandé pour les réseaux non fiables, tels que les réseaux sans fil ou les réseaux qui subissent des fluctuations importantes du trafic réseau, telles que les modems câble. Il est également recommandé pour le contenu VBR (variable bit rate). Les exigences en matière de bande passante pour le contenu VBR ne sont pas constantes, et le cache rapide permet au lecteur de mettre le flux en mémoire tampon pendant les parties à débit inférieur.

La diffusion en continu du cache rapide est prise en charge uniquement pour le contenu à la demande. En outre, le serveur doit être configuré pour utiliser la diffusion en continu du cache rapide.

Pour activer Fast cache dans l’objet Reader, appelez les méthodes [**IWMReaderNetworkConfig2 :: SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) et [**IWMReaderNetworkConfig2 :: SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) avec la valeur **true**. La première méthode permet au lecteur de mettre en cache le contenu diffusé en continu. Le deuxième permet d’utiliser rapidement le cache en particulier.

Avec ces paramètres, le lecteur active le cache rapide par défaut si la bande passante réseau est sensiblement supérieure ou inférieure à la vitesse de transmission du contenu, et si le serveur le prend en charge. L’utilisateur peut également contrôler si l’objet lecteur utilise Fast cache en ajoutant un ou plusieurs des modificateurs suivants à l’URL.



| Modificateur         | Description                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMCache          | Si ce modificateur est présent, la valeur « 0 » désactive explicitement le cache rapide, tandis que la valeur « 1 » l’active explicitement.                                                                                                                                                                                                                            |
| WMBitrate        | Ce modificateur spécifie la vitesse de transmission maximale du serveur. Ce modificateur peut être utilisé pour limiter Fast cache à une certaine limite de bande passante. Ce modificateur est ignoré si une bande passante de connexion explicite est déjà définie à l’aide d’un appel à [**IWMReaderNetworkConfig :: SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth). |
| WMContentBitrate | Ce modificateur spécifie la vitesse de transmission du contenu. Le lecteur utilise ce modificateur, s’il est présent, lorsqu’il sélectionne des flux à partir d’un fichier de débit binaire multiple (MBR). Cela peut amener le lecteur à recevoir un contenu à débit élevé sur une connexion lente, ce qui se traduit par des temps de mise en mémoire tampon et des retards très longs.                                          |



 

Le modificateur WMCache = 1 force le lecteur à utiliser la diffusion en continu de cache rapide, quelle que soit la bande passante réseau ou la vitesse de transmission du contenu et quels que soient les appels précédents à **SetEnableFastCache**. Toutefois, elle ne remplace pas le paramètre **SetEnableContentCaching** sur le lecteur ; il ne remplace pas non plus la configuration du serveur.

Les modificateurs d’URL se présentent sous la forme suivante :

*URL*? *modificateur* = *valeur*

Par exemple :

mms://MyServer/MyVideo.wmv ? WMCache = 1

Plusieurs modificateurs peuvent être spécifiés ; Utilisez une esperluette (&) pour les séparer :

mms://MyServer/MyVideo.wmv ? WMCache = 1&WMContentBitrate = 56000

 

 




