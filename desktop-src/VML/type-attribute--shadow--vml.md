---
title: Attribut type (Shadow) (VML)
description: Attribut type (Shadow) (VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d90a264cbaf77890e39f10d56103c8acdc84727de21d7f2de9946911b6df41dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513159"
---
# <a name="type-attribute-shadowvml"></a>Attribut type (Shadow) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Spécifie le type d’ombre. En lecture/écriture. **Chaîne**.

**S’applique à**

[Shadow](msdn-online-vml-shadow-element.md)

**Syntaxe de balise**

<v : type d' *élément* = « *expression* » >

**Syntaxe du script**

*Element* . type = "*expression*"

*expression* = *Element*. type

**Remarques**

Ces valeurs comprennent :



| Valeur           | Description                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| unique          | Ombre unique. Par défaut.                                                                                                                                                                              |
| double          | Ombre double. [Color2](color2-attribute--shadow--vml.md) est utilisé pour la couleur de la deuxième ombre et [Offset2](msdn-online-vml-offset2-attribute.md) est utilisé pour le décalage de la deuxième ombre. |
| perspective     | Ombre de perspective.                                                                                                                                                                                |
| shapeRelative   | L’ombre est créée par rapport à la forme.                                                                                                                                                         |
| drawingRelative | L’ombre est créée par rapport au dessin.                                                                                                                                                       |
| gaufrage          | L’ombre a un aspect en relief.                                                                                                                                                                     |



 

**Attribut standard VML**

**Exemple**

Une double ombre est créée avec le deuxième vert de l’ombre et le décalage de 5 points vers le point et vers la droite.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 