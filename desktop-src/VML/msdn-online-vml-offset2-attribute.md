---
title: Offset2 VML (attribut)
description: Offset2 VML (attribut)
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc06b68f075b139f6822a38672b8530fc2172071aab35072659968725d9866b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124222"
---
# <a name="vml-offset2-attribute"></a>Offset2 VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine un deuxième offset. En lecture/écriture. **VgVector2D**.

**S’applique à**

[Shadow](msdn-online-vml-shadow-element.md)

**Syntaxe de balise**

<v : *Element* offset2 = " *expression* " >

**Syntaxe du script**

*Element* . offset2 = "*expression*"

*expression* = *élément*. offset2

**Remarques**

La valeur par défaut d’un deuxième décalage pour la valeur x est 0 et la valeur par défaut de la valeur y est 0. Les valeurs sont soit une mesure absolue, soit une valeur fractionnaire de forme. Si fractionnaires, les valeurs sont comprises entre 50% et-50%.

Utilisez un deuxième décalage pour créer des effets d’ombre spéciaux. Pour plus d’informations sur les deux décalages, consultez l’attribut [type](type-attribute--shadow--vml.md) .

*Attribut standard VML*

**Exemple**

Une double ombre est créée pour la forme.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 