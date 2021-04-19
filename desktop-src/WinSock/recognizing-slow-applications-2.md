---
description: Ce guide identifie une application lente en tant qu’application Microsoft Windows avec des performances altérées.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Reconnaître les applications lentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534715"
---
# <a name="recognizing-slow-applications"></a>Reconnaître les applications lentes

Ce guide identifie une application *lente* en tant qu’application Microsoft Windows avec des performances altérées. Une application lente présente un ou plusieurs des symptômes suivants :

-   L’utilisation du processeur et du réseau est faible.

    L’ordinateur semble être en attente d’un événement. Souvent, l’application est en attente sur le réseau.

-   La désactivation de l’algorithme Nagle par le biais de l' \_ option de socket TCP NoDelay augmente les performances.

    Cela indique d’autres problèmes et ne doit pas être considéré comme une solution. La désactivation de l’algorithme Nagle augmente la surcharge du protocole. N’utilisez pas cette méthode comme correctif pour les applications endommagées, mais uniquement en tant qu’indication, l’application a besoin d’autres tâches pour résoudre les problèmes de performances.

-   L’application présente une surcharge élevée.

    Pour calculer la charge de votre application, déterminez la quantité de données que vous souhaitez transférer dans chaque direction. Utilisez ensuite netstat et ajoutez (pour Ethernet) 60 octets pour chaque paquet et 500 octets pour chaque connexion. La meilleure surcharge qui peut être attendue pour la diffusion sur Ethernet est d’environ 6%. Pour une connexion par modem, la meilleure surcharge est d’environ 2%, en raison du fait qu’une liaison PPP utilise la compression d’en-tête. Pour plus d’informations, consultez calcul de la [surcharge avec netstat](calculating-overhead-with-netstat-2.md) .

-   La réponse de l’application est lente lorsque la connexion a un temps RTT important.

    En supposant que l’application n’approche pas de la bande passante de la liaison, un RTT important doit avoir peu ou pas d’effet. Un ralentissement spectaculaire d’un RTT important est un signe clair de traitement sérialisé et de nombreuses petites transactions.

Chaque application doit être testée dans un environnement avec un temps RTT important. Cela révèle la plupart des applications qui subissent des choix de développement médiocres. Ce test peut être effectué dans plusieurs environnements, y compris un réseau local sans fil, un simulateur de délai de liaison ou un réseau satellite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comportement de l’application](application-behavior-2.md)
</dt> <dt>

[Applications Windows Sockets hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[L’algorithme Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



