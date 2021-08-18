---
description: les ordinateurs personnels exécutant Microsoft Windows avoir souvent de nombreuses connexions réseau, telles que plusieurs cartes d’interface réseau (NIC) connectées à différents réseaux, ou une connexion réseau physique et une connexion d’accès à distance.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Fournisseur d’emplacement réseau (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7378aff6f51f2785671f1d424a4721f9cd77fad22d60554746f9427d7f24f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132092"
---
# <a name="network-location-awareness-service-provider-nla"></a>Fournisseur d’emplacement réseau (NLA)

les ordinateurs personnels exécutant Microsoft Windows avoir souvent de nombreuses connexions réseau, telles que plusieurs cartes d’interface réseau (NIC) connectées à différents réseaux, ou une connexion réseau physique et une connexion d’accès à distance. Windows Les sockets peuvent énumérer des interfaces réseau disponibles pendant un certain temps, mais certaines informations critiques sur les connexions réseau n’étaient pas disponibles auparavant. cela comprend des informations telles que le réseau logique auquel un ordinateur Windows est attaché ou si plusieurs interfaces sont connectées au même réseau.

le fournisseur de service de reconnaissance d’emplacement réseau, communément appelé NLA, permet à Windows applications sockets 2 d’identifier le réseau logique auquel un ordinateur Windows est attaché. en outre, NLA permet aux applications de Windows sockets d’identifier l’interface réseau physique à laquelle une application donnée a enregistré des informations spécifiques. NLA est implémentée en tant que fournisseur de services de résolution de noms Windows sockets 2 génériques.

 

 



