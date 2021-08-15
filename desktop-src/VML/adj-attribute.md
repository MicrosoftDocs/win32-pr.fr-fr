---
title: Adj (attribut)
description: Adj (attribut)
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85869500cc3e9f86e0f48e67f63cfd9e6ed2cff5580caa04994169a9e4b50df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137142"
---
# <a name="adj-attribute"></a>Adj (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Spécifie une valeur d’ajustement utilisée pour définir les valeurs d’une formule. En lecture/écriture. **Chaîne**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *élément* adj = " *expression* " >

**Syntaxe du script**

*Element* . adj = "*expression*"

*expression* = *élément*. adj

**Remarques**

**Adj** est utilisé pour fournir des points réglables pour une formule. S’il est utilisé dans les balises, **Adj** est une chaîne délimitée par des virgules pouvant comporter jusqu’à 8 valeurs. Certaines valeurs peuvent être omises. Par exemple, « 0, 1, 2,, 4, 5,, 7 » serait une chaîne valide, alors que les quatrième et septième éléments n’auraient pas de valeurs (les éléments sont comptés à partir de 0).

Pour les scripts, **Adj** utilise le type de données [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md) .

*Attribut standard VML*

**Voir aussi**

[Formule](msdn-online-vml-formulas-element.md)

**Exemple**

Un carré simple est créé avec des ajustements. Tout d’abord, la chaîne **Adj** est créée pour définir huit valeurs d’ajustement. Ensuite, chaque valeur d’ajustement est référencée par l’une des huit formules, chaque valeur d’ajustement étant précédée d’un symbole dièse ( \# ). Enfin, un chemin d’accès est défini par une chaîne qui fait référence aux formules, chaque formule étant précédée du symbole arobase (@).


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



[Exemple d’attribut Adj](/previous-versions/bb229662(v=vs.85)) (nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 