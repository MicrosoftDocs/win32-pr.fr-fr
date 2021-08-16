---
title: Attribut Focus VML
description: Attribut Focus VML
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b60eeb9ff379c8006cbb9068b6b78c8f24490ecf2fd15573b5b224a9ee1208ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057867"
---
# <a name="vml-focus-attribute"></a>Attribut Focus VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le centre d’un remplissage dégradé linéaire. En lecture/écriture. **VgFraction**.

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : Focus sur l' *élément* = « *expression* » >

**Syntaxe du script**

*Element* . Focus = "*expression*"

*expression* = *élément*. Focus

**Remarques**

Définit la position de départ du centre de la fusion. Les valeurs sont comprises entre 100% et-100%. La valeur par défaut est 0. Une valeur de 100% (ou-100%) déplace le focus afin que la direction de la fusion soit inversée (en effet, en inversant la **couleur** et le **Color2**). Une valeur de 50% change la fusion afin que la **couleur** soit aux deux extrémités et que la couleur **Color2** soit au milieu. La valeur-50% change la fusion afin que **Color2** soit aux deux extrémités et que la **couleur** soit au milieu.

*Attribut standard VML*

**Exemple**

Le focus dégradé du remplissage est décalé de sorte que le rouge (**couleur**) soit une bande au centre de la forme et que le haut et le bas soient bleus (**Color2**).


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 