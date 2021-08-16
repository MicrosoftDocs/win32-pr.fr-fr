---
title: Objet réseau
description: L’objet réseau fournit des propriétés et des méthodes permettant d’accéder aux statistiques relatives à la qualité d’une connexion réseau, ainsi que de spécifier et de récupérer les paramètres du proxy réseau.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Lecteur Windows Media d’objets réseau
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bf91c23d6a5c581430b17a370e66027a5f9174d0511a2647fba33834ec6c4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996109"
---
# <a name="network-object"></a>Objet réseau

L’objet **réseau** fournit des propriétés et des méthodes permettant d’accéder aux statistiques relatives à la qualité d’une connexion réseau, ainsi que de spécifier et de récupérer les paramètres du proxy réseau.

L’objet **réseau** prend en charge les propriétés suivantes.



| Propriété                                           | Description                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [La](network-bandwidth.md)                 | Récupère la bande passante actuelle de l’élément multimédia.                                          |
| [DEBIT](network-bitrate.md)                     | Récupère la vitesse de transmission actuelle en cours de réception.                                              |
| [bufferingCount](network-bufferingcount.md)       | Récupère le nombre de fois où la mise en mémoire tampon s’est produite pendant la lecture.                           |
| [bufferingProgress](network-bufferingprogress.md) | Récupère le pourcentage de la mise en mémoire tampon terminée.                                            |
| [bufferingTime](network-bufferingtime.md)         | Spécifie ou récupère la quantité de temps de mise en mémoire tampon, en millisecondes, avant le début de la lecture. |
| [downloadProgress](network-downloadprogress.md)   | Récupère le pourcentage de téléchargement effectué.                                             |
| [encodedFrameRate](network-encodedframerate.md)   | Récupère la fréquence d’images vidéo spécifiée par l’auteur du contenu.                             |
| [Fréquence](network-framerate.md)                 | Récupère la fréquence d’images vidéo actuelle.                                                     |
| [framesSkipped](network-framesskipped.md)         | Récupère le nombre total de trames ignorées lors de la lecture.                               |
| [lostPackets](network-lostpackets.md)             | Récupère le nombre de paquets perdus.                                                       |
| [maxBandwidth](network-maxbandwidth.md)           | Spécifie ou récupère la bande passante maximale autorisée.                                       |
| [maxBitRate](network-maxbitrate.md)               | Récupère la vitesse de transmission vidéo maximale possible.                                              |
| [receivedPackets](network-receivedpackets.md)     | Récupère le nombre de paquets reçus.                                                   |
| [receptionQuality](network-receptionquality.md)   | Récupère le pourcentage de paquets reçus au cours des 30 dernières secondes.                        |
| [recoveredPackets](network-recoveredpackets.md)   | Récupère le nombre de paquets récupérés.                                                  |
| [sourceProtocol](network-sourceprotocol.md)       | Récupère le protocole source utilisé pour recevoir des données.                                         |



 

L’objet **réseau** prend en charge les méthodes suivantes.



| Méthode                                                       | Description                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [getProxyBypassForLocal](network-getproxybypassforlocal.md) | Récupère une valeur qui indique si le serveur proxy doit être ignoré si le serveur d’origine se trouve sur un réseau local. |
| [getProxyExceptionList](network-getproxyexceptionlist.md)   | Récupère la liste des exceptions du proxy.                                                                                  |
| [getProxyName](network-getproxyname.md)                     | Récupère le nom d’un serveur proxy à utiliser.                                                                         |
| [getProxyPort](network-getproxyport.md)                     | Récupère le port du proxy à utiliser.                                                                                     |
| [getProxySettings](network-getproxysettings.md)             | Récupère le paramètre de proxy pour un protocole donné.                                                                    |
| [setProxyBypassForLocal](network-setproxybypassforlocal.md) | Spécifie une valeur qui indique si le serveur proxy doit être ignoré si le serveur d’origine se trouve sur un réseau local. |
| [setProxyExceptionList](network-setproxyexceptionlist.md)   | Spécifie la liste des exceptions du proxy.                                                                                  |
| [setProxyName](network-setproxyname.md)                     | Spécifie le nom d’un serveur proxy à utiliser.                                                                         |
| [setProxyPort](network-setproxyport.md)                     | Spécifie le port du proxy à utiliser.                                                                                     |
| [Setproxysettings n'](network-setproxysettings.md)             | Spécifie le paramètre de proxy pour un protocole donné.                                                                    |



 

L’accès à l’objet **réseau** s’effectue par le biais de la propriété suivante.



| Object                      | Propriété                      |
|-----------------------------|-------------------------------|
| [Lecteur](player-object.md) | [network](player-network.md) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




