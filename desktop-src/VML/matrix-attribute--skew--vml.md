---
title: Attribut de matrice (skew) (VML)
description: Attribut de matrice (skew) (VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7fd3989807951f06df963c6899a2c81ce6e7faaa76432172e4391a4ce11029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768448"
---
# <a name="matrix-attribute-skewvml"></a>Attribut de matrice (skew) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit une transformation de perspective d’un skew. En lecture/écriture. **Chaîne**.

**S’applique à**

[Appliquez](msdn-online-vml-skew-element.md)

**Syntaxe de balise**

<o : *Element* Matrix = " *expression* " >

**Syntaxe du script**

*Element* . Matrix = "*expression*"

*expression* = *élément*. Matrix

**Remarques**

La matrice est une chaîne au format « Sxx, SXY, syx, SYY, PX, py » où s est Scale, p est perspective et x et y sont des valeurs x et y. Si le [décalage](offset-attribute--skew--vml.md) est en unités absolues, PX et PY sont en unités UME ^ [-1 (](msdn-online-vml-units.md) sinon, elles sont une fraction inverse de la taille de la forme). La valeur par défaut est « 1, 0, 0, 1, 0, 0 ».

*Microsoft Office Attribut extensions*

 

 