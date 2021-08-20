---
title: Intégration des informations de l’album
description: Intégration des informations de l’album
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- magasins en ligne Lecteur Windows Media, intégration des informations sur les albums
- magasins en ligne, intégration des informations sur les albums
- types 2 magasins en ligne, intégration des informations sur les albums
- Lecteur Windows Media magasins en ligne, intégration des informations relatives aux albums
- magasins en ligne, intégration des informations relatives aux albums
- tapez 2 magasins en ligne, en intégrant les informations de l’album
- Lecteur Windows Media, intégration des informations relatives aux albums
- Lecteur Windows Media, intégration des informations sur les albums
- intégration des informations de l’album
- intégration des informations relatives aux albums
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdd8c0c200d0d1779ecc9d4f90da3f3755f276431792f7a6b6450dd43e51cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055427"
---
# <a name="album-info-integration"></a>Intégration des informations de l’album

Lecteur Windows Media permet aux utilisateurs de demander des informations détaillées sur le CD ou le DVD à partir duquel le contenu multimédia numérique provient en cliquant sur un bouton, par exemple **plus d’informations**. lorsque l’utilisateur clique sur le bouton, Lecteur Windows Media 10 ou des appels ultérieurs sur le magasin de musique actuel pour afficher les détails de l’album. Dans ce cas, le lecteur ouvre le volet informations sur l’album et affiche la page Web spécifiée par l’attribut **URL** de l’élément **AlbumInfo** du document serviceInfo.

Lecteur Windows Media ajoute une chaîne de requête à l’URL pour fournir des informations au magasin en ligne sur le contenu demandé par l’utilisateur. La chaîne de requête comprend des attributs tels que **titre**, **album** et **artiste**, que le magasin en ligne peut utiliser pour déterminer l’album approprié à afficher. La documentation de référence de l’élément **AlbumInfo** fournit la liste complète des attributs de chaîne de requête et leurs descriptions.

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

 

 




