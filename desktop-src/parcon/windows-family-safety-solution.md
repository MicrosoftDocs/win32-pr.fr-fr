---
description: Windows Solution de sécurité des familles
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Windows Solution de sécurité des familles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc5e5749201fc849e7c9476c97c6fbd3dc5ee5b2d3f26ed3988eb72ac59c1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951649"
---
# <a name="windows-family-safety-solution"></a>Windows Solution de sécurité des familles

Les exigences clés définies par Microsoft pour une solution plus complète sont les suivantes. Notez que la définition de Online est une technologie essentiellement accessible sur Internet, contrairement à un client hors connexion qui est généralement limité au niveau de l’ordinateur.

-   Fournissez une zone unique et facile à trouver dans l’interface utilisateur du système d’exploitation dans laquelle toutes les stratégies de contrôle parental, le contrôle de la surveillance des activités et les données d’activité d’une identité peuvent être facilement découvertes.

-   Prendre en charge la surveillance de l’activité suffisante de l’utilisateur contrôlé pour qu’un parent ou gardien ait une confiance raisonnable dans le cas où des activités à risque peuvent être découvertes. Vous pouvez également reconfigurer la reconfiguration des stratégies de l’utilisateur contrôlé de sorte que les modifications non souhaitées ou non autorisées soient détectables.

-   exposez les fonctionnalités de surveillance de l’activité via des interfaces standard de journalisation des événements Windows Vista et fournissez une solution de la visionneuse. Définissez des événements d’activité standard et fournissez une extensibilité à la génération d’événements personnalisés par les éditeurs de logiciels indépendants.

-   Promouvez que toutes les analyses et restrictions pour un utilisateur sont activées uniquement sur la base d’un abonnement par les parents ou les gardiens. Dans la mesure du possible, les fonctionnalités des restrictions doivent être complètement inactives pour que les utilisateurs non contrôlés réduisent les risques liés à la sécurité et à la compatibilité des applications.

-   Chaque fois que cela est possible, Microsoft s’efforce de ne pas prendre de décisions de valeur par âge ou par d’autres paramètres pour l’utilisateur contrôlé (des tiers peuvent choisir de le faire). Ces décisions sont laissées au parent ou au gardien, souvent influencées par les communautés ou les organisations.

-   Fournissez des implémentations dans le produit pour la surveillance de l’activité hors connexion et des restrictions où peu ou pas d’offres sont disponibles aujourd’hui, où la fonctionnalité de risque de sécurité associée est disponible dans le produit, ou lorsqu’une solution Microsoft fournit des fonctionnalités puissantes et robustes entièrement intégrées à la conception du système d’exploitation.

-   En règle générale, faites en sorte que les applications effectuent leurs propres journaux et restrictions pour un contexte et une expérience d’interface utilisateur optimaux.

    Exception : fournir une surveillance des activités en ligne complète et des restrictions dans les domaines sélectionnés, où l’avantage pour les consommateurs et l’industrie l’emporte sur les coûts.

-   exposez les paramètres d’interface utilisateur et les définitions d’événements d’activité des contrôles parentaux en utilisant des api publiques afin que des tiers puissent interroger l’état, modifier les paramètres et lire les journaux d’activité s’ils s’exécutent avec des privilèges de compte Windows suffisants.

L’objectif principal est de promouvoir la coexistence de solutions de contrôle parental tierces avec la fonctionnalité intégrée et de prendre en charge l’ajout de valeur en intégrant, en étendant ou en fournissant des fonctionnalités alternatives qui conviennent.

 

 



