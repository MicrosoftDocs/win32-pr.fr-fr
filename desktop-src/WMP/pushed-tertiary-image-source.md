---
title: Source d’image tertiaire envoyée
description: Source d’image tertiaire envoyée
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Lecteur Windows Media Skins mobiles, source d’image de bouton
- apparences, source de l’image du bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, source d’image
- source d’image pour les apparences, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010954"
---
# <a name="pushed-tertiary-image-source"></a>Source d’image tertiaire envoyée

La fonction bouton PlayPauseStop exige que vous définissiez l’emplacement de l’image Push pour l’État tertiaire du bouton. Il s’agit de l’image que les utilisateurs voient quand ils poussent le bouton PlayPauseStop lors de la diffusion en continu d’une diffusion en direct.

Pour définir cette image, vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace. Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées de l’angle supérieur gauche (en pixels) de l’image à utiliser dans le type de bitmap à partir duquel vous dessinez.

Par exemple, pour définir l’image faisant l’objet d’un push pour une source d’image tertiaire, si votre image est à l’intérieur de la bitmap push, tapez :


```C++
Pushed @ 324,0

```



Les États tertiaires ne peuvent pas avoir d’image désactivée. Les images tertiaires sont supposées avoir la même largeur et la même hauteur que les images primaires et secondaires.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Boutons**](buttons.md)
</dt> </dl>

 

 




