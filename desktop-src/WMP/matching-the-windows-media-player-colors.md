---
title: Correspondance des couleurs du lecteur Windows Media
description: Correspondance des couleurs du lecteur Windows Media
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Windows Media Player Online stores, correspondance des couleurs du lecteur Windows Media
- magasins en ligne, correspondance des couleurs du lecteur Windows Media
- tapez 1 magasins en ligne, en faisant correspondre les couleurs du lecteur Windows Media
- tapez 2 magasins en ligne, en faisant correspondre les couleurs du lecteur Windows Media
- Windows Media Player Online stores, correspondance des couleurs du lecteur Windows Media
- magasins en ligne, correspondance des couleurs du lecteur Windows Media
- types 1 magasins en ligne, correspondance des couleurs du lecteur Windows Media
- type 2 magasins en ligne, correspondance des couleurs du lecteur Windows Media
- Windows Media Player Online stores, correspondance des couleurs pour Windows Media Player
- magasins en ligne, correspondance des couleurs pour Windows Media Player
- tapez 1 magasins en ligne, correspondance des couleurs pour Windows Media Player
- type 2 magasins en ligne, correspondance des couleurs pour le lecteur Windows Media
- correspondance des couleurs pour le lecteur Windows Media
- correspondance des couleurs du lecteur Windows Media
- Lecteur Windows Media, couleurs correspondantes
- Lecteur Windows Media, correspondance des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512462"
---
# <a name="matching-the-windows-media-player-colors"></a>Correspondance des couleurs du lecteur Windows Media

Il est facile de faire en sorte que votre page Web de boutique en ligne corresponde au jeu de couleurs du lecteur Windows Media. Gérez simplement l’événement **External. OnColorChange** . Pour spécifier une fonction pour gérer l’événement, utilisez un code semblable au suivant lors du chargement de votre page Web :


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



Chaque fois que l’utilisateur modifie le modèle de couleurs du lecteur Windows Media, le lecteur appellera votre fonction. L’exemple suivant montre une fonction simple qui définit l’arrière-plan de la page Web pour qu’il corresponde à la propriété **External. appColorLight** :


```C++
// Match the current color.
function OnAppColor()
{
    window.document.bgColor = external.appColorLight;
}
```



D’autres propriétés de couleur sont également disponibles pour votre utilisation. Consultez [objet externe pour les magasins en ligne de type 2](external-object-for-type-2-online-stores.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**External. appColorLight**](external-appcolorlight.md)
</dt> <dt>

[**External. OnColorChange, événement**](external-oncolorchange-event.md)
</dt> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




