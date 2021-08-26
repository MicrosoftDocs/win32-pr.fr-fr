---
title: VML Alt (attribut)
description: VML Alt (attribut)
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08714efca9a390cbbec2f3dcf14782053d34db3506462214b9e62ebf1da206a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905339"
---
# <a name="vml-alt-attribute"></a>VML Alt (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le texte de remplacement à afficher à la place d’un graphique. En lecture/écriture. **Chaîne**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* Alt = " *expression* " >

**Syntaxe du script**

*Element* . Alt = "*expression*"

*expression* = *élément*. Alt

**Remarques**

L’attribut **ALT** est semblable à l’attribut **ALT** HTML standard. Cet attribut permet aux navigateurs qui convertissent du texte en parole de décrire les éléments graphiques d’une page.

*Attribut standard VML*

**Voir aussi**

[Forme](shape-element--vml.md)

**Exemple**

L’élément **ALT** ci-dessous affiche l’expression « rectangle rouge » dans les navigateurs qui convertissent les pages Web en expressions vocales.


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemple d’attribut alt](/previous-versions/bb229663(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 