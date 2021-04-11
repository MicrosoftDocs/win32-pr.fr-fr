---
title: Ajout d’un curseur
description: Ajout d’un curseur
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- création d’apparences, de curseurs
- Apparences du lecteur Windows Media, curseurs
- apparences, curseurs
- curseurs dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029464"
---
# <a name="adding-a-slider"></a>Ajout d’un curseur

Vous pouvez ajouter un curseur pour afficher la position actuelle du média et permettre également à l’utilisateur de modifier la position dans le fichier multimédia actuel.

Tout d’abord, vous devez ajouter l’élément **Slider** :


```C++
<SLIDER
  id = "myslider"
  min = "0"
  max = "wmpprop:player.currentMedia.duration"
  onmouseup = "player.controls.currentPosition = myslider.value; "
  tooltip = "current position"
  height = "10"
  width = "180"
  top = "150"
  left = "88"
  backgroundColor = "red"
  foregroundColor = "blue"
  thumbImage = "thumb.bmp"/>

```



Cela définit une valeur maximale en fonction de la durée du fichier multimédia actuel. Cela utilise une petite image bitmap de pouce qui est simplement un carré vert de 10 pixels par 10 pixels. L’arrière-plan du curseur est rouge et le premier plan est bleu. Lorsque l’utilisateur fait glisser l’image Thumb vers une nouvelle position et laisse le bouton de la souris enfoncé, le média passe à cette position.

Toutefois, le curseur ne se déplacera pas de lui-même, sauf si vous mesurez la position actuelle avec l’attribut **CurrentPosition \_ OnChange** de l’élément **Controls** , qui est incorporé dans l’élément **Player** .


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



Lorsque la position du média change, cela déclenche un événement qui exécute ensuite la ligne de code qui modifie la valeur du curseur à la position actuelle du média.

Vous pouvez voir une apparence de curseur de travail similaire dans la section exemple du kit de développement logiciel (SDK).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de création d’apparence**](skin-creation-guide.md)
</dt> </dl>

 

 




