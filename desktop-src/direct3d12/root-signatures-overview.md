---
title: Vue d’ensemble des signatures racine
description: Une signature racine est configurée par les listes de commandes App et Links pour les ressources requises par les nuanceurs.
ms.assetid: 2E649DA2-6CAC-4C2A-A420-D4EC0DD6EA73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85eb5882e4a893c2933c55281f21c49f2d7d50d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012884"
---
# <a name="root-signatures-overview"></a>Vue d’ensemble des signatures racine

Une signature racine est configurée par les listes de commandes App et Links pour les ressources requises par les nuanceurs. La liste de commandes Graphics comporte à la fois une signature de graphique et une signature racine de calcul. Une liste de commandes Compute aura simplement une signature racine de calcul. Ces signatures racines sont indépendantes les unes des autres.

-   [Paramètres et arguments racine](#root-parameters-and-arguments)
-   [Constantes racine, descripteurs et tables](#root-constants-descriptors-and-tables)
-   [Rubriques connexes](#related-topics)

## <a name="root-parameters-and-arguments"></a>Paramètres et arguments racine

Une **signature racine** est semblable à une signature de fonction API, elle détermine les types de données que les nuanceurs doivent attendre, mais ne définit pas la mémoire ou les données réelles. Un **paramètre racine** est une entrée dans la signature racine. Les valeurs réelles des paramètres racine définis et modifiés au moment de l’exécution sont appelées des **arguments racine**. La modification des arguments racine modifie les données lues par les nuanceurs.

## <a name="root-constants-descriptors-and-tables"></a>Constantes racine, descripteurs et tables

La signature racine peut contenir trois types de paramètres ; les constantes racine (constantes incluses dans les arguments racine), les descripteurs racines (descripteurs inclus dans les arguments racine) et les tables de descripteurs (pointeurs vers une plage de descripteurs dans le tas du descripteur).

Les constantes racine sont des valeurs inline 32 bits qui s’affichent dans le nuanceur en tant que mémoire tampon constante.

Les descripteurs racine Inline doivent contenir des descripteurs dont l’accès est le plus fréquent, bien que soit limité à CBVs et aux tampons UAV ou SRV bruts ou structurés. Un type plus complexe, tel qu’un SRV de texture 2D, ne peut pas être utilisé comme descripteur racine. Les descripteurs racine n’incluent pas de limite de taille, donc il ne peut pas y avoir de contrôle hors limites, contrairement aux descripteurs dans les tas de descripteurs, qui incluent une taille.

Les entrées de table de descripteur dans les signatures racines contiennent le descripteur, le nom de liaison de nuanceur HLSL et l’indicateur de visibilité Reportez-vous au [nuancier Model 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1) pour plus d’informations sur les noms des nuanceurs. Sur un matériel, il peut y avoir un gain de performances par rapport à l’affichage des descripteurs uniquement pour les étapes de nuanceur qui en ont besoin (consultez [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)).

![entrée de table du descripteur racine](images/root-descriptor-table.png)

La disposition de la signature racine est assez flexible, avec certaines contraintes imposées sur un matériel moins performant. Quel que soit le niveau de matériel, les applications doivent toujours essayer de rendre la signature racine aussi petite que nécessaire pour une efficacité maximale. Les applications peuvent être dépourvues de tables de descripteurs dans la signature racine, mais moins de place pour les constantes racine, ou vice versa.

Le contenu de la signature racine (les tables de descripteurs, les constantes racine et les descripteurs racine) auxquels l’application est liée obtient automatiquement une version par le pilote D3D12 chaque fois qu’une partie du contenu change entre des appels Draw (Graphics)/Dispatch (Compute). Par conséquent, chaque trace/distribution obtient un jeu complet unique d’état de signature racine.

Dans l’idéal, il existe des groupes d’objets d’état de pipeline (objets PSO) qui partagent la même signature racine. Une fois qu’une signature racine est définie sur le pipeline, toutes les liaisons qu’elle définit (tables de descripteurs, descripteurs, constantes) peuvent être définies ou modifiées individuellement, y compris l’héritage en bottes.

Une application peut faire son propre compromis entre le nombre de tables de descripteurs qu’elle souhaite que les descripteurs Inline en ligne (qui prennent plus d’espace mais suppriment une indirection) les constantes incluses (qui n’ont aucune indirection) qu’elles souhaitent dans la signature racine. Les applications doivent utiliser la signature racine aussi facilement que possible, en se basant sur la mémoire contrôlée par l’application telle que les tas et les tas de descripteurs qui pointent vers eux pour représenter des données en bloc.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Signatures racine](root-signatures.md)
</dt> </dl>

 

 