---
title: Élément ImageData VML
description: Élément ImageData VML
ms.assetid: 91004646-b031-4973-a32d-7afdd10dab48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3a307dd36daf0ff08d2fab7cd9086a3bc07447872cf36cb41972e4aa5a4d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600290"
---
# <a name="vml-imagedata-element"></a>Élément ImageData VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit une image pour une forme.

Les attributs suivants modifient une image.



| Attribut                                                          | Description                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| [AltHRef](althref-attribute--imagedata--vml.md)                   | Spécifie une autre référence pour une image.                        |
| [Anticrénelage](msdn-online-vml-bilevel-attribute.md)                   | Détermine si une image s’affichera en noir et blanc.          |
| [BlackLevel](msdn-online-vml-blacklevel-attribute.md)             | Détermine l’intensité du noir dans une image.                        |
| [Chromakey](msdn-online-vml-chromakey-attribute.md)               | Définit la couleur de la palatte qui sera traitée comme transparente. |
| [CropBottom](msdn-online-vml-cropbottom-attribute.md)             | Définit le pourcentage de suppression d’image du côté inférieur.       |
| [CropLeft](msdn-online-vml-cropleft-attribute.md)                 | Définit le pourcentage de suppression d’image du côté gauche.         |
| [CropRight](msdn-online-vml-cropright-attribute.md)               | Définit le pourcentage de suppression d’image du côté droit.        |
| [CropTop](msdn-online-vml-croptop-attribute.md)                   | Définit le pourcentage de suppression d’image du côté supérieur.          |
| [DetectMouseClick](detectmouseclick-attribute--imagedata--vml.md) | Détermine si un clic de souris sera détecté.                    |
| [EmbossColor](msdn-online-vml-embosscolor-attribute.md)           | Définit la couleur des effets de couleur en relief.                         |
| [Maîtrise](msdn-online-vml-gain-attribute.md)                         | Définit l’intensité de toutes les couleurs d’une image.                      |
| [Gamma](msdn-online-vml-gamma-attribute.md)                       | Définit la quantité de contraste pour une image.                          |
| [Semble](msdn-online-vml-grayscale-attribute.md)               | Détermine si une image s’affichera en mode nuances de gris.          |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Définit une URL pour une image.                                           |
| [Identifiant](id-attribute--image--vml.md)                                 | Définit un identificateur unique pour une image.                             |
| [Film](msdn-online-vml-movie-attribute.md)                       | Définit un pointeur vers une image de film.                                   |
| [OLEID](msdn-online-vml-oleid-attribute.md)                       | Stocke l’ID OLE d’une image.                                        |
| [Sources](src-attribute--imagedata--vml.md)                           | Définit une source pour l’image.                                       |
| [Titre](title-attribute--imagedata--vml.md)                       | Définit le titre d’une image.                                        |



 

**Remarques**

Cet élément doit être défini dans un élément [Shape](shape-element--vml.md) .

En outre, l’attribut [**src**](src-attribute--imagedata--vml.md) doit pointer vers une image.

Voici le code minimal nécessaire pour générer une image.


```HTML
   <v:rect
   style="position:relative;top:1;left:1;width:50;height:50">
   <v:imagedata src="../art/kids.jpg"/>
   </v:rect>
```



> [!Note]  
> Dans les versions préliminaires de VML, cet élément était appelé **image** .

 

**Exemples**

-   [Exemple de ImageData simple](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/t_image.md)
-   [Exemple de ImageData dynamique](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/x_image.md)

 

 