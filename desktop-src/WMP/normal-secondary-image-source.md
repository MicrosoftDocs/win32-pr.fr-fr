---
title: Source d’image secondaire normale
description: Source d’image secondaire normale
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Lecteur Windows Media Skins mobiles, source d’image de bouton
- apparences, source de l’image du bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, source d’image
- source d’image pour les apparences, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f6aeb48ceabc873d4aeb0db910db896712fe16377aa0f67b76205ad8a39c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573729"
---
# <a name="normal-secondary-image-source"></a>Source d’image secondaire normale

Selon la fonction Button, vous devrez peut-être définir l’emplacement de l’image normale pour l’état secondaire du bouton. Il s’agit de l’image que les utilisateurs voient quand ils poussent le bouton de fonction PlayPause la première fois.

Pour définir cette image, vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace. Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées de l’angle supérieur gauche (en pixels) de l’image à utiliser dans le type de bitmap à partir duquel vous dessinez.

Par exemple, pour définir l’image normale pour une source d’image secondaire, si votre image est à l’intérieur de la bitmap push, tapez :


```C++
Pushed @ 210,0

```



Les États secondaires ne peuvent pas avoir d’image désactivée. Les images secondaires sont supposées avoir la même largeur et la même hauteur que l’image principale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Boutons**](buttons.md)
</dt> </dl>

 

 




