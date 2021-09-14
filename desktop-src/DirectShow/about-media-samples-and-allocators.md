---
description: À propos des exemples de supports et des allocators
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: À propos des exemples de supports et des allocators
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112422"
---
# <a name="about-media-samples-and-allocators"></a>À propos des exemples de supports et des allocators

Les filtres fournissent des données sur les connexions de code confidentiel. Les données sont déplacées de la broche de sortie d’un filtre vers la broche d’entrée d’un autre filtre. La méthode la plus courante pour que la broche de sortie remette les données consiste à appeler la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur l’entrée, bien qu’il existe également quelques autres mécanismes.

Selon le filtre, il est possible d’allouer de la mémoire pour les données multimédias de différentes façons : sur le tas, dans une surface DirectDraw, à l’aide de la mémoire GDI partagée ou à l’aide d’un autre mécanisme d’allocation. L’objet chargé d’allouer la mémoire est appelé *Allocator*, qui est un objet com qui expose l’interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Lorsque deux codes confidentiels se connectent, l’un des codes confidentiels doit fournir un allocateur. DirectShow définit une séquence d’appels de méthode qui est utilisée pour établir quel pin fournit l’allocateur. Les codes confidentiels acceptent également le nombre de mémoires tampons que l’allocateur va créer et la taille des mémoires tampons.

Avant le début de la diffusion en continu, l’allocateur crée un pool de mémoires tampons. Pendant la diffusion en continu, le filtre amont remplit les tampons de données et les remet au filtre en aval. Toutefois, le filtre amont n’attribue pas de pointeurs bruts de filtre en aval aux tampons. Au lieu de cela, il utilise les objets COM appelés *exemples de médias*, que l’allocateur crée pour gérer les mémoires tampons. Les exemples de supports exposent l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Un exemple de support contient les éléments suivants :

-   pointeur vers la mémoire tampon sous-jacente
-   un horodatage
-   différents indicateurs
-   éventuellement, un type de média

L’horodatage définit l’heure de présentation, que le filtre de convertisseur utilise pour planifier le rendu. Les indicateurs indiquent notamment s’il y a eu une rupture dans les données depuis l’exemple précédent. Le type de média offre un moyen pour les filtres de modifier les formats mi-flux. En règle générale, l’exemple n’a aucun type de média, ce qui indique que le format n’a pas changé depuis l’exemple précédent.

Lorsqu’un filtre utilise une mémoire tampon, il contient le nombre de références sur l’exemple. L’allocateur utilise le décompte de références pour déterminer quand il peut réutiliser la mémoire tampon. Cela empêche un filtre de remplacer une mémoire tampon qu’un autre filtre utilise encore. Un exemple ne retourne pas au pool d’exemples disponibles de l’allocateur tant que chaque filtre ne l’a pas libéré.

Pour plus d'informations, voir les rubriques suivantes :

-   La rubrique [exemples et allocators](samples-and-allocators.md) fournit une description plus détaillée du fonctionnement des allocateurs.
-   le [Flow de données de la rubrique dans le Graph de filtre](data-flow-in-the-filter-graph.md) donne une vue d’ensemble générale du workflow de données dans DirectShow.

Les rubriques suivantes sont destinées aux développeurs qui écrivent leurs propres filtres personnalisés :

-   [Flow de données pour les développeurs de filtres](data-flow-for-filter-developers.md)
-   [Threads et sections critiques](threads-and-critical-sections.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[le filtre Graph et ses composants](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



