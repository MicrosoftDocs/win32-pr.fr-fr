---
title: ShadowOK VML (attribut)
description: ShadowOK VML (attribut)
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce851a8e6d6bf458213521248cee05d3beb3d32dd6b235b93dd666a4c75051
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099099"
---
# <a name="vml-shadowok-attribute"></a>ShadowOK VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 