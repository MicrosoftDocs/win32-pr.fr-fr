---
title: Attribut Margin-Top VML
description: Attribut Margin-Top VML
ms.assetid: bce0c575-918a-45ea-a068-cfb6f4a16b1a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e42d86ba6e0fe05c2b0dff1f6d8bdabba0100fffee97d489fd59360cb8e13bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346395"
---
# <a name="vml-margin-top-attribute"></a>Attribut Margin-Top VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Spécifie le bord supérieur du rectangle conteneur de la forme par rapport au point d’ancrage de la forme. En lecture/écriture. **Chaîne**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* margin-top = " *expression* " >

**Syntaxe du script**

*Element* . margin-top = "*expression*"

*expression* = *Element*. margin-top

**Remarques**

L’attribut **margin-top** est semblable à l’attribut de **marge HTML standard-Top** utilisé avec les feuilles de style.

Notez que **marginTop** est utilisé à la place de **margin-top** pour les scripts. Notez également que si la **position** est **absolue**, la marge n’apparaîtra pas pour changer.

cette propriété est utilisée à la place de **Top** pour les formes dans Microsoft Word et Microsoft Excel qui flottent dans une position par rapport à un point d’ancrage.

Ces valeurs comprennent :



| Valeur      | Description                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auto       | Position par défaut d’un élément dans le Flow de la page.                                                                                                                                           |
| units      | Par défaut. Nombre avec un indicateur d’unités absolues (cm, mm, in, PT, PC ou px) ou un indicateur d’unités relatives (em ou ex). Si aucune unité n’est donnée, les pixels (PX) sont pris en compte. La valeur par défaut est 0. |
| percentage | Valeur exprimée sous la forme d’un pourcentage de la hauteur de l’objet parent.                                                                                                                                    |



 

*Attribut standard VML*

**Voir aussi**

[Unités](msdn-online-vml-units.md)

**Exemple**

La marge supérieure est définie sur 25 pixels.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-top:25px">
   </v:rect>
```



[Exemple d’attribut margin-top](/previous-versions/bb264087(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 