---
title: Modifications importantes entre Direct3D 11 et Direct3D 12
description: Direct3D 12 représente un écart significatif par rapport au modèle de programmation Direct3D 11. Direct3D 12 permet aux applications d’être plus proches du matériel que jamais.
ms.assetid: CE5066C9-7EA6-437D-9EB0-AACFB6CFAD9E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3afc5fe9a451addf1d1f7b9aeddf1f55ca40a22db99134ba71d8195c72ad2b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123832"
---
# <a name="important-changes-from-direct3d-11-to-direct3d-12"></a>Modifications importantes entre Direct3D 11 et Direct3D 12

Direct3D 12 représente un écart significatif par rapport au modèle de programmation Direct3D 11. Direct3D 12 permet aux applications d’être plus proches du matériel que jamais. En étant plus proche du matériel, Direct3D 12 est plus rapide et plus efficace. Toutefois, le compromis de votre application ayant une rapidité et une efficacité accrues avec Direct3D 12 est que vous êtes responsable des tâches supplémentaires que vous étiez avec Direct3D 11.

-   [Synchronisation explicite](#explicit-synchronization)
-   [Gestion de la résidence de la mémoire physique](#physical-memory-residency-management)
-   [Objets d’état de pipeline](#pipeline-state-objects)
-   [Listes de commandes et offres groupées](#command-lists-and-bundles)
-   [Tas et tables de descripteurs](#descriptor-heaps-and-tables)
-   [Portage à partir de Direct3D 11](#porting-from-direct3d-11)
-   [Rubriques connexes](#related-topics)

Direct3D 12 est un retour à la programmation de bas niveau. il vous donne davantage de contrôle sur les éléments graphiques de vos jeux et applications en introduisant ces nouvelles fonctionnalités : les objets pour représenter l’état global du pipeline, les listes de commandes et les offres groupées pour l’envoi de travail, ainsi que les tas et les tables de descripteurs pour l’accès aux ressources.

Votre application a augmenté la vitesse et l’efficacité avec Direct3D 12, mais vous êtes responsable des tâches supplémentaires que vous étiez avec Direct3D 11.

## <a name="explicit-synchronization"></a>Synchronisation explicite

-   Dans Direct3D 12, la synchronisation processeur-GPU est désormais la responsabilité explicite de l’application et n’est plus implicitement effectuée par le runtime, comme c’est le cas dans Direct3D 11. Cela signifie également qu’aucune vérification automatique des risques de pipeline n’est effectuée par Direct3D 12. il s’agit donc de la responsabilité des applications.
-   Dans Direct3D 12, les applications sont responsables du traitement par pipeline des mises à jour des données. Autrement dit, le modèle « mapper/verrouiller-ignorer » dans Direct3D 11 doit être effectué manuellement dans Direct3D 12. Dans Direct3D 11, si le GPU utilise toujours la mémoire tampon quand vous appelez [**ID3D11DeviceContext :: Map**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map) avec [**d3d11 \_ mapper \_ Write \_ ignore**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_map), le runtime retourne un pointeur vers une nouvelle région de mémoire au lieu des anciennes données de mémoire tampon. Cela permet au GPU de continuer à utiliser les anciennes données pendant que l’application place les données dans la nouvelle mémoire tampon. Aucune gestion supplémentaire de la mémoire n’est nécessaire dans l’application. l’ancienne mémoire tampon est réutilisée ou détruite automatiquement lorsque le GPU en a terminé avec celle-ci.
-   Dans Direct3D 12, toutes les mises à jour dynamiques (y compris les mémoires tampons constantes, les mémoires tampons de vertex dynamiques, les textures dynamiques, etc.) sont explicitement contrôlées par l’application. Ces mises à jour dynamiques incluent toutes les délimitations GPU nécessaires ou la mise en mémoire tampon. L’application est chargée de conserver la mémoire disponible jusqu’à ce qu’elle ne soit plus nécessaire.
-   Direct3D 12 utilise le comptage de références de style COM uniquement pour les durées de vie des interfaces (en utilisant le modèle de référence faible de Direct3D lié à la durée de vie de l’appareil). Toutes les durées de vie de la mémoire des ressources et des descriptions sont le seul responsable de l’application à maintenir pour la durée appropriée, et ne sont pas comptés comme des références. Direct3D 11 utilise le décompte de références pour gérer également les durées de vie des dépendances d’interface.

## <a name="physical-memory-residency-management"></a>Gestion de la résidence de la mémoire physique

Une application Direct3D 12 doit empêcher les conditions de concurrence entre plusieurs files d’attente, plusieurs adaptateurs et les threads de l’UC. D3D12 ne synchronise plus le processeur et le GPU, ni ne prend en charge des mécanismes pratiques pour le changement de nom des ressources ou la mise en mémoire tampon multiple. Les délimitations doivent être utilisées pour éviter que plusieurs unités de traitement n’écrivent de la mémoire au-delà d’une autre unité de traitement.

L’application Direct3D 12 doit s’assurer que les données résident dans la mémoire pendant que le GPU les lit. La mémoire utilisée par chaque objet est rendue résidente pendant la création de l’objet. Les applications qui appellent ces méthodes doivent utiliser des délimiteurs pour garantir que le GPU n’accède pas aux objets qui ont été supprimés.

Les barrières de ressources sont un autre type de synchronisation nécessaire, utilisé pour synchroniser des transitions de ressources et de sous-ressources à un niveau très granulaire.

Reportez-vous à [gestion de la mémoire dans Direct3D 12](memory-management.md).

## <a name="pipeline-state-objects"></a>Objets d’état de pipeline

Direct3D 11 permet la manipulation de l’état du pipeline via un grand ensemble d’objets indépendants. Par exemple, l’état de l’assembleur d’entrée, l’état du nuanceur de pixels, l’état du rastériseur et l’état de fusion des sorties peuvent tous être modifiés indépendamment. Cette conception fournit une représentation pratique et relativement générale du pipeline Graphics, mais elle n’utilise pas les fonctionnalités du matériel moderne, principalement parce que les différents États sont souvent interdépendants. Par exemple, de nombreuses GPU associent un nuanceur de pixels et un état de fusion de sortie en une seule représentation matérielle. Toutefois, étant donné que l’API Direct3D 11 permet de définir séparément ces étapes de pipeline, le pilote d’affichage ne peut pas résoudre les problèmes d’état de pipeline tant que l’État n’est pas finalisé, ce qui n’est pas jusqu’à l’heure de création. Ce schéma retarde la configuration de l’état du matériel, ce qui signifie une surcharge supplémentaire et un nombre d’appels de dessin maximum par trame.

Direct3D 12 traite ce schéma en unifiant une grande partie de l’état du pipeline en objets d’état de pipeline immuables (objets PSO), qui sont finalisés lors de la création. Le matériel et les pilotes peuvent ensuite convertir immédiatement l’PSO en un état matériel et des instructions natives pour exécuter le travail GPU. Vous pouvez toujours changer de manière dynamique l’PSO en cours d’utilisation, mais pour ce faire, le matériel doit uniquement copier la quantité minimale d’État précalculé directement dans les registres matériels, plutôt que de calculer l’état du matériel à la volée. En utilisant objets PSO, la surcharge des appels de dessin est considérablement réduite, et beaucoup d’appels de dessin peuvent se produire par trame. Pour plus d’informations sur objets PSO, consultez [gestion de l’état des pipelines graphiques dans Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="command-lists-and-bundles"></a>Listes de commandes et offres groupées

Dans Direct3D 11, toute la soumission de travail s’effectue via le [contexte immédiat](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render), qui représente un flux unique de commandes qui sont dirigées vers le GPU. Pour obtenir une mise à l’échelle multithread, des [contextes différés](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render) sont également disponibles pour les jeux. Les contextes différés dans Direct3D 11 ne sont pas parfaitement mappés sur le matériel, donc relativement peu de travail peut être effectué dans ces derniers.

Direct3D 12 introduit un nouveau modèle d’envoi de travail basé sur des listes de commandes qui contiennent l’intégralité des informations nécessaires à l’exécution d’une charge de travail particulière sur le GPU. Chaque nouvelle liste de commandes contient des informations telles que l’PSO à utiliser, la texture et les ressources de mémoire tampon nécessaires, ainsi que les arguments de tous les appels de dessin. Étant donné que chaque liste de commandes est autonome et n’hérite d’aucun État, le pilote peut précalculer toutes les commandes GPU nécessaires à l’avance et en mode thread libre. Le seul processus en série nécessaire est la soumission finale des listes de commandes au GPU via la file d’attente de commandes.

En plus des listes de commandes, Direct3D 12 introduit également un deuxième niveau de précalcul de travail : *bundles*. À la différence des listes de commandes, qui sont entièrement autonomes et sont généralement construites, soumises une seule fois et ignorées, les offres groupées fournissent une forme d’héritage d’État qui permet la réutilisation. Par exemple, si un jeu souhaite dessiner deux modèles de caractères avec différentes textures, une approche consiste à enregistrer une liste de commandes avec deux ensembles d’appels de dessin identiques. Toutefois, une autre approche consiste à « enregistrer » un bundle qui dessine un modèle à un seul caractère, puis à « lire » le bundle à deux reprises sur la liste des commandes à l’aide de différentes ressources. Dans ce dernier cas, le pilote d’affichage doit uniquement calculer les instructions appropriées une seule fois, et la création de la liste de commandes est essentiellement de deux appels de fonction à faible coût.

Pour plus d’informations sur les listes de commandes et les offres groupées, consultez [soumission de travail dans Direct3D 12](command-queues-and-command-lists.md).

## <a name="descriptor-heaps-and-tables"></a>Tas et tables de descripteurs

La liaison de ressources dans Direct3D 11 est très abstraite et pratique, mais laisse de nombreuses capacités matérielles modernes sous-exploitées. Dans Direct3D 11, les jeux créent des objets de *vue* de ressources, puis lient ces vues à plusieurs *emplacements* à différentes étapes de nuanceur dans le pipeline. À leur tour, les nuanceurs lisent les données à partir de ces emplacements de liaison explicites, qui sont fixes au moment du tracé. Ce modèle signifie que chaque fois qu’un jeu dessine à l’aide de différentes ressources, il doit lier de nouveau des vues différentes à des emplacements différents et appeler à nouveau Draw. Ce cas représente également une surcharge qui peut être éliminée en utilisant pleinement les fonctionnalités matérielles modernes.

Direct3D 12 modifie le modèle de liaison pour qu’il corresponde au matériel moderne et améliore considérablement les performances. Au lieu de demander des vues de ressources autonomes et un mappage explicite aux emplacements, Direct3D 12 fournit un tas de descripteurs dans lequel les jeux créent leurs différents affichages de ressources. Ce schéma fournit un mécanisme permettant au GPU d’écrire directement la description de la ressource matérielle (descripteur) sur la mémoire à l’avance. Pour déclarer les ressources qui doivent être utilisées par le pipeline pour un appel de dessin particulier, les jeux spécifient une ou plusieurs tables de descripteurs qui représentent des sous-plages du tas de descripteur complet. Comme le tas du descripteur a déjà été rempli avec les données de descripteur spécifiques au matériel appropriées, la modification des tables de descripteurs est une opération extrêmement économique.

En plus des performances améliorées offertes par les tas et les tables de descripteurs, Direct3D 12 permet également l’indexation dynamique des ressources dans les nuanceurs, ce qui offre une flexibilité sans précédent et déverrouille les nouvelles techniques de rendu. À titre d’exemple, les moteurs de rendu différé modernes encodent généralement un matériau ou un identificateur d’objet d’un certain type dans la mémoire tampon g intermédiaire. Dans Direct3D 11, ces moteurs doivent être vigilants pour éviter d’utiliser un trop grand nombre de documents, comme le nombre trop important d’une mémoire tampon g peut considérablement ralentir la passe de rendu finale. Avec les ressources indexables de manière dynamique, une scène avec mille documents peut être finalisée tout aussi rapidement qu’une seule avec dix.

Pour plus d’informations sur les tables et les tas de descripteurs, consultez [liaison de ressources](resource-binding.md)et [différences dans le modèle de liaison de Direct3D 11](binding-model.md).

## <a name="porting-from-direct3d-11"></a>Portage à partir de Direct3D 11

Le portage à partir de Direct3D 11 est un processus impliqué, décrit dans [Portage de Direct3D 11 vers Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md). Reportez-vous également à la gamme d’options disponibles dans [utilisation de Direct3D 11, Direct3D 10 et Direct2D](direct3d-12-interop.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comprendre Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 