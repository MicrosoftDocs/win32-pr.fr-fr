---
title: Utilisation de HTMLView avec des magasins en ligne
description: Utilisation de HTMLView avec des magasins en ligne
ms.assetid: 78de7ef3-400c-4411-8ade-35c421805df8
keywords:
- Windows Media Player Online stores, HTMLView
- magasins en ligne, HTMLView
- tapez 1 magasins en ligne, HTMLView
- tapez 2 magasins en ligne, HTMLView
- HTMLView, magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d136be4f7866b6911b8b007de7e784d6133c217
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510441"
---
# <a name="using-htmlview-with-online-stores"></a>Utilisation de HTMLView avec des magasins en ligne

Le lecteur Windows Media demande à l’utilisateur l’autorisation d’afficher le contenu HTMLView en **cours de lecture**. Les magasins en ligne peuvent désactiver cette invite en spécifiant une valeur d’URL de base dans l’élément **HTMLView** du document serviceInfo. Lorsque le lecteur Windows Media ouvre une sélection qui spécifie le contenu de HTMLView à afficher, le lecteur compare l’URL de base du document ServiceInfo du magasin en ligne actif à l’URL de base du contenu HTMLView. S’ils correspondent, le lecteur Windows Media affiche le contenu HTMLView sans inviter l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Affichage des pages Web dans le lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Élément HTMLView**](htmlview-element.md)
</dt> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




