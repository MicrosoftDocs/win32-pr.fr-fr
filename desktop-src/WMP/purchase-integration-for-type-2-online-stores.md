---
title: Acheter l’intégration pour les magasins de type 2 en ligne
description: Acheter l’intégration pour les magasins de type 2 en ligne
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player Online stores, intégration des achats
- magasins en ligne, intégration des achats
- type 2 magasins en ligne, intégration d’achat
- Windows Media Player Online stores, intégration des achats
- magasins en ligne, intégration des achats
- type 2 magasins en ligne, intégration des achats
- Windows Media Player, intégration des achats
- Windows Media Player, intégration des achats
- intégration des achats
- intégration des achats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511029"
---
# <a name="purchase-integration-for-type-2-online-stores"></a>Acheter l’intégration pour les magasins de type 2 en ligne

Lorsque le lecteur Windows Media lit du contenu multimédia numérique ou que l’utilisateur choisit l’option **Rechercher les informations** de l’album, le lecteur offre à l’utilisateur un lien pour acheter le CD ou DVD dont provient le contenu si un tel lien est disponible. Lorsque l’utilisateur clique sur le lien, le lecteur Windows Media 10 ou une version ultérieure appelle sur le magasin musical actuel pour gérer la demande d’achat. Dans ce cas, le lecteur accède au volet des tâches du premier service (dans le lecteur Windows Media 10) ou à l’onglet des magasins en ligne (dans le lecteur Windows Media 11) et affiche la page Web spécifiée par l’attribut **MediaPlayerURL** de l’élément **BuyCD** du document serviceInfo. (Les attributs **MediaCenterURL** et **BrowserURL** sont utilisés de la même manière pour gérer les appels de Windows xp Media Center Edition 2004 et Windows XP Service Pack 2).

Le lecteur Windows Media ajoute une chaîne de requête à l’URL pour fournir des informations au magasin en ligne sur le contenu que l’utilisateur a choisi d’acheter. La chaîne de requête comprend des attributs tels que **titre**, **album** et **artiste**, que le magasin en ligne peut utiliser pour déterminer l’album à vendre. La documentation de référence de l’élément **BuyCD** fournit la liste complète des attributs de chaîne de requête et leurs descriptions.

## <a name="guidelines-for-the-buycd-page"></a>Instructions pour la page BuyCD

Lorsque vous créez votre page Web BuyCD, suivez les instructions ci-dessous :

-   La page doit clairement identifier la Banque en ligne qui fournit les informations. Pour ce faire, vous pouvez afficher de manière visible votre logo, par exemple.
-   La page doit inclure un lien vers la déclaration de confidentialité de votre société.
-   Il est préférable de fournir des informations d’achat initiales sans que l’utilisateur soit obligé d’installer des programmes ou de se connecter à votre boutique en ligne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Élément BuyCD**](buycd-element.md)
</dt> </dl>

 

 




