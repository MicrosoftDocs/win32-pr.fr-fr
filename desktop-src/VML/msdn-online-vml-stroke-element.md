---
title: VML Stroke, élément
description: VML Stroke, élément
ms.assetid: 300ecde5-f19d-4ff7-89a4-af9b8e82ae9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34fa3b8293c8d540af47578ac522ff1cde179d8858c4f1e16aa95a0cd6e635e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513209"
---
# <a name="vml-stroke-element"></a>VML Stroke, élément

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit un trait pour une forme.

Les attributs suivants modifient un trait.



| Attribut                                                          | Description                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------|
| [AltHRef](althref-attribute--stroke--vml.md)                      | Spécifie une autre référence pour un trait.                |
| [Couleur](color-attribute--stroke--vml.md)                          | Définit la couleur d’un trait.                                |
| [Couleur2](color2-attribute--stroke--vml.md)                        | Définit une deuxième couleur pour un trait.                          |
| [DashStyle](msdn-online-vml-dashstyle-attribute.md)               | Spécifie le motif de point et de tiret pour un trait.              |
| [EndArrow](msdn-online-vml-endarrow-attribute.md)                 | Définit un style de flèche pour la fin d’un trait.           |
| [EndArrowLength](msdn-online-vml-endarrowlength-attribute.md)     | Définit une longueur de flèche pour la fin d’un trait.          |
| [EndArrowWidth](msdn-online-vml-endarrowwidth-attribute.md)       | Définit une largeur de flèche pour la fin d’un trait.           |
| [Extrem](msdn-online-vml-endcap-attribute.md)                     | Définit le style d’extrémité pour la fin d’un trait.                |
| [FillType](msdn-online-vml-filltype-attribute.md)                 | Définit le type de remplissage utilisé pour l’arrière-plan d’un trait. |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229431(v=vs.85))    | Définit l’URL de l’image d’origine du trait.         |
| [Identifiant](id-attribute--stroke--vml.md)                                | Définit un identificateur unique pour le trait.                   |
| [ImageAlignShape](msdn-online-vml-imagealignshape-attribute.md)   | Détermine l’alignement d’une image de trait.                   |
| [ImageAspect](msdn-online-vml-imageaspect-attribute.md)           | Définit la manière dont les proportions de l’image du trait sont conservées.  |
| [ImageSize](msdn-online-vml-imagesize-attribute.md)               | Définit la taille de l’image pour le trait.                 |
| [JoinStyle](msdn-online-vml-joinstyle-attribute.md)               | Définit le style de jointure d’une polyligne.                         |
| [LineStyle](msdn-online-vml-linestyle-attribute.md)               | Définit le style de ligne d’un trait.                           |
| [MiterLimit](msdn-online-vml-miterlimit-attribute.md)             | Définit le lissage d’un joint mitre.                      |
| [Activé](on-attribute--stroke--vml.md)                                | Détermine si le trait sera affiché.              |
| [Opacity](opacity-attribute--stroke--vml.md)                      | Définit la quantité de transparence d’un trait.               |
| [Sources](src-attribute--stroke--vml.md)                              | Définit l’image source à charger pour un remplissage de trait.           |
| [StartArrow](msdn-online-vml-startarrow-attribute.md)             | Définit la pointe de flèche pour le début d’un trait.              |
| [StartArrowLength](msdn-online-vml-startarrowlength-attribute.md) | Définit la longueur de la flèche pour le début d’un trait.       |
| [StartArrowWidth](msdn-online-vml-startarrowwidth-attribute.md)   | Définit la largeur de la flèche pour le début d’un trait.        |
| [Titre](title-attribute--stroke--vml.md)                          | Définit le titre d’un trait.                                |
| [Poids](msdn-online-vml-weight-attribute.md)                     | Définit l’épaisseur d’un trait.                            |



 

**Remarques**

Cet élément doit être défini dans un élément [Shape](shape-element--vml.md) .

Le code suivant montre comment l’élément **Stroke** peut être utilisé pour modifier une ligne.


```HTML
   <v:line
   to="300pt,50pt" from="50pt,50pt">
   <v:stroke weight="50pt" color="red" linestyle="ThickThin"/>
   </v:line>
```



**Exemples**

-   [Exemple de trait simple](/previous-versions/bb229466(v=vs.85))
-   [Exemple d’image de trait](/previous-versions/bb229468(v=vs.85))

 

 