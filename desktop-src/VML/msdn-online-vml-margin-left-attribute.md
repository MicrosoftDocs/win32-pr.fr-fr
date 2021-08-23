---
title: Attribut Margin-Left VML
description: Attribut Margin-Left VML
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f403c19e617f8131886d3f4a862ff1ac0b878edbd2acf2fd0e27cb17b3406c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680819"
---
# <a name="vml-margin-left-attribute"></a>Attribut Margin-Left VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Spécifie le bord gauche du rectangle conteneur de la forme par rapport au point d’ancrage de la forme. En lecture/écriture. **Chaîne**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "margin-left : *expression* " >

**Syntaxe du script**

*Element* . style. MarginLeft = "*expression*"

*expression* = *Element*. style. MarginLeft

**Remarques**

L’attribut **margin-left** est semblable à l’attribut de **marge HTML standard-Left** utilisé avec les feuilles de style.

Notez que la procédure **MarginLeft** est utilisée à la place de la **marge gauche** pour les scripts. Notez également que si la **position** est **absolue**, la marge n’apparaîtra pas pour changer.

cette propriété est utilisée à la place de **Left** pour les formes dans Microsoft Word et Microsoft Excel qui flottent dans une position par rapport à un point d’ancrage.

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

La marge de gauche est définie à 25 pixels.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-left:25px">
   </v:rect>
```



[Exemple d’attribut margin-left](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 