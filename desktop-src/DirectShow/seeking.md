---
description: Cherche
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: Cherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104570043"
---
# <a name="seeking"></a>Cherche

Les filtres prennent en charge la recherche par le biais de l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . L’application interroge le gestionnaire du graphique de filtre pour **IMediaSeeking** et l’utilise pour émettre des commandes de recherche. Le gestionnaire de graphes de filtre distribue chaque commande de recherche à tous les filtres de convertisseur du graphique. Chaque convertisseur transmet la commande en amont, via les broches de sortie des filtres en amont, jusqu’à ce qu’elle atteigne un filtre qui peut exécuter la recherche. En général, un filtre source ou un filtre d’analyseur, tel que le [séparateur AVI](avi-splitter-filter.md), effectue l’opération de recherche.

Lorsqu’un filtre effectue une opération de recherche, il vide toutes les données en attente. Le résultat est de réduire la latence des commandes de recherche, car les données existantes sont vidées du graphique. Après une commande Seek, le temps de flux se réinitialise à zéro.

Le diagramme suivant illustre la séquence d’événements.

![séquence d’événements](images/seeking.png)

Si un filtre de l’analyseur a plusieurs broches de sortie, il les désigne généralement pour accepter les commandes Seek. Les autres codes confidentiels rejettent ou ignorent les commandes de recherche qu’ils reçoivent. De cette façon, l’analyseur conserve tous ses flux synchronisés. Toutefois, toutes les broches de sortie doivent implémenter [**IMediaSeeking :: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) et [**IMediaSeeking :: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) pour retourner les fonctionnalités de recherche du filtre. Cela permet de s’assurer que le gestionnaire de graphes de filtres retourne la valeur correcte à l’application.

L’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) est dépréciée pour les filtres. Les clients Automation doivent toujours utiliser cette interface sur le gestionnaire de graphique de filtre, car **IMediaSeeking** n’est pas compatible avec Automation, mais le gestionnaire de graphique de filtre traduit tous les appels **IMediaPosition** en appels **IMediaSeeking** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidage](flushing.md)
</dt> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



