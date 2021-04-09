---
description: La taxonomie décrite dans cette section distingue d’abord le plan de contrôle qui se rapporte à la façon dont une session multipoint est établie, à partir du plan de données qui gère le transfert de données entre les participants à la session.
ms.assetid: f411acd7-5e33-4760-8a12-31c2d615426f
title: Taxonomie multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97159312a2e431cb82b73336a13904c6b5ab021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862558"
---
# <a name="multipoint-taxonomy"></a>Taxonomie multipoint

La taxonomie décrite dans cette section distingue d’abord le plan de contrôle qui se rapporte à la façon dont une session multipoint est établie, à partir du plan de données qui gère le transfert de données entre les participants à la session.

## <a name="session-establishment-in-the-control-plane"></a>Établissement de session dans le plan de contrôle

Dans le plan de contrôle, il existe deux types distincts d’établissement de session :

-   rooté
-   avec racine

Dans le cas d’un contrôle associé à une racine, il existe un participant spécial, \_ racine c, qui est différent du reste des membres de cette session multipoint, chacun d’eux étant appelé \_ feuille c. La \_ racine c doit rester présente pendant toute la durée de la session multipoint, car la session est décomposée en l’absence de la \_ racine c. La \_ racine c initie généralement la session multipoint en configurant la connexion à une \_ feuille c, ou un nombre de \_ feuilles c. La \_ racine c peut ajouter des feuilles c supplémentaires \_ ou (dans certains cas) une feuille c \_ peut joindre la racine c \_ à un moment ultérieur. Vous trouverez des exemples de plan de contrôle enraciné dans ATM et ST-II.

Pour un plan de contrôle sans racine, tous les membres appartenant à une session multipoint sont conservés, autrement dit, aucun participant spécial agissant comme racine c n' \_ existe. Chaque \_ feuille c doit s’ajouter à une session multipoint préexistante qui est toujours disponible (comme dans le cas d’une adresse de multidiffusion IP) ou a été configurée via un mécanisme hors bande (OOB) qui est en dehors de l’étendue de la spécification Windows Sockets.

Une autre façon de regarder ce problème est qu’il \_ existe toujours une racine c, mais elle peut être considérée comme étant dans le Cloud réseau plutôt que pour l’un des participants. Étant donné qu’il existe toujours une racine de contrôle, un plan de contrôle qui n’est pas enraciné peut également être considéré comme ayant une racine implicite. Voici des exemples de ce type de schémas multipoint à racine implicite :

-   Un pont de téléconférence.
-   Système de multidiffusion IP.
-   Une unité de contrôle multipoint (MCU) dans une conférence vidéo H. 320.

## <a name="data-transfer-in-the-data-plane"></a>Transfert de données dans le plan de données

Dans le plan de données, il existe deux types de styles de transfert de données :

-   rooté
-   avec racine

Dans un plan de données enraciné, il existe un participant spécial appelé d \_ root. Le transfert de données se produit uniquement entre la \_ racine d et le reste des membres de cette session multipoint, chacun étant désigné sous le terme de \_ feuille d. Le trafic peut être unidirectionnel ou bidirectionnel. Les données envoyées à partir de la \_ racine d sont dupliquées (le cas échéant) et remises à chaque \_ feuille d, tandis que les données des feuilles d sont \_ uniquement dirigées vers la \_ racine d. Dans le cas d’un plan de données enraciné, aucun trafic n’est autorisé entre les \_ feuilles d. Par exemple, un protocole qui est enraciné dans le plan de données est ST-II.

Dans un plan de données non enraciné, tous les participants sont égaux, autrement dit, toutes les données qu’ils envoient sont remises à tous les autres participants de la même session multipoint. De même, chaque \_ nœud terminal peut recevoir des données à partir de toutes les autres \_ feuilles d et, dans certains cas, à partir d’autres nœuds qui ne participent pas à la session multipoint. \_Il n’existe aucun nœud racine d spécial. IP-multicast n’est pas enraciné dans le plan de données.

Notez que la question de l’emplacement où se produit la duplication d’unité de données, ou si une arborescence unique partagée ou plusieurs arborescences de chemins d’accès les plus courtes sont utilisées pour la distribution multipoint, sont des problèmes de protocole et ne sont pas pertinentes pour l’interface que l’application utiliserait pour effectuer des communications multipoint. Par conséquent, ces problèmes ne sont pas traités dans cette annexe ou l’interface Windows Sockets.

Le tableau suivant représente la taxonomie décrite ci-dessus et indique comment les schémas existants s’intègrent à chacune des catégories. Notez qu’il n’existe aucun schéma existant qui utilise un plan de contrôle non enraciné avec un plan de données rootés.

|                      | Plan de contrôle enraciné | Plan de contrôle (avec racine implicite) qui n’a pas de racine |
|----------------------|----------------------|-------------------------------------------|
| Plan de données enraciné    | ATM, ST-II           | Aucun exemple connu.                        |
| Plan de données à racine | T. 120                | IP-multicast, H. 320 (MCU)                 |



 

 

 



