---
title: Utilisation de l’élément Handles
description: Utilisation de l’élément Handles
ms.assetid: d748f74c-40e5-499a-bb61-94862eb3811c
keywords:
- Atelier Web, élément Handles
- conception de pages Web, Handles, élément
- Langage VML (VML), Handles (élément)
- VML (langage VML), élément Handles
- Vector Graphics, Handles, élément
- élément Handles
- Éléments VML, Handles
- Formes VML, élément Handles
- Langage VML (VML), attacher du texte à des formes
- VML (langage VML), attacher du texte à des formes
- graphiques vectoriels, attacher du texte à des formes
- Formes VML, joindre du texte
- attacher du texte à des formes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d504024a3d5c42caf8af116a08e5bd8787905991f14c4181fe3a75b10f4814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057204"
---
# <a name="using-the-handles-element"></a>Utilisation de l’élément Handles

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Dans cette rubrique, nous allons vous montrer comment utiliser l' `<handles>` élément pour attacher du texte à une forme.

Vous pouvez placer le `<handles>` sous-élément à l’intérieur de `<shape>` ou `<shapetype>` pour définir des éléments d’interface utilisateur qui peuvent faire varier les valeurs d' **ajustement** sur la forme.

Par exemple, comme illustré dans la représentation VML suivante, vous pouvez fournir une poignée d’ajustement (zone jaune) que les utilisateurs peuvent simplement faire glisser pour ajuster la forme.

remarque : les descripteurs sont disponibles lorsque cette forme VML est affichée dans Microsoft Office applications, où la forme est destinée à être manipulablee.

![shape1.gif (564 octets)](images/shape1h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="16200,5400"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Notez que la seule différence entre la représentation VML précédente et la seule qui suit est la valeur **Adj** .

![shape2.gif (1361 octets)](images/shape2h.gif)


```HTML
<v:shape style='width:90pt;height:54pt;'strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="11304,6600"
path="m@0,0l@0@1,0@1,0@2@0@2@0,21600,21600,10800xe">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="val #1"/>
<v:f eqn="sum height 0 #1"/>
<v:f eqn="sum 10800 0 #1"/>
<v:f eqn="sum width 0 #0"/>
<v:f eqn="prod @4 @3 10800"/>
<v:f eqn="sum width 0 @5"/>
</v:formulas>
<v:handles>
<v:h position="#0,#1" xrange="0,21600" yrange="0,10800"/>
</v:handles>
</v:shape>
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858393) .

 

 