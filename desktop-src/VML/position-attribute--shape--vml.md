---
title: Position, attribut (Shape) (VML)
description: Position, attribut (Shape) (VML)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ffede6653fd865c254392ffbab0bc3feac2f5e0bf51046fc85398306842dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475075"
---
# <a name="position-attribute-shapevml"></a>Position, attribut (Shape) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le type de positionnement utilisé pour placer un élément. En lecture/écriture. **Chaîne**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "position : *expression* " >

**Syntaxe du script**

*Element* . style. position = "*expression*"

*expression* = *Element*. style. position

**Remarques**

L’attribut **position** est semblable à l’attribut **position** HTML standard utilisé avec les feuilles de style.

Ces valeurs comprennent :



| Valeur    | Description                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static   | Par défaut. L’élément est positionné en fonction du déroulement normal de la page. Les attributs **Top** et **Left** sont ignorés. si l’objet est ancré en ligne, ce qui se produit uniquement dans Microsoft Word, cette valeur est utilisée. |
| absolute | L’élément est positionné par rapport au parent, à l’aide des attributs **Top** et **Left** . cette valeur est utilisée par les Microsoft Word et Microsoft Excel les objets flottants et les diapositives Microsoft PowerPoint.                  |
| relative | L’élément est positionné en fonction du déroulement normal de la page, mais les attributs **supérieur** et **gauche** sont utilisés. Le chevauchement des éléments qui se chevauchent est régi par l’attribut **Z-index** .                       |



 

*Attribut standard VML*

**Exemple**

La position du rectangle est affichée à l’aide du style *relatif* .


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemple d’attribut position](/previous-versions/bb264090(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 