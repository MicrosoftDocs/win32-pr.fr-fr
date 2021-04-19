---
title: Color2, attribut (Fill) (VML)
description: Color2, attribut (Fill) (VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106538599"
---
# <a name="color2-attribute-fillvml"></a>Color2, attribut (Fill) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit une deuxième couleur pour les remplissages. En lecture/écriture. [VgColor](msdn-online-vml-ivgcolor.md) .

**S’applique à**

[Complète](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *élément* color2 = « *expression* » >

**Syntaxe du script**

*Element* . color2 = "*expression*"

*expression* = *élément*. color2

**Remarques**

Une deuxième couleur est utilisée lorsqu’un type de remplissage est un modèle ou un dégradé. La valeur par défaut est **blanc**.

*Attribut standard VML*

**Exemple**

Le type de remplissage de la forme est un modèle dans lequel le remplissage de premier plan est défini par l’image source, mais l’arrière-plan transparent est défini par la deuxième couleur.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 