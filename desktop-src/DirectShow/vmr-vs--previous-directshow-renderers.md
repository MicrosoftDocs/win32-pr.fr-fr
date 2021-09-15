---
description: VMR et
ms.assetid: 45b3f964-6ec7-48b8-a66e-3c9883e6d780
title: VMR et les convertisseurs de DirectShow précédents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db40f9789a73446cb2dac4ed7033bdb163141bff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238926"
---
# <a name="vmr-vs-previous-directshow-renderers"></a>VMR et les convertisseurs de DirectShow précédents

Avec les anciens filtres, différents convertisseurs seraient nécessaires dans le graphique en fonction de la configuration matérielle.

Le filtre de [convertisseur vidéo](video-renderer-filter.md) a été utilisé pour afficher un flux vidéo unique dans les scénarios de port non vidéo. Il était basé sur la technologie matérielle graphique qui est désormais de plus de cinq ans et sur une version plus ancienne de DirectDraw. Dans certains scénarios, il utilise GDI pour le rendu. Cette opération est effectuée pour économiser des ressources vidéo, qui étaient bien plus limitées il y a cinq ans, ou pour surmonter les limitations de DirectDraw liées à la prise en charge de plusieurs moniteurs. Ni VMR-7, ni le VMR-9 n’utilisent jamais GDI pour le rendu ; VMR-7 est entièrement basé sur DirectDraw 7 et VMR-9 est basé sur Direct3D 9.

dans les scénarios impliquant un port vidéo ou plusieurs flux d’entrée vidéo, avant VMR, le filtre de [Mixer de superposition](overlay-mixer-filter.md) a été utilisé pour le rendu. Ce filtre utilise uniquement la superposition matérielle sur la carte graphique. il est donc généralement limité à la surface de superposition fournie par la plupart des cartes. la superposition Mixer effectue le masquage des couleurs de destination, mais il n’est pas possible de procéder à une fusion alpha. Comme il n’a pas de gestionnaire de fenêtres, il doit utiliser un second filtre, le convertisseur vidéo, pour la gestion des fenêtres. VMR est capable d’effectuer une véritable fusion alpha et peut créer plusieurs superpositions dans le logiciel en plus des superpositions matérielles.

Dans les scénarios de port vidéo où les applications superposent des sous-titres ou d’autres données VBI sur la vidéo, un filtre supplémentaire, l' [allocateur de surface VBI](vbi-surface-allocator.md), était nécessaire pour allouer la mémoire vidéo supplémentaire pour le texte VBI. Pour les éditeurs de logiciels indépendants, VMR-7 simplifie le développement d’applications en combinant la fonctionnalité d’allocation et de rendu dans un filtre unique utilisé dans tous les scénarios. Avec VMR, l’allocateur de surface VBI n’est plus nécessaire. ce filtre est remplacé dans Windows XP par le nouveau filtre de [gestionnaire de port vidéo](video-port-manager.md) qui effectue toutes les tâches de port vidéo précédemment effectuées par le Mixer de superposition.

> [!Note]  
> VMR-9 ne prend pas en charge les ports vidéo.

 

Le VMR est plus robuste que les convertisseurs antérieurs, en partie parce qu’il utilise uniquement DirectDraw 7 (ou Direct3D 9 Si vous utilisez les interfaces VMR-9), par opposition aux anciens convertisseurs qui utilisaient un mélange d’interfaces provenant de versions plus anciennes et plus récentes de DirectDraw. VMR utilise également un nouveau mécanisme de présentation d’image conçu pour les générations actuelles et futures des adaptateurs, qui prennent en charge Direct3D, une VRAM accrue et une bande passante de mémoire vidéo, ainsi que des fonctionnalités d’accélération matérielle. Avec VMR, l’accent est porté sur le traitement frontal et la dépendance réduite sur les ports vidéo et les superpositions. Mais même avec toutes ses nouvelles fonctionnalités, VMR est conçu pour une compatibilité maximale avec les applications existantes.

VMR est également extensible. Les applications peuvent fournir leurs propres sous-composants pour effectuer des effets vidéo personnalisés et/ou prendre le contrôle du processus d’allocation et de rendu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du rendu de mixage vidéo](about-the-video-mixing-render.md)
</dt> </dl>

 

 



