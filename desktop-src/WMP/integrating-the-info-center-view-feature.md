---
title: Intégration de la fonctionnalité d’affichage du centre d’informations
description: Intégration de la fonctionnalité d’affichage du centre d’informations
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Lecteur Windows Media des magasins en ligne, intégration du centre d’informations
- magasins en ligne, intégration de l’affichage du centre d’informations
- tapez 1 magasins en ligne, en intégrant le mode Info Center
- tapez 2 magasins en ligne, en intégrant le mode Info Center
- Lecteur Windows Media magasins en ligne, affichage centre d’informations
- magasins en ligne, affichage Centre d’informations
- tapez 1 magasins en ligne, affichage Centre d’informations
- type 2 magasins en ligne, affichage Centre d’informations
- intégration de l’affichage du centre d’informations
- Affichage du centre d’informations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caea279f933c3cbb411da72aab9ddf971df5f38c69d7291ae4ac67f7b96ed91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135462"
---
# <a name="integrating-the-info-center-view-feature"></a>Intégration de la fonctionnalité d’affichage du centre d’informations

Lecteur Windows Media permet aux utilisateurs d’ouvrir et de fermer la fonctionnalité d’affichage du centre d’informations. Le mode Info Center est la fonctionnalité dans laquelle les utilisateurs s’attendent à trouver des informations riches et étendues sur du contenu multimédia numérique spécifique. lorsque l’utilisateur choisit d’ouvrir le mode info center, Lecteur Windows Media appels sur le magasin de musique actuel pour afficher la page web du mode info center spécifiée par l’attribut **URL** de **l’élément centre** d’informations du document ServiceInfo.

pour récupérer des informations sur le contenu multimédia numérique en cours de lecture, vous devez incorporer une instance du contrôle Lecteur Windows Media dans votre page web et utiliser le modèle objet Player. par exemple, pour récupérer le titre, vous pouvez utiliser le code JScript suivant :


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a>Instructions pour le mode Info Center

Lorsque vous créez votre page Web d' **affichage du centre d’informations** , suivez les instructions ci-dessous :

-   La page doit clairement identifier la Banque en ligne qui fournit les informations. Pour ce faire, vous pouvez afficher de manière visible votre logo, par exemple.
-   La page doit inclure un lien vers la déclaration de confidentialité de votre société.
-   Évitez autant que possible la navigation entre les pages au sein de la fonctionnalité d’affichage du centre d’informations. Vous devez accéder à votre magasin en ligne pour la plupart des activités.
-   Il est préférable de fournir des informations précieuses sans que l’utilisateur soit obligé d’installer des programmes ou de se connecter à votre boutique en ligne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Élément Centre d’informations**](infocenter-element.md)
</dt> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**utilisation du contrôle Lecteur Windows Media dans une Page Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




