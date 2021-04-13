---
title: Intégration de la bibliothèque
description: Intégration de la bibliothèque
ms.assetid: 6ff1b379-983b-4cd7-8142-27523a7a03e7
keywords:
- Windows Media Player Online stores, intégration de bibliothèque
- magasins en ligne, intégration de bibliothèque
- types 1 magasins en ligne, intégration de bibliothèque
- Windows Media Player Online stores, volets des tâches
- magasins en ligne, volets des tâches
- tapez 1 magasins en ligne, volets des tâches
- Windows Media Player, volets des tâches
- Bibliothèque du lecteur Windows Media, intégration
- bibliothèque, intégration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5353aba7099acd2dfd08596be7ffd43503bdad91
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381526"
---
# <a name="library-integration"></a>Intégration de la bibliothèque

L’interface utilisateur du lecteur Windows Media est organisée en zones de fonctionnalités, appelées *volets de tâches*, qui encapsulent les diverses fonctionnalités de haut niveau du programme. Celles-ci incluent les volets des tâches **bibliothèque**, **synchroniser** et **graver** (entre autres). Le volet des tâches de la **bibliothèque** permet aux utilisateurs de travailler avec la bibliothèque. le volet **synchroniser** les tâches permet aux utilisateurs de synchroniser des fichiers multimédias numériques sur un appareil mobile. le volet de tâches **grave** permet aux utilisateurs de graver des fichiers multimédias numériques sur un CD ou un DVD.

> [!Note]  
> Le volet des tâches de la **bibliothèque** est parfois appelé volet des tâches **Parcourir** .

 

Chacun de ces volets de tâches a un certain niveau d’intégration avec la bibliothèque. Par exemple, si l’utilisateur souhaite graver de la musique sur un CD, il est judicieux de laisser l’utilisateur choisir la musique à graver en parcourant la bibliothèque et en faisant simplement glisser-déplacer des éléments multimédias dans une liste. Cela signifie que les utilisateurs peuvent afficher et utiliser un catalogue de magasin en ligne entièrement intégré à la bibliothèque lors de l’utilisation des volets des tâches **bibliothèque**, **synchroniser** et **graver** . L’énumération [WMPTaskType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmptasktype) contient des valeurs qui représentent ces trois volets de tâches afin qu’ils puissent être identifiés par programmation.

Chacun de ces trois volets de tâches est organisé en trois parties principales. La première partie est le contrôle d’arborescence de la bibliothèque. Ce contrôle fournit à l’utilisateur une vue hiérarchique de la bibliothèque du lecteur Windows Media, y compris les fonctionnalités de catégorisation par chanson, artiste, album, etc. La deuxième partie du volet des tâches est le volet d’informations. Ce volet fournit des informations détaillées organisées en fonction de la catégorie actuellement sélectionnée dans le contrôle arborescence de la bibliothèque. Par exemple, si l’utilisateur a cliqué sur des **chansons** dans l’arborescence, le volet d’informations affiche les titres des chansons actuellement dans la bibliothèque, ainsi que d’autres informations telles que la longueur et le titre de l’album. La troisième partie est le volet liste, ou *panier*. Les utilisateurs peuvent glisser-déplacer des éléments multimédias dans le panier pour créer des listes, telles que des sélections, des listes de synchronisation et des listes de gravure.

Lorsqu’un catalogue de magasin en ligne est intégré à la bibliothèque, le magasin en ligne s’affiche sous la forme d’une catégorie de niveau supérieur, ou *nœud*, dans le contrôle d’arborescence de la bibliothèque. (Un seul catalogue de magasin en ligne est visible par l’utilisateur à la fois.) Quand un utilisateur choisit d’afficher le catalogue du magasin en ligne en cliquant sur le nœud, le volet d’informations affiche des informations sur la musique dans le catalogue du magasin en ligne. Cela inclut la musique achetée ou louée par l’utilisateur, ainsi que la musique que l’utilisateur n’a pas encore acquise.

Le nœud de magasin en ligne de niveau supérieur possède un ensemble de nœuds enfants fournis par le lecteur Windows Media. Par exemple, le nœud de magasin en ligne de niveau supérieur a des nœuds de radio, d’artiste et d’album enfants, entre autres. Le nœud de magasin en ligne de niveau supérieur peut également avoir jusqu’à huit nœuds enfants personnalisés fournis par le magasin en ligne. Le lecteur Windows Media crée un nœud enfant personnalisé pour toutes les listes ayant un identificateur de liste compris entre 0 et 7. Le magasin en ligne spécifie l’identificateur d’une liste dans le fichier [list.csv](list-csv.md) qui fait partie du catalogue du magasin.

Le lecteur Windows Media récupère une icône pour chacun des nœuds de l’arborescence personnalisée de la Banque en ligne en appelant [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), en passant CPListIDIcon dans le paramètre *bstrInfoName* .

Lorsque l’utilisateur navigue dans le catalogue, le lecteur Windows Media effectue des appels à **IWMPContentPartner :: GetItemInfo** pour récupérer les métadonnées du plug-in de partenaire de contenu à propos des éléments de musique sélectionnés par l’utilisateur. Ces métadonnées fournissent des informations au joueur afin que le lecteur puisse afficher des détails sur les éléments du catalogue. Par exemple, si l’utilisateur sélectionne un album, le lecteur Windows Media récupère l’URL de la pochette de l’album afin que l’utilisateur puisse voir l’image de la couverture de l’album.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




