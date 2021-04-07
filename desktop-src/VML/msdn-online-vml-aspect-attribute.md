---
title: Attribut aspect VML
description: Attribut aspect VML
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728333"
---
# <a name="vml-aspect-attribute"></a>Attribut aspect VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Spécifie la manière dont les proportions de l’image de remplissage sont conservées. En lecture/écriture. **Chaîne**.

**S’applique à**

[Complète](msdn-online-vml-fill-element.md)

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



 

 