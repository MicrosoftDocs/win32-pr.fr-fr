---
description: les composants de mise en réseau Microsoft Windows ont été développés pour des performances et une évolutivité.
ms.assetid: 2160b93e-c126-4592-972c-d9cc14eec745
title: Applications de sockets Windows hautes performances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df2b050ac45bf0bf7788a356f4fdba98197d481dd99180f99f7dbf8cdfb5b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927868"
---
# <a name="high-performance-windows-sockets-applications"></a>Applications de sockets Windows hautes performances

les composants de mise en réseau Microsoft Windows ont été développés pour des performances et une évolutivité. Cela permet aux applications d’optimiser la bande passante réseau disponible. Windows les sockets et la Windows pile de protocole TCP/IP ont été optimisés et rationalisés. par conséquent, les applications Windows correctement écrites peuvent obtenir des performances et un débit exceptionnels, comme l’illustrent les informations suivantes :

-   Windows peut traiter des connexions TCP simultanées à 200 000.
-   dans un test effectué par SPECWeb96, Internet Information Server sur Windows desservi par plus de 25 000 requêtes HTTP par seconde.
-   Windows définir un enregistrement de transmission de sur 750Mbps sur un réseau transcontinental gigabit comprenant 10 tronçons.

ces résultats montrent que Windows TCP/IP traite les données très rapidement. toutefois, de nombreuses applications ne tirent pas parti des fonctionnalités de performances de Windows, TCP/IP et Windows sockets, car elles n’implémentent pas sciemment les techniques qui entravent les performances.

Dans ce guide, vous allez apprendre à identifier les erreurs de programmation courantes et à les éviter. vous découvrirez ensuite les techniques qui permettent aux applications de Windows sockets de fonctionner de manière optimale. Ce guide est présenté en six sections. L’ordre des sections est intentionnel ; pour tirer le meilleur parti de ce guide, lisez-le dans l’ordre. Le tableau suivant fournit des liens vers chaque section, ainsi qu’une brève description de chaque rubrique.



| Rubrique                                                                                            | Description                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Terminologie du réseau](network-terminology-2.md)                                                 | Définit la terminologie et les métriques de mise en réseau nécessaires à la compréhension des performances d’une application réseau.                                     |
| [Dimensions de performances](performance-dimensions-2.md)                                           | Décrit les dimensions de performances qui affectent les performances réseau perçues et réelles d’une application.                                        |
| [Caractéristiques de TCP/IP](tcp-ip-characteristics-2.md)                                           | Définit des caractéristiques de protocole TCP/IP qui peuvent entraîner des problèmes de performances pour une application mal écrite.                                     |
| [Comportement de l’application](application-behavior-2.md)                                               | Explique comment reconnaître les signes d’une application réseau peu performante.                                                                     |
| [Amélioration d’une application lente](improving-a-slow-application-2.md)                               | Fournit des exemples de problèmes de conception d’applications qui contribuent à une application peu performante et apporte des modifications au code pour améliorer les performances. |
| [Meilleures pratiques pour les applications interactives](best-practices-for-interactive-applications-2.md) | Répertorie les meilleures pratiques à utiliser pour développer des applications réseau interactives optimales.                                                         |



 

 

 



