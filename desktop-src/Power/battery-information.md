---
description: Les batteries peuvent fournir de la puissance pour les ordinateurs portables et les ordinateurs qui s’exécutent sur un onduleur.
ms.assetid: 3580b37d-611c-46b4-9300-4943833d6852
title: Informations sur la batterie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f9838a2a95db037b9655f116f07e3cf2e072d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518256"
---
# <a name="battery-information"></a>Informations sur la batterie

Les batteries peuvent fournir de la puissance pour les ordinateurs portables et les ordinateurs qui s’exécutent sur un onduleur. Sur ces ordinateurs, le système d’exploitation fournit des informations sur l’état de la batterie afin que les applications puissent fournir des fonctions utiles à l’utilisateur. (Certains anciens systèmes de batterie non standard et onduleurs ne sont pas pris en charge.)

Notez que cette vue d’ensemble suppose que vous êtes familiarisé avec la [gestion des appareils](/windows/desktop/DevIO/device-management).

Pour obtenir des informations sur l’état de la batterie, utilisez la fonction [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) , qui retourne des informations générales sur toutes les sources d’alimentation du système. Vous devez utiliser **GetSystemPowerStatus** dans la mesure du possible.

Dans certains cas, toutefois, des informations détaillées sur chaque batterie sont nécessaires. À cet effet, chaque unité de batterie expose une interface IOCTL. Les opérations IOCTL suivantes sont effectuées à l’aide de la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) :

<dl>

[**\_ \_ informations sur les requêtes de batterie IOCTL \_**](ioctl-battery-query-information.md)  
[**État de la \_ requête de batterie IOCTL \_ \_**](ioctl-battery-query-status.md)  
[**\_ \_ balise de requête de batterie IOCTL \_**](ioctl-battery-query-tag.md)  
[**\_ \_ informations sur le jeu de batteries IOCTL \_**](ioctl-battery-set-information.md)  
</dl>

Pour utiliser cette interface, une application doit suivre plusieurs étapes. Tout d’abord, il doit utiliser des routines de configuration pour énumérer tous les appareils qui ont une interface de classe de batterie. Notez que ces appareils représentent les ports de la batterie, pas les batteries réelles présentes dans le système. L’application doit ensuite ouvrir un descripteur sur chaque appareil afin de pouvoir utiliser la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) pour envoyer des requêtes à l’appareil, puis acquérir des balises pour toutes les batteries insérées. Une fois ces étapes terminées, l’application peut envoyer des requêtes à chaque périphérique de batterie.

## <a name="battery-tags"></a>Étiquettes de batterie

Étant donné que chaque unité de batterie représente un emplacement dans lequel une batterie peut être insérée, il doit exister un moyen de déterminer à quel moment la batterie est retirée, remplacée, remplacée ou modifiée d’une autre façon. Pour ce faire, une étiquette est affectée à chaque batterie d’un emplacement particulier. Cette balise doit être utilisée pour toutes les requêtes pour obtenir des informations. Si la balise fournie par l’application ne correspond pas à la batterie, la requête échoue, indiquant à l’application que la batterie a changé d’une certaine façon. Pour mener à bien la requête, une nouvelle balise de batterie est nécessaire. Obtenez la balise à l’aide de l’opération de [**\_ \_ \_ balise de requête de batterie IOCTL**](ioctl-battery-query-tag.md) . Si une batterie est présente dans cet emplacement, la balise retournée peut être transmise à l’une des autres IOCTL de la batterie pour exécuter d’autres fonctions. Sur un système à plusieurs batteries, chaque unité de batterie émet des étiquettes de batterie indépendamment, de sorte que la balise de deux appareils distincts peut parfois être identique.

Une modification dans la balise de batterie ne signifie pas nécessairement que la batterie a été retirée, réinsérée ou remplacée. Une nouvelle balise peut être générée si une modification est apportée à une des données qui seraient normalement statiques. Par exemple, lorsqu’une batterie est chargée, la dernière capacité entièrement facturée a peut-être changé. La balise peut également changer si la communication de la batterie a été temporairement perdue ou si une notification incorrecte a été signalée par le BIOS. Sur certains systèmes, la balise de batterie peut être mise à jour chaque fois que l’État AC change. Ce comportement est dû à une caractéristique du système de batterie et n’est pas courant.

Chaque fois que la balise de batterie est mise à jour, la batterie doit être traitée comme s’il s’agissait d’une nouvelle batterie et toutes les données mises en cache doivent être relues. Si une application doit savoir si la même batterie physique est présente, elle doit vérifier la valeur de **BatteryUniqueID** dans la mémoire tampon de sortie [**des \_ \_ \_ informations de requête de batterie IOCTL**](ioctl-battery-query-information.md) lorsqu’elle est appelée avec le niveau d’informations **BatteryUniqueID** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion de l’alimentation](about-power-management.md)
</dt> <dt>

[Énumération des unités de batterie](enumerating-battery-devices.md)
</dt> </dl>

 

 
