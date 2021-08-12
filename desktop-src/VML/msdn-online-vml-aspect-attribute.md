---
title: Attribut aspect VML
description: Attribut aspect VML
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669b0f93e740e6bc4d4fb94155f6ca0ab60d5e00cebfb1604d5272d45d4dd8ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602896"
---
# <a name="vml-aspect-attribute"></a>Attribut aspect VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Spécifie la manière dont les proportions de l’image de remplissage sont conservées. En lecture/écriture. **Chaîne**.

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *élément* aspect = « *expression* » >

**Syntaxe du script**

*Element* . aspect = "*expression*"

*expression* = *Element*. aspect

**Remarques**

Ces valeurs comprennent :



| Valeur   | Description                           |
|---------|---------------------------------------|
| ignore  | Ignorer les problèmes d’aspect. Par défaut.        |
| au moins | L’image est au moins aussi grande que la **taille**. |
| atmost  | L’image n’est pas supérieure à la **taille**.     |



 

*Attribut standard VML*

**Exemple**

L’image qui compose le remplissage est supérieure ou égale à une taille de 10 points de 10 points.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 