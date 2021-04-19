---
title: Position, attribut (H) (VML)
description: Position, attribut (H) (VML)
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513735"
---
# <a name="position-attribute-hvml"></a>Position, attribut (H) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Spécifie les valeurs thex et y du handle. **VgVector2D** en lecture/écriture.

**S’applique à**

[H](msdn-online-vml-h-element.md) (sous-élément de [Handles](msdn-online-vml-handles-element.md))

**Syntaxe de balise**

<v : *Element* position = " *expression* " >

**Remarques**

les valeurs x et y peuvent être de l’un des types suivants :

-   constant
-   formule (par exemple, @2 )
-   ajuster (par exemple, \# 3)
-   centre
-   côté gauche
-   telle

Si l’un des types ci-dessus sauf *Adjust* est spécifié, la position du handle est fixe dans cette dimension. Si une poignée d’ajustement est spécifiée, le descripteur est libre de se déplacer dans cette dimension et la valeur d’ajustement est déterminée par la position de la poignée.

Si un attribut [polaire](msdn-online-vml-polar-attribute.md) est spécifié, l’attribut **position** représente les valeurs de rayon et d’angle du handle au lieu de x et y.

La valeur par défaut est 0,0.

*Attribut standard VML*

 

 