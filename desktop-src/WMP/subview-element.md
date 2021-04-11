---
title: Subview, élément
description: Subview, élément
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Apparences du lecteur Windows Media, élément de sous-affichage
- Skins, subview, élément
- Subview, élément
- référence pour les apparences, élément de sous-affichage
- éléments, sous-affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310970"
---
# <a name="subview-element"></a>Subview, élément

L’élément de sous- **affichage** permet de manipuler une partie d’une apparence, par exemple pour fournir un panneau de configuration qui peut être masqué lorsqu’il n’est pas utilisé. Les éléments de la sous- **vue** sont toujours des enfants des éléments d' **affichage** parents et peuvent contenir d’autres éléments d’apparence, à l’exception de la **vue**, du **thème** et d’autres éléments de la sous- **vue** .

L’élément **subview** prend en charge les attributs suivants, qui sont définis sous l’élément **View** .



| Attribut                                                       | Description                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)                     | Spécifie ou récupère la couleur d’arrière-plan du contrôle de sous- **affichage** . La valeur par défaut est « None ».        |
| [backgroundImage](view-backgroundimage.md)                     | Spécifie ou récupère l’image d’arrière-plan du contrôle de sous- **affichage** .                                     |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Spécifie ou récupère la valeur de décalage de la teinte de l’image d’arrière-plan.                      |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Spécifie ou récupère la valeur de saturation de l’image d’arrière-plan.                                        |
| [backgroundTiled](view-backgroundtiled.md)                     | Spécifie ou récupère une valeur indiquant si l’image d’arrière-plan du contrôle de sous- **affichage** est affichée en mosaïque. |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Spécifie ou récupère une valeur indiquant si l’image d’arrière-plan peut être redimensionnée.                      |
| [Transparente](view-transparencycolor.md)                 | Spécifie ou récupère la couleur de transparence de l’image d’arrière-plan.                                      |



 

L’élément **subview** prend en charge les attributs ambiants, sauf indication contraire. Pour plus d’informations, consultez [attributs ambiants](ambient-attributes.md).

L’élément **subview** peut implémenter les gestionnaires d’événements ambiants suivants : [onendmove](onendmove.md) et [OnResize](onresize.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> <dt>

[**Élément VIEW**](view-element.md)
</dt> </dl>

 

 




