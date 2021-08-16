---
title: Acheter l’intégration pour les magasins de type 2 en ligne
description: Acheter l’intégration pour les magasins de type 2 en ligne
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Lecteur Windows Media des magasins en ligne, intégration des achats
- magasins en ligne, intégration des achats
- type 2 magasins en ligne, intégration d’achat
- Lecteur Windows Media des magasins en ligne, intégration des achats
- magasins en ligne, intégration des achats
- type 2 magasins en ligne, intégration des achats
- Lecteur Windows Media, intégration des achats
- Lecteur Windows Media, intégration des achats
- intégration des achats
- intégration des achats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d854ecfd91cd0a887c242ad743874a6ec1a469ebcca3aa788bf57c2c59041d6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746693"
---
# <a name="purchase-integration-for-type-2-online-stores"></a>Acheter l’intégration pour les magasins de type 2 en ligne

lorsque Lecteur Windows Media lit le contenu multimédia numérique ou que l’utilisateur choisit **rechercher des informations sur l’Album**, le lecteur offre à l’utilisateur un lien pour acheter le CD ou DVD dont provient le contenu si un tel lien est disponible. lorsque l’utilisateur clique sur le lien, Lecteur Windows Media 10 appels ou ultérieurs sur le magasin musical actuel pour gérer la demande d’achat. dans ce cas, le lecteur accède au volet office premier service (dans Lecteur Windows Media 10) ou à l’onglet magasins en ligne (dans Lecteur Windows Media 11) et affiche la page web spécifiée par l’attribut **MediaPlayerURL** de l’élément **BuyCD** du document ServiceInfo. (les attributs **MediaCenterURL** et **BrowserURL** sont utilisés de la même manière pour gérer les appels de Windows xp Media Center Edition 2004 et Windows XP Service Pack 2).

Lecteur Windows Media ajoute une chaîne de requête à l’URL pour fournir des informations au magasin en ligne sur le contenu que l’utilisateur a choisi d’acheter. La chaîne de requête comprend des attributs tels que **titre**, **album** et **artiste**, que le magasin en ligne peut utiliser pour déterminer l’album à vendre. La documentation de référence de l’élément **BuyCD** fournit la liste complète des attributs de chaîne de requête et leurs descriptions.

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

 

 




