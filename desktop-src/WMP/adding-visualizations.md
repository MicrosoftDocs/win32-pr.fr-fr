---
title: Ajout de visualisations
description: Ajout de visualisations
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- création d’apparences, visualisations
- apparences de Lecteur Windows Media, visualisations
- apparences, visualisations
- visualisations, apparences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d236990d3e29cf4e51dbb46e8e1269b0c8a50ccaf205940a6f34b97c89fa6e62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619149"
---
# <a name="adding-visualizations"></a>Ajout de visualisations

Vous pouvez ajouter une fenêtre de visualisation de la même façon que vous avez ajouté une fenêtre vidéo. La même apparence peut être utilisée, mais un élément **Effects** est utilisé.

Tout d’abord, vous devez ajouter l’élément **Effects** et lui attribuer un ID et une taille :


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



Vous pouvez ensuite assigner les deux boutons une chaîne de code de visualisation précédente et suivante :


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



Les couches et les bitmaps étaient les mêmes que celles utilisées dans l’exemple de vidéo, à la différence près que la flèche de lecture a été copiée et retournée horizontalement.

Enfin, un simple élément **Player** avec l’attribut **URL** a été ajouté pour choisir une chanson à lire.


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



Vous pouvez voir une apparence de visualisation de travail similaire dans la section exemple du kit de développement logiciel (SDK).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de création d’apparence**](skin-creation-guide.md)
</dt> </dl>

 

 




