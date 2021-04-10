---
title: Substitution de protocole
description: Substitution de protocole
ms.assetid: 61db5e2b-4858-446e-9a27-e0305b46683d
keywords:
- Windows Media Format SDK, substitution de protocole
- ASF (Advanced Systems Format), substitution de protocole
- ASF (format de systèmes avancés), substitution de protocole
- substitution de protocole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2de8d0496467535f5740a10082f82e285c11ef6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030808"
---
# <a name="protocol-rollover"></a>Substitution de protocole

La substitution de protocole est un processus dans lequel l’objet lecteur Découvre le meilleur protocole de diffusion en continu disponible sur un serveur. Le lecteur utilise la substitution de protocole chaque fois qu’il ouvre une URL qui contient un schéma « MMS ».

Le lecteur prend en charge plusieurs protocoles :

-   Protocole RTSP (Real Time Streaming Protocol)
-   Hypertext Transfer Protocol (HTTP)
-   Microsoft Media Server (MMS)

Les protocoles RTSP et MMS se présentent sous deux formes, l’un utilisant [*UDP*](wmformat-glossary.md) comme protocole de remise sous-jacent et l’autre utilisant TCP.

L’objet lecteur utilise toujours le protocole TCP pour les commandes de contrôle de lecture, mais il peut utiliser le protocole TCP ou UDP pour la remise du contenu diffusé en continu. Le protocole UDP est préféré pour la distribution de contenu, car il impose une surcharge de bande passante inférieure à celle de TCP. Le protocole TCP garantit un transport fiable via l’utilisation de « circuits virtuels », mais le coût de cette opération signifie que le protocole TCP n’est pas aussi adapté aux flux multimédias numériques, car l’utilisation efficace de la bande passante est plus importante que les paquets perdus occasionnellement.

Quand une URL spécifie « mms:// », le lecteur tente d’utiliser les protocoles suivants pour la remise des données, dans l’ordre suivant :

1.  RTSP (RTSP avec UDP)
2.  RTSPt (RTSP avec TCP)
3.  MMSU (MMS utilisant UDP)
4.  MMST (MMS utilisant TCP)
5.  HTTP

HTTP est un protocole unidirectionnel basé sur TCP. il s’agit du protocole utilisé par les serveurs Web. La diffusion en continu avec HTTP est moins efficace que RTSP. Toutefois, la plupart des pare-feu sont configurés pour accepter les requêtes HTTP, alors qu’ils rejettent généralement d’autres protocoles de diffusion en continu.

Windows Media Services 9 Series dans Microsoft Windows Server 2003 rejette les demandes MMSU ou MMST d’un lecteur SDK Windows Media format, car RTSP est le protocole de diffusion en continu préféré. Windows Media Services version 4,1 et les versions antérieures ne prennent pas en charge RTSP. Dans ce cas, l’objet lecteur revient à MMSU ou HTTP.

La substitution de protocole ne s’applique pas si le schéma d’URL fournit un protocole spécifique, tel que « rtspu:// » pour RTSP ou « https:// » pour HTTP. Si le schéma d’URL est « rtsp:// », le lecteur essaie RTSP et RTSPt, mais pas d’autres.

Une fois que le lecteur a ouvert un fichier, vous pouvez interroger le protocole qu’il utilise en appelant la méthode [**IWMReaderAdvanced2 :: GetProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname) sur le lecteur. Pendant que le contenu est diffusé en continu ou téléchargé, cette méthode retourne le nom dès que le contenu est entièrement mis en cache, la méthode **GetProtocolName** retourne la chaîne « cache ».

Pour récupérer les noms de tous les protocoles Windows Media Server pris en charge par le lecteur, appelez la méthode [**IWMReaderNetworkConfig :: GetSupportedProtocolName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getsupportedprotocolname) sur le lecteur. Vous pouvez désactiver un ou plusieurs des protocoles dans la liste de substitution de protocole du lecteur à l’aide de l’interface **IWMReaderNetworkConfig** . Par exemple, la méthode [**IWMReaderNetworkConfig :: SetEnableTCP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenabletcp) active ou désactive les protocoles TCP, et [**IWMReaderNetworkConfig :: SetEnableUDP**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp) active ou désactive les protocoles basés sur UDP. Ces méthodes s’appliquent uniquement à la substitution de protocole. les protocoles sont toujours disponibles si le schéma d’URL contient un protocole spécifique. Il n’y a généralement aucune raison de désactiver les protocoles utilisés dans la substitution de protocole ; Cela peut dégrader les performances. Toutefois, il peut être utile pour le test.

 

 




