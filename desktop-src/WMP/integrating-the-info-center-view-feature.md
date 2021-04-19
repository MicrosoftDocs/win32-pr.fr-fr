---
title: Intégration de la fonctionnalité d’affichage du centre d’informations
description: Intégration de la fonctionnalité d’affichage du centre d’informations
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player Online stores, intégration de l’affichage du centre d’informations
- magasins en ligne, intégration de l’affichage du centre d’informations
- tapez 1 magasins en ligne, en intégrant le mode Info Center
- tapez 2 magasins en ligne, en intégrant le mode Info Center
- Magasins en ligne du lecteur Windows Media, affichage Centre d’informations
- magasins en ligne, affichage Centre d’informations
- tapez 1 magasins en ligne, affichage Centre d’informations
- type 2 magasins en ligne, affichage Centre d’informations
- intégration de l’affichage du centre d’informations
- Affichage du centre d’informations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106536877"
---
# <a name="integrating-the-info-center-view-feature"></a>Intégration de la fonctionnalité d’affichage du centre d’informations

Le lecteur Windows Media permet aux utilisateurs d’ouvrir et de fermer la fonctionnalité d’affichage du centre d’informations. Le mode Info Center est la fonctionnalité dans laquelle les utilisateurs s’attendent à trouver des informations riches et étendues sur du contenu multimédia numérique spécifique. Lorsque l’utilisateur choisit d’ouvrir le mode Info Center, les appels du lecteur Windows Media sur le magasin de musique actuel permettent d’afficher la page Web du mode Info Center spécifiée par l’attribut **URL** de l’élément **Centre** d’informations du document serviceInfo.

Pour récupérer des informations sur le contenu multimédia numérique en cours de lecture, vous devez incorporer une instance du contrôle du lecteur Windows Media dans votre page Web et utiliser le modèle objet du lecteur. Par exemple, pour récupérer le titre, vous pouvez utiliser le code JScript suivant :


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

[**Utilisation du contrôle du lecteur Windows Media dans une page Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




