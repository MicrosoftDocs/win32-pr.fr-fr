---
title: Color2, attribut (Stroke) (VML)
description: Color2, attribut (Stroke) (VML)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108c767f7337f486f8b7df5a4506b3b3d487dabf146656890def0c5e1ad32a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867429"
---
# <a name="color2-attribute-strokevml"></a>Color2, attribut (Stroke) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit une deuxième couleur pour les traits. En lecture/écriture. **Chaîne**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *élément* color2 = « *expression* » >

Syntaxe du script

*Element* . color2 = "*expression*"

*expression* = *élément*. color2

**Remarques**

Une deuxième couleur est utilisée lorsque le type de remplissage d’un trait est un modèle.

*Attribut standard VML*

**Exemple**

Le trait de la forme est un motif de remplissage dans lequel le remplissage est défini par l’image source, mais l’arrière-plan transparent est défini par la deuxième couleur.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 