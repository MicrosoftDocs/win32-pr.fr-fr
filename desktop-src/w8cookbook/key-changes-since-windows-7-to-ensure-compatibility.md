---
title: Modifications clés depuis Windows 7 pour garantir la compatibilité
description: Modifications clés depuis Windows 7 pour garantir la compatibilité
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee24b18be55ff498d6c3870f77a32270df68284
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310849"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a>Modifications clés depuis Windows 7 pour garantir la compatibilité

Nous comprenons que la compatibilité est importante pour les développeurs. Les éditeurs de logiciels indépendants et les développeurs veulent garantir que leurs applications s’exécuteront comme prévu sur toutes les versions prises en charge du système d’exploitation Windows. L’investissement des consommateurs et des entreprises est essentiel ici : ils veulent être sûrs que les applications qu’ils ont payées continueront de fonctionner. Nous savons que la compatibilité est le principal critère motivant les décisions d’achat. Les applications bien écrites sur la base des meilleures pratiques aboutiront à une plus grande quantité d’évolution du code lors de la publication d’une nouvelle version de Windows et réduiront la fragmentation : ces applications ont un investissement d’ingénierie réduit pour la maintenance et un délai de mise sur le marché plus rapide.

À l’époque de Windows 7, la compatibilité était une approche extrêmement réactive. Dans Windows 8, nous avons commencé à l’envisager différemment, en travaillant dans Windows pour nous assurer que la compatibilité tenait plus de la conception que d’un ajout ultérieur. Windows 10 est la version du système d’exploitation relevant de la conception la plus compatible à ce jour. Voici quelques moyens clés qui nous ont permis d’atteindre cet objectif :

-   Télémétrie de l’application : cela nous aide à comprendre la popularité de l’application dans l’écosystème Windows pour informer les tests de compatibilité.
-   Partenariats ISV : travaillez directement avec des partenaires externes pour leur fournir des données et résoudre les problèmes rencontrés par nos utilisateurs.
-   Révision de conception, détection amont : partenaire avec des équipes de fonctionnalités pour réduire le nombre de modifications avec rupture dans Windows. La vérification de la compatibilité est l’une des étapes que doivent effectuer nos équipes chargées des fonctionnalités.
-   Contrôle plus étroit des modifications d’API & communication améliorée
-   Boucle de vol et de commentaires : la population Windows Insider reçoit des builds en vol qui contribuent à améliorer notre capacité à trouver des problèmes de compatibilité avant la publication d’une version finale pour les clients. Ce processus de feedback ne révèle pas seulement les bogues : il nous permet également de garantir que nous fournissons à nos clients les fonctionnalités qu’ils souhaitent.

 

 




