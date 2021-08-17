---
title: StrokeOK VML (attribut)
description: StrokeOK VML (attribut)
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5051f3a2d5e7ac8e4d509d8b8f65182f86799db41bbd8a4d71741961c3a1e406
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475219"
---
# <a name="vml-strokeok-attribute"></a>StrokeOK VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si un trait sera affiché. En lecture/écriture. **VgTriState**.

**S’applique à**

[Chemin d’accès](msdn-online-vml-path-element.md)

**Syntaxe de balise**

<v : *Element* strokeok = " *expression* " >

**Syntaxe du script**

*Element* . strokeok = "*expression*"

*expression* = *élément*. strokeok

**Remarques**

Si la **valeur est false**, le tracé ne peut pas être rayé. La valeur par défaut est **True**. Cet attribut remplace tous les autres attributs de trait dans l’élément parent ou **Stroke** .

*Attribut standard VML*

**Exemple**

Le chemin d’accès ne sera pas rayé.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 