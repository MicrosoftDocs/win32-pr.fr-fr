---
title: VML VMLFrame, élément
description: VML VMLFrame, élément
ms.assetid: a1582223-d6e2-42d1-95bb-97f6f1d453d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f53371afb0c2790ff6dd666f0121b30b586c51b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101748"
---
# <a name="vml-vmlframe-element"></a>VML VMLFrame, élément

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit un cadre pour une forme externe.

Les attributs suivants modifient un frame.



| Attribut                                     | Description                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------|
| [Capture](msdn-online-vml-clip-attribute.md)    | Détermine si l’image sera découpée.                         |
| [Identifiant](id-attribute--vmlframe--vml.md)         | Définit un identificateur unique pour le frame.                            |
| [Origine](origin-attribute--vmlframe--vml.md) | Spécifie l’origine du frame.                                    |
| [Taille](size-attribute--vmlframe.md)          | Spécifie la taille du frame.                                      |
| [Sources](src-attribute--vmlframe--vml.md)       | Spécifie la source des données qui seront affichées dans le frame. |
| [Style](msdn-online-vml-style-attribute.md)  | Définit les styles CSS normaux qui peuvent être utilisés pour positionner le cadre. |



 

**Remarques**

Les données sources à afficher dans le frame peuvent être contenues dans la même page Web ou faire partie d’une autre page. Grâce aux scripts, la source peut être modifiée dynamiquement et les caractéristiques d’affichage peuvent être modifiées.

Les objets à l’intérieur du **VMLFrame** sont « zoom mis à l’échelle ». Autrement dit, elles sont mises à l’échelle comme des sous-fichiers, où les poids de ligne, les décalages d’ombre et les zones de texte sont tous mis à l’échelle proportionnellement. Cela est différent d’un groupe, où la taille et la position de l’objet sont mises à l’échelle proportionnellement, contrairement à Line, Shadow, etc.

Voici le code minimal requis pour charger une image dans un frame.


```HTML
   <v:vmlframe
     style="top:1;left:1;width:50;height:50">
     src="external.vml#rect01"/>
   </v:vmlframe>
```



Si le fichier est externe, il doit s’agir d’un fichier XML. Le code suivant est le code minimal nécessaire pour spécifier un fichier source externe qui doit contenir une forme identifiable. Cet exemple contient une forme d’image qui affiche une image bitmap.


```HTML
   <xml xmlns:v = "urn:schemas-microsoft-com:vml">
   <v:image id="rect01"
     style="height:100;width:100;top:50;left:50">
     src="kids.jpg">
   </v:rect>
   </xml>
```



> [!Note]  
> Dans les versions préliminaires de VML, cet élément était appelé **VMLCanvas** .

 

**Exemples**

-   [Exemple de VMLFrame simple](/previous-versions/bb263920(v=vs.85))
-   [Exemple de VMLFrame dynamique](/previous-versions/bb263902(v=vs.85))

 

 