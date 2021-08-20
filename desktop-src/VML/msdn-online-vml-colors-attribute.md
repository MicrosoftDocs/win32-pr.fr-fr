---
title: Attribut des couleurs VML
description: Attribut des couleurs VML
ms.assetid: 466ed1d7-8861-44db-bd96-a2fd119b12f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a699b0ab8da898dd82fa4e1bf4823c0f9fdd443eb8275e25dbfaac6d2f039a6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999279"
---
# <a name="vml-colors-attribute"></a>Attribut des couleurs VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit plusieurs couleurs pour un remplissage dégradé. En lecture/écriture. **IVgGradientColorArray**.

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *Element* Colors = " *expression* " >

**Syntaxe du script**

*Element* . Colors = "*expression*"

*expression* = *Element*. couleurs

**Remarques**

Utilisé pour définir un tableau constitué de valeurs jumelées de pourcentages ([VgFraction](msdn-online-vml-vgfraction-data-type.md)) et de couleurs ([VgColor](msdn-online-vml-ivgcolor.md)). Le tableau crée un remplissage fusionné à l’aide de chaque point du tableau, en commençant à 0% (défini par la **couleur**) et en se terminant à 100% (défini par **Color2**). Les couleurs intermédiaires peuvent être définies en affectant une valeur de couleur à un pourcentage. Les paires pourcentage et couleur ne sont pas séparées par une virgule, mais les paires sont séparées par des virgules.

Attribut standard VML

**Exemple**

La forme a un remplissage dégradé constitué de quatre couleurs, en commençant par la couleur rouge, en utilisant la couleur jaune, puis en vert et en finallyblue.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   colors="30% yellow,70% green"/>
   </v:shape>
```



 

 