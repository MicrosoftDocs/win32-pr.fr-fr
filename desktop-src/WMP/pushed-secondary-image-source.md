---
title: Source d’image secondaire faisant l’objet d’un push
description: Source d’image secondaire faisant l’objet d’un push
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Lecteur Windows Media Skins mobiles, source d’image de bouton
- apparences, source de l’image du bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, source d’image
- source d’image pour les apparences, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37045da71b8417856ec72ac7e57a6a787426ba486993b9fef03910b4d32e663d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861829"
---
# <a name="pushed-secondary-image-source"></a>Source d’image secondaire faisant l’objet d’un push

Selon la fonction Button, vous devrez peut-être définir l’emplacement de l’image Poussée pour l’état secondaire du bouton. Il s’agit de l’image que les utilisateurs voient lorsqu’ils poussent le bouton de fonction PlayPause la deuxième fois.

Pour définir cette image, vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace. Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées de l’angle supérieur gauche (en pixels) de l’image à utiliser dans le type d’image à partir duquel vous dessinez.

Par exemple, pour définir l’image de Push pour une source d’image secondaire, si votre image est à l’intérieur de la bitmap push, tapez :


```C++
Pushed @ 248,0

```



Les États secondaires ne peuvent pas avoir d’image désactivée. Les images secondaires sont supposées avoir la même largeur et la même hauteur que l’image principale.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Boutons**](buttons.md)
</dt> </dl>

 

 




