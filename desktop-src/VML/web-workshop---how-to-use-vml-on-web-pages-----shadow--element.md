---
title: Utilisation de l’élément Shadow
description: Utilisation de l’élément Shadow
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Atelier Web, élément Shadow
- conception de pages Web, élément Shadow
- Langage VML (VML), élément Shadow
- VML (langage VML), élément Shadow
- graphiques vectoriels, élément Shadow
- élément Shadow
- Éléments VML, ombre
- Formes VML, élément Shadow
- Langage VML (VML), dessin avec des effets d’ombre
- VML (langage VML), dessin avec des effets d’ombre
- graphiques vectoriels, dessin avec des effets d’ombre
- Formes VML, dessin avec des effets d’ombre
- dessiner avec des effets d’ombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83be3f59eacfb495a2c80d212bc99cfd3d43be10aa8144eb68d3defd8a029e41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512593"
---
# <a name="using-the-shadow-element"></a>Utilisation de l’élément Shadow

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Dans cette rubrique, nous allons vous montrer comment utiliser le `<shadow>` sous-élément pour dessiner une forme qui a divers effets d’ombre.

Vous pouvez placer le `<shadow>` sous-élément à l’intérieur du `<shape>` , `<shapetype>` ou de n’importe quel élément de forme prédéfini pour dessiner une forme avec une ombre. Vous pouvez ensuite utiliser les attributs de propriété du `<shadow>` sous-élément pour personnaliser l’ombre.

Par exemple, pour créer une forme avec une ombre, comme illustré dans l’image suivante, vous pouvez taper les lignes suivantes dans la `<BODY>` région de votre page Web :

![shape1.gif (887 octets)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   `on="t"` et `type="perspective"` indiquent d’activer l’ombre à l’aide du type de perspective.
-   L' **origine** et le **décalage** indiquent où dessiner l’ombre.
-   `matrix="..."` spécifie la matrice de transformation de perspective.

Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858396) .

 

 