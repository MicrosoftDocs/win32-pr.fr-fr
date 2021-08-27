---
title: Specularity VML (attribut)
description: Specularity VML (attribut)
ms.assetid: df04c15c-cfad-4172-81fa-a28e13f205fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b44cc9e8d266ba5ca9c7acb960425d7d4b246145c2d29ba0cc23f668d4aa24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098939"
---
# <a name="vml-specularity-attribute"></a>Specularity VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le specularity d’une forme extrudée. En lecture/écriture. **VgNumber**.

**S’applique à**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Syntaxe de balise**

<o : *Element* specularity = " *expression* " >

**Syntaxe du script**

*Element* . specularity = "*expression*"

*expression* = *élément*. specularity

**Remarques**

Cette valeur définit le rapport entre l’incident et la lumière modèle éclairé réfléchie. Les valeurs normales sont comprises entre 0 et 1. La valeur par défaut est 0.

Si les valeurs supérieures à 1 sont spécifiées, des effets inhabituels peuvent se produire.

Microsoft Office Attribut extensions

 

 