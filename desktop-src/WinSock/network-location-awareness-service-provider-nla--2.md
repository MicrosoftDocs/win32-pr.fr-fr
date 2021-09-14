---
description: les ordinateurs personnels exécutant Microsoft Windows avoir souvent de nombreuses connexions réseau, telles que plusieurs cartes d’interface réseau (NIC) connectées à différents réseaux, ou une connexion réseau physique et une connexion d’accès à distance.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Fournisseur d’emplacement réseau (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414521"
---
# <a name="network-location-awareness-service-provider-nla"></a>Fournisseur d’emplacement réseau (NLA)

les ordinateurs personnels exécutant Microsoft Windows avoir souvent de nombreuses connexions réseau, telles que plusieurs cartes d’interface réseau (NIC) connectées à différents réseaux, ou une connexion réseau physique et une connexion d’accès à distance. Windows Les sockets peuvent énumérer des interfaces réseau disponibles pendant un certain temps, mais certaines informations critiques sur les connexions réseau n’étaient pas disponibles auparavant. cela comprend des informations telles que le réseau logique auquel un ordinateur Windows est attaché ou si plusieurs interfaces sont connectées au même réseau.

le fournisseur de service de reconnaissance d’emplacement réseau, communément appelé NLA, permet à Windows applications sockets 2 d’identifier le réseau logique auquel un ordinateur Windows est attaché. en outre, NLA permet aux applications de Windows sockets d’identifier l’interface réseau physique à laquelle une application donnée a enregistré des informations spécifiques. NLA est implémentée en tant que fournisseur de services de résolution de noms Windows sockets 2 génériques.

 

 



