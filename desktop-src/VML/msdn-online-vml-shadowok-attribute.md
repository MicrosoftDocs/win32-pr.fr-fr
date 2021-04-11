---
title: ShadowOK VML (attribut)
description: ShadowOK VML (attribut)
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e6b4ca6b98ce66208e906c45fd560324121e8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031273"
---
# <a name="vml-shadowok-attribute"></a>ShadowOK VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si une ombre sera affichée. En lecture/écriture. **VgTriState**.

**S’applique à**

[Chemin d’accès](msdn-online-vml-path-element.md)

**Syntaxe de balise**

<v : *Element* shadowok = " *expression* " >

**Syntaxe du script**

*Element* . shadowok = "*expression*"

*expression* = *élément*. shadowok

**Remarques**

Si la **valeur est false**, le chemin d’accès ne peut pas avoir d’ombre. La valeur par défaut est **True**. Cet attribut remplace tous les autres attributs fantômes dans l’élément parent ou le **cliché instantané** .

*Attribut standard VML*

**Exemple**

La forme n’a pas d’ombre.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True" offset="5pt,5pt" color="blue"/>
   <v:path id= "myPath" shadowok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 