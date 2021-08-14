---
title: Attribut Margin-Right VML
description: Attribut Margin-Right VML
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5569f4f89cbe5320cfc348f2e2929b986736412f4cb864a62dd4584bde43a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346457"
---
# <a name="vml-margin-right-attribute"></a>Attribut Margin-Right VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Spécifie le bord droit du rectangle conteneur de la forme par rapport au point d’ancrage de la forme. En lecture/écriture. **Chaîne**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "margin-right : *expression* " >

**Syntaxe du script**

*Element* . style. marginRight = "*expression*"

*expression* = *Element*. style. marginRight

**Remarques**

L’attribut **margin-right** est semblable à l’attribut Margin HTML standard **-Right** utilisé avec les feuilles de style.

Notez que **marginRight** est utilisé à la place de **margin-right** pour les scripts. Notez également que si la **position** est **absolue**, la marge n’apparaîtra pas pour changer.

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

La marge de droite est définie à 25 pixels.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



[Exemple d’attribut margin-right](/previous-versions/bb229677(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 