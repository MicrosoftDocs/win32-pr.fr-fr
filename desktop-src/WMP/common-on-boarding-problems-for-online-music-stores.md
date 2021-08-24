---
title: problèmes d’intégration courants pour les magasins de Musique en ligne
description: problèmes d’intégration courants pour les magasins de Musique en ligne
ms.assetid: 4210aabb-d1ad-4f98-88e0-941933d77303
keywords:
- Lecteur Windows Media Magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c4cb38f088f463d6bea8ca15b3a92cea9610cc8541f27d55c48df07f9286d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763959"
---
# <a name="common-on-boarding-problems-for-online-music-stores"></a>problèmes d’intégration courants pour les magasins de Musique en ligne

voici une liste des problèmes courants d’intégration de Lecteur Windows Media que vous devez essayer d’éviter. L’un de ces problèmes peut entraîner l’échec du test de validation de votre magasin. Si le test RC2 échoue, le lancement est retardé jusqu’à la prochaine fenêtre de lancement disponible.

1.  Échec de la transition des serveurs de test vers les serveurs de production
    -   Pages manquantes
    -   Paramètres IIS (Access, VRoots, HTTPS ou autres paramètres de sécurité)
    -   Les comptes de test ne fonctionnent plus.
    -   Les comptes de test n’ont pas de crédits appliqués.
    -   Les logos hébergés par le service ne sont pas déplacés.
    -   Les restrictions d’adresse IP qui ont été précédemment contournées ont été effectuées. En particulier, les systèmes de commerce électronique peuvent avoir un ensemble différent de restrictions sur le site musical.
    -   Le document ServiceInfo n’est pas mis à jour pour pointer vers la production.
2.  Le lien d’achat (ou lien d’achat) dans la zone de jeu en cours n’est pas valide. Il s’agit d’un problème souvent négligé, et cela entraînera l’échec de votre magasin, même si tout le reste est en bon état de fonctionnement.
3.  Les testeurs Microsoft doivent disposer d’une puissance d’achat suffisante. L’équipe de validation de Microsoft va exécuter plusieurs scénarios d’achat allant des petits achats à des achats très importants. Vous devez fournir un moyen de refacturation pour qu’ils jouent le rôle de consommateurs dans votre magasin. Cela peut aller de la fourniture d’un grand nombre de comptes à l’aide d’une carte de crédit factice. Par exemple, un magasin échouera en RC2 si un testeur de validation tente d’acheter un album, mais ne dispose que d’un crédit suffisant pour acheter une seule piste.
4.  si vous utilisez des contrôles de ActiveX à l’intérieur de vos pages de service, assurez-vous qu’ils sont installés et désinstallés correctement, tous deux sur toutes les versions applicables de Windows. Dans le cas contraire, il s’agit d’un problème type. souvent, les développeurs et les testeurs d’un magasin en ligne disposent des contrôles de ActiveX inscrits sur leurs propres ordinateurs, mais oublient d’installer les contrôles sur l’ordinateur de l’utilisateur.

    si votre magasin installe un plug-in ou un contrôle de ActiveX, vous devez fournir à l’utilisateur un moyen simple de le désinstaller. par exemple, Microsoft a récemment découvert que certains magasins en ligne étaient installés ActiveX contrôles dans Lecteur Windows Media 11 pour Windows Vista qui n’ont pas pu être supprimés via le menu ajout/suppression de programmes. après quelques investigations, Microsoft a constaté que les contrôles de ActiveX pouvaient être supprimés via le gestionnaire de modules complémentaires d’Internet Explorer. il est important de communiquer (par le biais d’un fichier d’aide, au moins) la façon d’installer et de désinstaller ActiveX contrôles et les plug-ins.

    pour plus d’informations sur l’intégration de votre magasin à l’infrastructure de sécurité dans Windows Vista, consultez l’article intitulé [« meilleures pratiques pour les développeurs et instructions pour les Applications dans un environnement à privilèges minimum »](/previous-versions/aa905330(v=msdn.10)).

 

 