---
title: Élément de tracé VML
description: Élément de tracé VML
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1de9440761479d6b3dc6cb10c96b00ea48626247
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510071"
---
# <a name="vml-path-element"></a>Élément de tracé VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit un chemin d’accès pour une forme.

Les attributs suivants modifient une ombre.



| Attribut                                                        | Description                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Arrowok](msdn-online-vml-arrowok-attribute.md)                 | Détermine si les flèches sont affichées.                                |
| [ConnectAngles](msdn-online-vml-connectangles-attribute.md)     | Spécifie la manière dont une courbe se connecte à un point de connexion.                       |
| [ConnectLocs](msdn-online-vml-connectlocs-attribute.md)         | Définit l’emplacement des points de connexion sur un chemin d’accès.                            |
| [ConnectType](msdn-online-vml-connecttype-attribute.md)         | Définit le type de point de connexion utilisé pour attacher des formes à d’autres formes. |
| [ExtrusionOK](msdn-online-vml-extrusionok-attribute.md)         | Détermine si une extrusion sera affichée.                              |
| [FillOK](msdn-online-vml-fillok-attribute.md)                   | Détermine si un remplissage est affiché.                                    |
| [GradientShapeOK](msdn-online-vml-gradientshapeok-attribute.md) | Détermine si une forme de dégradé sera affichée.                          |
| [Identifiant](id-attribute--path--vml.md)                                | Définit un identificateur unique pour un chemin d’accès.                                         |
| [Limo](msdn-online-vml-limo-attribute.md)                       | Définit un point d’étirement sur le tracé.                                            |
| [ShadowOK](msdn-online-vml-shadowok-attribute.md)               | Détermine si une ombre sera affichée.                                  |
| [StrokeOK](msdn-online-vml-strokeok-attribute.md)               | Détermine si un trait sera affiché.                                  |
| [TextBoxRect](msdn-online-vml-textboxrect-attribute.md)         | Définit une ou plusieurs zones de texte à l’intérieur d’une forme.                                   |
| [TextPathOK](msdn-online-vml-textpathok-attribute.md)           | Détermine si un TextPath sera affiché.                                |
| [V](msdn-online-vml-v-attribute.md)                             | Définit les commandes qui composent un chemin d’accès.                                       |



 

**Remarques**

Cet élément doit être défini dans un élément [Shape](shape-element--vml.md) .

Le code suivant montre comment définir une forme avec un chemin d’accès.


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



Notez que l’attribut [V](msdn-online-vml-v-attribute.md) de **path** remplace l’attribut [path](msdn-online-vml-path-attribute.md) de [Shape](shape-element--vml.md).

**Exemples**

-   [Exemple d’élément enfant Path simple](/previous-versions/bb229545(v=vs.85))
-   [Exemple d’élément enfant Dynamic Path](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 