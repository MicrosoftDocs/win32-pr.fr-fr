---
title: Création de curseurs personnalisés
description: Création de curseurs personnalisés
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- création d’apparences, de curseurs
- habillages Lecteur Windows Media, curseurs
- apparences, curseurs
- curseurs dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919308"
---
# <a name="creating-custom-sliders"></a>Création de curseurs personnalisés

Vous pouvez créer des curseurs personnalisés dans n’importe quelle forme de votre choix. Pour cet exemple, un simple bandeau est choisi, mais la forme réelle peut être n’importe quoi. Voici le code de l’élément **CUSTOMSLIDER** :


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



Cela permet de définir une valeur initiale pour le curseur. Deux nouvelles bitmaps sont introduites. L’une est la bitmap en nuances de gris (slider.bmp) qui définit les valeurs qui seront utilisées lorsque vous cliquez sur, et l’autre (slider.bmp) qui détermine l’image qui sera affichée lorsqu’un clic est effectué sur une partie particulière de la nuances de gris.

La valeur initiale est déterminée par l’écoute du volume avec wmpprop, puis le volume peut être modifié lorsque l’utilisateur clique sur une partie du curseur qui déclenche une modification de la valeur.

Vous pouvez voir une apparence de curseur de travail similaire dans la section exemple du kit de développement logiciel (SDK).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de création d’apparence**](skin-creation-guide.md)
</dt> </dl>

 

 




