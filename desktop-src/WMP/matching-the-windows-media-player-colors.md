---
title: correspondance des couleurs de Lecteur Windows Media
description: correspondance des couleurs de Lecteur Windows Media
ms.assetid: b4d1da08-a4cf-46dd-82a5-40562bb3c049
keywords:
- Lecteur Windows Media des magasins en ligne, mise en correspondance des couleurs de Lecteur Windows Media
- magasins en ligne, mise en correspondance des couleurs de Lecteur Windows Media
- types 1 magasins en ligne, Lecteur Windows Media des couleurs de correspondance
- type 2 magasins en ligne, correspondance Lecteur Windows Media couleurs
- Lecteur Windows Media les magasins en ligne, Lecteur Windows Media la correspondance des couleurs
- magasins en ligne, Lecteur Windows Media correspondance des couleurs
- tapez 1 magasins en ligne, Lecteur Windows Media la correspondance des couleurs
- type 2 magasins en ligne, Lecteur Windows Media correspondance des couleurs
- Lecteur Windows Media des magasins en ligne, correspondance des couleurs pour Lecteur Windows Media
- magasins en ligne, correspondance des couleurs pour Lecteur Windows Media
- types 1 magasins en ligne, correspondance des couleurs pour Lecteur Windows Media
- type 2 magasins en ligne, correspondance des couleurs pour Lecteur Windows Media
- correspondance des couleurs pour Lecteur Windows Media
- couleurs de Lecteur Windows Media correspondantes
- Lecteur Windows Media, couleurs correspondantes
- Lecteur Windows Media, correspondance des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eedf3e5df7c02f498c0dc21aeeed16c99452003c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919155"
---
# <a name="matching-the-windows-media-player-colors"></a>correspondance des couleurs de Lecteur Windows Media

la création d’une page web de boutique en ligne qui correspond à la Lecteur Windows Media modèle de couleurs est simple. Gérez simplement l’événement **External. OnColorChange** . Pour spécifier une fonction pour gérer l’événement, utilisez un code semblable au suivant lors du chargement de votre page Web :


```C++
// Set up the color change event.
external.OnColorChange = OnAppColor;
```



chaque fois que l’utilisateur modifie le modèle de couleurs de Lecteur Windows Media, le lecteur appellera votre fonction. L’exemple suivant montre une fonction simple qui définit l’arrière-plan de la page Web pour qu’il corresponde à la propriété **External. appColorLight** :


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

 

 




