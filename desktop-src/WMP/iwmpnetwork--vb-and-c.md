---
title: interface IWMPNetwork (VB et C) (Wmp. h)
description: Fournit des propriétés et des méthodes permettant d’accéder aux statistiques relatives à la qualité d’une connexion réseau, ainsi que de spécifier et de récupérer les paramètres du proxy réseau. L’interface IWMPNetwork expose les propriétés suivantes.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- interface IWMPNetwork (VB et C) Lecteur Windows Media
- Lecteur Windows Media de l’interface IWMPNetwork (VB et C), description
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93110b25bd7d194c4f1d7c213228512fd8bc6000df15b726e3f32a6e6e79a62a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572449"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a>interface IWMPNetwork (VB et C#)

Fournit des propriétés et des méthodes permettant d’accéder aux statistiques relatives à la qualité d’une connexion réseau, ainsi que de spécifier et de récupérer les paramètres du proxy réseau.

L’interface **IWMPNetwork** expose les propriétés suivantes.

## <a name="members"></a>Membres

l’interface **IWMPNetwork (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

l’interface **IWMPNetwork (VB et C#)** possède ces méthodes.



| Méthode                                                                                           | Description                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**getProxyBypassForLocal**](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | Retourne une valeur indiquant si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.<br/> |
| [**getProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | Retourne la liste des exceptions du proxy.<br/>                                                                           |
| [**getProxyName**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | Retourne le nom du serveur proxy utilisé.<br/>                                                            |
| [**getProxyPort**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | Retourne le port du proxy utilisé.<br/>                                                                          |
| [**getProxySettings**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | Retourne des informations sur les paramètres de proxy pour un protocole.<br/>                                                |
| [**setProxyBypassForLocal**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | Spécifie si le serveur proxy est contourné si le serveur d’origine se trouve sur un réseau local.<br/>                  |
| [**setProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | Spécifie la liste des exceptions du proxy.<br/>                                                                         |
| [**setProxyName**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | Spécifie le nom du serveur proxy à utiliser.<br/>                                                              |
| [**setProxyPort**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | Spécifie le port du proxy à utiliser.<br/>                                                                            |
| [**Setproxysettings n'**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | Spécifie les paramètres de proxy pour un protocole.<br/>                                                                |



 

### <a name="properties"></a>Propriétés

l’interface **IWMPNetwork (VB et C#)** a ces propriétés.



| Propriété                                                                                          | Type d’accès           | Description                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [**La**](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | Lecture seule<br/>  | Obtient la bande passante actuelle de l’élément multimédia.<br/>                                     |
| [**DEBIT**](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | Lecture seule<br/>  | Obtient la vitesse de transmission actuelle en cours de réception.<br/>                                         |
| [**bufferingCount**](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | Lecture seule<br/>  | Obtient le nombre de fois où la mise en mémoire tampon s’est produite pendant la lecture.<br/>                      |
| [**bufferingProgress**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | Lecture seule<br/>  | Obtient le pourcentage de la mise en mémoire tampon terminée.<br/>                                       |
| [**bufferingTime**](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | Lecture/écriture<br/> | Obtient ou définit la quantité de temps de mise en mémoire tampon, en millisecondes, avant le début de la lecture.<br/> |
| [**downloadProgress**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | Lecture seule<br/>  | Obtient le pourcentage de téléchargement terminé.<br/>                                     |
| [**encodedFrameRate**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | Lecture seule<br/>  | Obtient la fréquence d’images vidéo spécifiée par l’auteur du contenu.<br/>                        |
| [**Fréquence**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | Lecture seule<br/>  | Obtient la fréquence d’images vidéo actuelle.<br/>                                                |
| [**framesSkipped**](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | Lecture seule<br/>  | Obtient le nombre total de trames ignorées lors de la lecture.<br/>                          |
| [**lostPackets**](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | Lecture seule<br/>  | Obtient le nombre de paquets perdus.<br/>                                                  |
| [**maxBandwidth**](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | Lecture/écriture<br/> | Obtient ou définit la bande passante maximale autorisée.<br/>                                       |
| [**maxBitRate**](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | Lecture seule<br/>  | Obtient la vitesse de transmission vidéo maximale possible.<br/>                                         |
| [**receivedPackets**](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | Lecture seule<br/>  | Obtient le nombre de paquets reçus.<br/>                                              |
| [**receptionQuality**](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | Lecture seule<br/>  | Obtient le pourcentage de paquets qui n’ont pas été perdus au cours des 30 dernières secondes.<br/>                   |
| [**recoveredPackets**](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | Lecture seule<br/>  | Obtient le nombre de paquets récupérés.<br/>                                             |
| [**sourceProtocol**](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | Lecture seule<br/>  | Obtient le protocole source utilisé pour recevoir des données.<br/>                                    |



 

Procurez-vous une interface **IWMPNetwork** à l’aide de la propriété suivante.



| Object                                                                   | Propriété                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Objet AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**réseaux**](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .net et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





