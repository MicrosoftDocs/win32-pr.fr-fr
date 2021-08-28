---
title: Utilisation de l’élément Formulas
description: Utilisation de l’élément Formulas
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Web Workshop, élément Formulas
- conception de pages Web, élément Formulas
- Langage VML (VML), élément Formulas
- VML (langage VML), élément Formulas
- élément Graphics, Formulas
- élément Formulas
- Éléments VML, formules
- Formes VML, élément Formulas
- Langage VML (VML), définition des tracés pour les formes
- VML (langage VML), définition des tracés pour les formes
- graphiques vectoriels, définition des tracés pour les formes
- Formes VML, définition de chemins d’accès
- définition des tracés pour les formes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9db791533190cd2f67e1043e345954fe71de251
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885623"
---
# <a name="using-the-formulas-element"></a>Utilisation de l’élément Formulas

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Dans cette rubrique, nous allons vous montrer comment utiliser le `&lt;formulas&gt;` sous-élément pour définir un chemin d’accès réglable pour une forme.

Vous pouvez placer le &lt; &gt; sous-élément Formulas dans `<shape>` ou `<shapetype>` pour définir des formules qui peuvent varier le tracé d’une forme. Dans le `&lt;formulas&gt;` sous-élément, un sous-élément **f** définit une formule afin qu’une valeur soit évaluée en fonction de cette formule. Par exemple, la formule `<v:f eqn="prod 10 4 5"/>` définit une valeur qui est équivalente à « 10 x 4/5 ».

Vous pouvez placer un grand nombre de sous-éléments **f** dans un `&lt;formulas&gt;` sous-élément. Les formules peuvent référencer les valeurs définies précédemment dans d’autres formules au sein du même `&lt;formulas&gt;` sous-élément. La valeur définie dans la première formule peut être appelée @0 , mais la valeur définie dans la deuxième formule peut être appelée @1 , et ainsi de suite.

En outre, vous pouvez spécifier l’attribut de propriété **Adj** de l' `<shape>` élément, par exemple adj = "100, 200, 150". À l’intérieur de l' `&lt;formulas&gt;` élément, vous pouvez référencer ces valeurs dans la liste **Adj** . La première valeur (100) dans la liste **Adj** peut être appelée \# 0, la seconde valeur (200) peut être appelée \# 1, et ainsi de suite.

Par exemple, pour dessiner un visage souriant, vous pouvez taper la représentation VML suivante :

![shape1.gif (735 octets)](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   `adj="17520"` définit une valeur (= 17520). Cette valeur peut être référencée sous la forme \# 0.
-   La première formule, `<v:f eqn="sum 33030 0 #0"/>` , définit la valeur (= 33030 + 0- \# 0). Cette valeur peut être référencée en tant que @0 .
-   La deuxième formule, `<v:f eqn="prod #0 4 3"/>` , définit la valeur (= \# 0 \* 4/3). Cette valeur peut être référencée en tant que @1 .
-   La troisième formule, `<v:f eqn="prod @0 1 3"/>` , définit la valeur (= @0 \* 1/3). Cette valeur peut être référencée en tant que @2 .
-   La quatrième formule, `<v:f eqn="sum @1 0 @2"/>` , définit la valeur (= @1 + 0 -@2 ). Cette valeur peut être référencée en tant que @3 .
-   À l’intérieur de l' `<path>` élément, les valeurs définies dans les formules First ( @0 ) et quatrième ( @3 ) sont utilisées pour déterminer le contour de la forme.

Si vous modifiez la liste **Adj** , par exemple `adj="20000"` , les valeurs des formules qui font référence à la liste **Adj** sont également modifiées, ce qui affecte le visage souriant comme suit :

![shape2.gif (765 octets)](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858392) .

 

 
