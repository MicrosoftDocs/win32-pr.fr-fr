---
title: Source d’image tertiaire normale
description: Source d’image tertiaire normale
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Apparences mobiles du lecteur Windows Media, source de l’image du bouton
- apparences, source de l’image du bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, source d’image
- source d’image pour les apparences, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380235"
---
# <a name="normal-tertiary-image-source"></a>Source d’image tertiaire normale

La fonction bouton PlayPauseStop exige que vous définissiez l’emplacement de l’image normale pour l’État tertiaire du bouton. Il s’agit de l’image que les utilisateurs voient après avoir appuyé sur le bouton PlayPauseStop pour commencer à diffuser en continu une diffusion en direct.

Pour définir cette image, vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace. Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées de l’angle supérieur gauche (en pixels) de l’image à utiliser dans le type de bitmap à partir duquel vous dessinez.

Par exemple, pour définir l’image normale pour une source d’image tertiaire, si votre image est à l’intérieur de la bitmap push, tapez :


```C++
Pushed @ 286,0

```



Les États tertiaires ne peuvent pas avoir d’image désactivée. Les images tertiaires sont supposées avoir la même largeur et la même hauteur que les images primaires et secondaires.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Boutons**](buttons.md)
</dt> </dl>

 

 




