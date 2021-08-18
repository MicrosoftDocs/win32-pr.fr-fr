---
title: Constantes d’emplacement de bibliothèque
description: Constantes d’emplacement de bibliothèque
ms.assetid: 88ff9b91-6b21-4f7d-ae13-e8456a3e0f75
keywords:
- Lecteur Windows Media les magasins en ligne, les constantes d’emplacement de bibliothèque
- magasins en ligne, constantes d’emplacement de bibliothèque
- types 1 magasins en ligne, constantes d’emplacement de la bibliothèque
- Lecteur Windows Media magasins en ligne, emplacements
- magasins en ligne, emplacements
- tapez 1 magasins en ligne, emplacements
- bibliothèque de Lecteur Windows Media, constantes d’emplacement
- bibliothèque, constantes d’emplacement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a677f405ff36030647618a83bd0b8b952dae254a756cebc48e4c3210e5fcde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135362"
---
# <a name="library-location-constants"></a>Constantes d’emplacement de bibliothèque

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

Les constantes d’emplacement de bibliothèque sont des variables de chaîne globales définies dans contentpartner. h. Elles sont utilisées par certaines méthodes des interfaces [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) et [IWMPContentPartnerCallback](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback) et par certaines méthodes de l’objet [externe](external-object-for-type-1-online-stores.md) . Ces constantes sont utilisées pour indiquer les types suivants.

-   type d’emplacement de la bibliothèque : il s’agit du type de vue de bibliothèque affiché par Lecteur Windows Media. Par exemple, le joueur peut afficher une vue d’un album particulier (g \_ szCPAlbumID) ou la vue de tous les genres (g \_ szAllCPGenreIDs).
-   Type d’élément sélectionné : il s’agit du type d’élément sélectionné dans la vue bibliothèque. Par exemple, l’utilisateur peut sélectionner un album particulier (g \_ szCPAlbumID) dans la vue de tous les albums.
-   Type de liste : il s’agit du type de liste demandé par le plug-in de partenaire de contenu. par exemple, Lecteur Windows Media pouvez demander au plug-in de fournir une liste d’éléments associés à une sélection particulière (g \_ szCPListID).
-   Type d’élément de liste : type d’élément de liste individuel demandé à partir du plug-in de partenaire de contenu. par exemple, Lecteur Windows Media pouvez demander au plug-in de fournir la liste des pistes (g \_ szCPTrackID) dans une sélection particulière.

Le tableau suivant indique le nom et la valeur de chaque constante, ainsi qu’une brève description de l’emplacement ou du type de la bibliothèque. Dans du code C ou C++ compilé avec le fichier d’en-tête contentpartner. h, vous pouvez utiliser le nom ou la valeur d’une constante. Il est préférable d’utiliser le nom, car le compilateur détectera les fautes d’orthographe. Dans le script (par exemple, lors de l’appel des méthodes de l’objet [externe](external-object-for-type-1-online-stores.md) ), vous ne pouvez pas utiliser le nom d’une constante ; vous devez utiliser la valeur.



| Nom                              | Valeur                        | Emplacement ou type                                                                                                                                                   |
|-----------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_szUnknownLocation g              | UnknownLocation              | Ensemble de pistes qui n’est ni un album ni une sélection. Lecteur Windows Media utilise également cette constante dans les rares cas où elle ne peut pas déterminer un emplacement valide. |
| \_szRootLocation g                 | RootLocation                 | Nœud supérieur dans le contrôle d’arborescence de la bibliothèque                                                                                                                      |
| \_szFlyoutMenu g                   | FlyoutMenu                   | Menu contextuel de la boutique en ligne actuelle                                                                                                                             |
| \_szOnlineStore g                  | OnlineStore                  | Tous les magasins en ligne                                                                                                                                                  |
| \_szCPListID g                     | CPListID                     | Une liste individuelle                                                                                                                                                 |
| \_szAllCPListIDs g                 | AllCPListIDs                 | Toutes les listes                                                                                                                                                          |
| \_szCPTrackID g                    | CPTrackID                    | Une piste individuelle                                                                                                                                                |
| \_szAllCPTrackIDs g                | AllCPTrackIDs                | Toutes les pistes                                                                                                                                                         |
| \_szCPArtistID g                   | CPArtistID                   | Un artiste individuel                                                                                                                                               |
| \_szAllCPArtistIDs g               | AllCPArtistIDs               | Tous les artistes                                                                                                                                                        |
| \_szCPAlbumID g                    | CPAlbumID                    | Un album individuel                                                                                                                                                |
| \_szAllCPAlbumIDs g                | AllCPAlbumIDs                | Tous les albums                                                                                                                                                         |
| \_szCPGenreID g                    | CPGenreID                    | Un genre individuel                                                                                                                                                |
| \_szAllCPGenreIDs g                | AllCPGenreIDs                | Tous les genres                                                                                                                                                         |
| \_szCPAlbumSubGenreID g            | CPAlbumSubGenreID            | Un sous-genre individuel                                                                                                                                             |
| \_szAllCPAlbumSubGenreIDs g        | AllCPAlbumSubGenreIDs        | Tous les sous-genres                                                                                                                                                      |
| \_szReleaseDateYear g              | ReleaseDateYear              | Année individuelle à laquelle le contenu du catalogue a été publié                                                                                                               |
| \_szAllReleaseDateYears g          | AllReleaseDateYears          | Toutes les années de publication du contenu du catalogue                                                                                                                        |
| \_szCPRadioID g                    | CPRadioID                    | Un flux radio individuel                                                                                                                                         |
| \_szAllCPRadioIDs g                | AllCPRadioIDs                | Tous les flux radio                                                                                                                                                  |
| \_szAuthor g                       | Auteur                       | Un auteur individuel                                                                                                                                               |
| \_szAllAuthors g                   | AllAuthors                   | Tous les auteurs                                                                                                                                                        |
| \_szWMParentalRating g             | WMParentalRating             | Une évaluation parentale individuelle                                                                                                                                      |
| \_szAllWMParentalRatings g         | AllWMParentalRatings         | Toutes les évaluations parentales                                                                                                                                               |
| \_szUserEffectiveRatingStars g     | UserEffectiveRatingStars     | Évaluation d’un utilisateur individuel, mesurée en nombre d’étoiles                                                                                                           |
| \_szAllUserEffectiveRatingStarss g | AllUserEffectiveRatingStarss | Toutes les évaluations utilisateur                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**External. addToBasket**](external-addtobasket.md)
</dt> <dt>

[**Externe. acheter**](external-buy.md)
</dt> <dt>

[**External. changeView**](external-changeview.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External. Download**](external-download.md)
</dt> <dt>

[**External. libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External. Play**](external-play.md)
</dt> <dt>

[**IWMPContentPartner::GetCommands**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartner::GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**IWMPContentPartner :: commande InvokeCommand**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)
</dt> <dt>

[**IWMPContentPartnerCallback::ChangeView**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-changeview)
</dt> </dl>

 

 




