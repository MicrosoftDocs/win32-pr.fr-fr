---
description: La quantité maximale de mémoire physique prise en charge par Microsoft Windows est comprise entre 2 Go et 2 to, en fonction de la version de Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Espace d’adressage virtuel et stockage physique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d36445eb2639cbfc4db2a6e4abaf28b9af87cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528888"
---
# <a name="virtual-address-space-and-physical-storage"></a>Espace d’adressage virtuel et stockage physique

La quantité maximale de mémoire physique prise en charge par Microsoft Windows est comprise entre 2 Go et 24 to, en fonction de la version de Windows. Pour plus d’informations, consultez [limites de mémoire pour les versions de Windows](memory-limits-for-windows-releases.md). L’espace d’adressage virtuel de chaque processus peut être plus petit ou plus grand que la mémoire physique totale disponible sur l’ordinateur. Le sous-ensemble de l’espace d’adressage virtuel d’un processus qui réside dans la mémoire physique est appelé la *plage de travail*. Si les threads d’un processus essaient d’utiliser plus de mémoire physique que ce qui est actuellement disponible, le système pagine le contenu de la mémoire sur le disque. La quantité totale d’espace d’adressage virtuel disponible pour un processus est limitée par la mémoire physique et l’espace libre sur le disque disponible pour le fichier d’échange.

Le stockage physique et l’espace d’adressage virtuel de chaque processus sont organisés en *pages*, en unités de mémoire dont la taille dépend de l’ordinateur hôte. Par exemple, sur les ordinateurs x86, la taille de la page hôte est de 4 kilo-octets.

Pour maximiser sa flexibilité dans la gestion de la mémoire, le système peut déplacer des pages de la mémoire physique vers et à partir d’un fichier d’échange sur le disque. Lorsqu’une page est déplacée dans la mémoire physique, le système met à jour les mappages de pages des processus affectés. Lorsque le système a besoin d’espace en mémoire physique, il déplace les pages les moins récemment utilisées de la mémoire physique vers le fichier d’échange. La manipulation de la mémoire physique par le système est totalement transparente pour les applications, qui fonctionnent uniquement dans leurs espaces d’adressage virtuels.

 

 



