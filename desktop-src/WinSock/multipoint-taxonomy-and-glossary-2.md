---
description: La taxonomie décrite ci-dessous distingue d’abord le plan de contrôle qui se rapporte à la façon dont une session multipoint est établie, à partir du plan de données qui gère le transfert de données entre les participants à la session.
ms.assetid: d138347a-826a-4615-afbd-ffa7726a47eb
title: Taxonomie et Glossaire multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5b42690ccd6d4037452d9f4071d9f28d9e2ca9ee5a6ebbd3beca0bc222a7a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097699"
---
# <a name="multipoint-taxonomy-and-glossary"></a>Taxonomie et Glossaire multipoint

La taxonomie décrite ci-dessous distingue d’abord le plan de contrôle qui se rapporte à la façon dont une session multipoint est établie, à partir du plan de données qui gère le transfert de données entre les participants à la session.

Dans le plan de contrôle, il existe deux types distincts d’établissement de session :

-   rooté
-   avec racine

Pour un plan de contrôle enraciné, il existe un participant spécial, appelé \_ racine c, qui est différent du reste des membres de cette session multipoint, chacun d’eux étant appelé \_ feuille c. La \_ racine c doit rester présente pendant toute la durée de la session multipoint, car la session est décomposée en l’absence de la \_ racine c. La \_ racine c initie généralement la session multipoint en configurant la connexion à une \_ feuille c, ou un nombre de \_ feuilles c. La \_ racine c peut ajouter des feuilles c supplémentaires \_ ou (dans certains cas) une feuille c \_ peut joindre la racine c \_ à un moment ultérieur. Vous trouverez des exemples de plan de contrôle enraciné dans ATM et ST-II.

Pour un plan de contrôle sans racine, tous les membres appartenant à une session multipoint sont conservés, autrement dit, aucun participant spécial agissant comme racine c n' \_ existe. chaque \_ feuille c doit s’ajouter à une session multipoint préexistante qui est toujours disponible (comme dans le cas d’une adresse de multidiffusion IP) ou qui a été configurée par le biais d’un mécanisme OOB qui dépasse le cadre de cette discussion (et donc non traitée dans les extensions de sockets Windows proposées). Une autre façon de regarder ce problème est qu’il \_ existe toujours une racine c, mais elle peut être considérée comme étant dans le Cloud réseau plutôt que pour l’un des participants. Étant donné qu’il existe toujours une racine de contrôle, un plan de contrôle qui n’est pas enraciné peut également être considéré comme ayant une racine implicite. Voici des exemples de ce type de schémas multipoint à racine implicite : un pont de téléconférence, le système de multidiffusion IP, une unité de contrôle multipoint (MCU) dans une conférence vidéo H. 320, etc.

Dans le plan de données, il existe également deux types de styles de transfert de données :

-   rooté
-   avec racine

Dans un plan de données enraciné, il existe un participant spécial appelé d \_ root. Le transfert de données se produit uniquement entre la \_ racine d et le reste des membres de cette session multipoint, chacun d’eux étant désigné sous le terme de \_ feuille d. Le trafic peut être unidirectionnel ou bidirectionnel. Les données envoyées à partir de la \_ racine d sont dupliquées (le cas échéant) et remises à chaque \_ feuille d, tandis que les données des feuilles d s’affichent \_ uniquement sur la \_ racine d. Dans le cas d’un plan de données enraciné, aucun trafic n’est autorisé entre les \_ feuilles d. Un exemple de protocole qui utilise un plan de données enraciné est ST-II.

Dans un plan de données non enraciné, tous les participants sont égaux dans le sens où les données qu’ils envoient seront remises à tous les autres participants de la même session multipoint. De même, chaque \_ nœud terminal d peut recevoir des données de toutes les autres \_ feuilles d et, dans certains cas, à partir d’autres nœuds qui ne participent pas également à la session multipoint. \_Il n’existe aucun nœud racine d spécial. IP-multicast est un exemple de protocole qui utilise un plan de données non enraciné.

Notez que la question de la duplication de l’unité de données ou de l’utilisation d’une arborescence unique partagée ou de plusieurs arborescences de chemins d’accès les plus courtes pour la distribution multipoint est un problème de protocole. Par conséquent, ils ne sont pas pertinents pour l’interface que le client utilise pour effectuer des communications multipoint. par conséquent, ces problèmes ne sont pas traités par l’interface de sockets Windows.

Le tableau suivant représente la taxonomie décrite ci-dessus et indique comment les schémas existants s’intègrent à chacune des catégories de contrôle et de plan de données. Notez qu’il n’existe aucun schéma multipoint qui utilise un plan de contrôle non enraciné avec un plan de données enraciné.

| Plan de données           | Exemples de plan de contrôle enracinés | Exemples de plan de contrôle à racine inversée (avec racine implicite) |
|----------------------|-------------------------------|----------------------------------------------------|
| Plan de données enraciné    | ATM, ST-II                    | Aucun exemple connu                                  |
| Plan de données à racine | T. 120                         | IP-multicast, H. 320 (MCU)                          |



 

 

 



