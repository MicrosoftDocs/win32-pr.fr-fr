---
title: Intégration des informations de l’album
description: Intégration des informations de l’album
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player Online stores, album info Integration
- magasins en ligne, intégration des informations sur les albums
- types 2 magasins en ligne, intégration des informations sur les albums
- Windows Media Player Online stores, intégration des informations relatives aux albums
- magasins en ligne, intégration des informations relatives aux albums
- tapez 2 magasins en ligne, en intégrant les informations de l’album
- Lecteur Windows Media, intégration des informations relatives aux albums
- Windows Media Player, intégration des informations sur les albums
- intégration des informations de l’album
- intégration des informations relatives aux albums
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029129"
---
# <a name="album-info-integration"></a>Intégration des informations de l’album

Le lecteur Windows Media permet aux utilisateurs de demander des informations détaillées sur le CD ou le DVD à partir duquel le contenu multimédia numérique provient en cliquant sur un bouton, par exemple **plus d’informations**. Lorsque l’utilisateur clique sur le bouton, le lecteur Windows Media 10 ou une version ultérieure appelle sur le magasin musical actuel pour afficher les détails de l’album. Dans ce cas, le lecteur ouvre le volet informations sur l’album et affiche la page Web spécifiée par l’attribut **URL** de l’élément **AlbumInfo** du document serviceInfo.

Le lecteur Windows Media ajoute une chaîne de requête à l’URL pour fournir des informations au magasin en ligne sur le contenu demandé par l’utilisateur. La chaîne de requête comprend des attributs tels que **titre**, **album** et **artiste**, que le magasin en ligne peut utiliser pour déterminer l’album approprié à afficher. La documentation de référence de l’élément **AlbumInfo** fournit la liste complète des attributs de chaîne de requête et leurs descriptions.

## <a name="guidelines-for-album-info"></a>Instructions pour les informations relatives aux albums

Lorsque vous créez votre page Web d’informations sur l’album, suivez les instructions ci-dessous :

-   La page doit clairement identifier la Banque en ligne qui fournit les informations. Pour ce faire, vous pouvez afficher de manière visible votre logo, par exemple.
-   La page doit inclure un lien vers la déclaration de confidentialité de votre société.
-   Évitez autant que possible la navigation entre les pages dans la fonctionnalité d’informations sur les albums. Vous devez accéder à votre magasin en ligne pour la plupart des activités.
-   Nous vous recommandons de fournir des informations précieuses sans que l’utilisateur soit obligé d’installer des programmes ou de se connecter à votre boutique en ligne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Élément AlbumInfo**](albuminfo-element.md)
</dt> </dl>

 

 




