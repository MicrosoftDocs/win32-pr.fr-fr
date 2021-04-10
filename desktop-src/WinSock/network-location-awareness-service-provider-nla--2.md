---
description: Les ordinateurs personnels exécutant Microsoft Windows ont souvent de nombreuses connexions réseau, telles que plusieurs cartes d’interface réseau (NIC) connectées à différents réseaux, ou une connexion réseau physique et une connexion d’accès à distance.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Fournisseur d’emplacement réseau (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113027"
---
# <a name="network-location-awareness-service-provider-nla"></a>Fournisseur d’emplacement réseau (NLA)

Les ordinateurs personnels exécutant Microsoft Windows ont souvent de nombreuses connexions réseau, telles que plusieurs cartes d’interface réseau (NIC) connectées à différents réseaux, ou une connexion réseau physique et une connexion d’accès à distance. Windows Sockets a été en capacité d’énumérer les interfaces réseau disponibles pendant un certain temps, mais certaines informations critiques sur les connexions réseau n’étaient pas disponibles auparavant. Cela comprend des informations telles que le réseau logique auquel un ordinateur Windows est attaché ou si plusieurs interfaces sont connectées au même réseau.

Le fournisseur de service de reconnaissance d’emplacement réseau, communément appelé NLA, permet aux applications Windows Sockets 2 d’identifier le réseau logique auquel un ordinateur Windows est attaché. En outre, NLA permet aux applications Windows Sockets d’identifier l’interface réseau physique à laquelle une application donnée a enregistré des informations spécifiques. NLA est implémentée en tant que fournisseur de services de résolution de noms Windows Sockets 2 générique.

 

 



