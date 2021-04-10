---
title: Attribut Focus VML
description: Attribut Focus VML
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031835"
---
# <a name="vml-focus-attribute"></a>Attribut Focus VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le centre d’un remplissage dégradé linéaire. En lecture/écriture. **VgFraction**.

**S’applique à**

[Complète](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : Focus sur l' *élément* = « *expression* » >

**Syntaxe du script**

*Element* . Focus = "*expression*"

*expression* = *élément*. Focus

**Remarques**

Définit la position de départ du centre de la fusion. Les valeurs sont comprises entre 100% et-100%. La valeur par défaut est 0. Une valeur de 100% (ou-100%) déplace le focus de manière à ce que la direction du lissage soit inversée (en effet, inversement **couleur** et **Color2**). Une valeur de 50% change la fusion afin que la **couleur** soit aux deux extrémités et que la couleur **Color2** soit au milieu. La valeur-50% change la fusion afin que **Color2** soit aux deux extrémités et que la **couleur** soit au milieu.

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



 

 