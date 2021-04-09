---
title: Utilisation de l’élément TextPath
description: Utilisation de l’élément TextPath
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Atelier Web, élément TextPath
- conception de pages Web, élément TextPath
- Langage VML (VML), élément TextPath
- VML (langage VML), élément TextPath
- Graphics Vector, élément TextPath
- élément TextPath
- Éléments VML, TextPath
- Formes VML, élément TextPath
- Langage VML (VML), dessin de texte
- VML (langage VML), dessin de texte
- graphiques vectoriels, dessiner du texte VML
- dessiner du texte
- Formes VML, dessiner du texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c032d14307dc07ec56911f4c5cc45a4c69664
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102264"
---
# <a name="using-the-textpath-element"></a>Utilisation de l’élément TextPath

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Dans cette rubrique, nous allons vous montrer comment utiliser l' `<textpath>` élément pour dessiner du texte avec différents styles.

Vous pouvez placer le `<textpath>` sous-élément à l’intérieur `<shape>` ou `<shapetype>` pour dessiner du texte. Vous pouvez ensuite utiliser les attributs de propriété du `<textpath>` sous-élément pour personnaliser le texte. Vous pouvez également utiliser le `<formulas>` sous-élément pour définir le contour du texte.

Par exemple, pour créer le texte affiché dans l’image suivante, vous pouvez taper la représentation VML ci-dessous. Notez que nous utilisons l' `<shapetype>` élément pour définir un prototype pour le contour du texte. Nous instancions ensuite deux formes à partir du même Typedeforme. Vous pouvez simplement modifier l’attribut de propriété de **chaîne** pour afficher un texte différent.

![Shape1 \-1.gif (4898 octets)](images/shape1-1t.gif)

![Shape1 \-2.gif (2789 octets)](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858398) .

 

 