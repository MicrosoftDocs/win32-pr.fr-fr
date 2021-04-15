---
title: Utilisation de l’élément TextBox
description: Utilisation de l’élément TextBox
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Atelier Web, élément TextBox
- conception de pages Web, élément TextBox
- Langage VML (VML), élément TextBox
- VML (langage VML), élément TextBox
- Vector Graphics, élément TextBox
- élément TextBox
- Éléments VML, TextBox
- Formes VML, élément TextBox
- Langage VML (VML), joindre du texte
- VML (langage VML), joindre du texte
- graphiques vectoriels, joindre du texte
- Formes VML, joindre du texte
- joindre du texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463647"
---
# <a name="using-the-textbox-element"></a>Utilisation de l’élément TextBox

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

## <a name="examples"></a>Exemples :

Pour attacher du texte à un rectangle, vous pouvez taper les lignes suivantes dans la `<BODY>` région de votre page Web :


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





Pour attacher un lien hypertexte à un rectangle arrondi qui est rempli d’un dégradé, vous pouvez taper les lignes suivantes dans la `<BODY>` région de votre page Web :

![textbox2.gif (1147 octets)](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858397) .

 

 