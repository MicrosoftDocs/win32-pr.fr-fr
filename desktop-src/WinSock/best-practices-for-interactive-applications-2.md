---
description: Dans la transformation du code de mise à jour de la cellule de vie, plusieurs recommandations pour l’écriture d’applications réseau hautes performances ont été découvertes.
ms.assetid: 2c5d0610-88b5-437e-acde-214553121380
title: Meilleures pratiques pour les applications interactives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89764cf19de223f4622edd947c8122bc7fe8b11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538641"
---
# <a name="best-practices-for-interactive-applications"></a>Meilleures pratiques pour les applications interactives

Dans la transformation du code de mise à jour de la cellule de vie, plusieurs recommandations pour l’écriture d’applications réseau hautes performances ont été découvertes. Voici quelques stratégies générales à appliquer lors de l’écriture de ces types d’applications :

-   Rendez le flux de données le plus possible, au lieu de passer en bloc.
-   Utilisez quelques transactions de grande taille plutôt que plusieurs petites. Les transactions volumineuses peuvent également être diffusées de façon efficace.
-   Reconnaissez que le réseau est une ressource lente et peu fiable et développez chaque application pour réduire sa dépendance sur le réseau.
-   Utilisez une représentation bien structurée des données sur le réseau. La représentation des données doit être indépendante de l’architecture de l’ordinateur, ne contenir aucun FAT et éventuellement être compressée.
-   Pendant l’initialisation et l’arrêt, ne laissez pas l’utilisateur attendre que le réseau démarre ou s’arrête. L’initialisation associée au réseau peut prendre beaucoup de temps. Séparez le code réseau non critique.
-   Gérer les erreurs en fonction de leur impact. Toutes les erreurs ne sont pas critiques. Implémentez des mécanismes de récupération et fournissez des commentaires utilisateur non intrusifs.
-   Utilisez des appels de procédure distante (RPC) uniquement lorsque cela est approprié. RPC est synchrone sur Windows Me/98 et produit toujours des protocoles de conversation et FAT lorsqu’il est utilisé pour envoyer de petites quantités de données.
-   Mesurez votre charge réseau à l’aide de netstat ; vous serez peut-être surpris de ce que vos mesures révèlent.
-   Testez l’application sur un grand nombre de réseaux, en particulier les réseaux lents ou susceptibles de nuire aux pertes. Les réseaux locaux sans fil, les modems et les réseaux privés virtuels (VPN) sur Internet sont de bons réseaux à tester.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications Windows Sockets hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



