---
title: Élément TextBox VML
description: Élément TextBox VML
ms.assetid: 3573256e-f241-4de7-8541-252c92109af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a46ce8b6636b79099b7f7423fd8f746602a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727565"
---
# <a name="vml-textbox-element"></a>Élément TextBox VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit une zone de texte pour une forme.

Les attributs suivants modifient une zone de texte.



| Attribut                                                                    | Description                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Sens](msdn-online-vml-direction-attribute.md)                         | Définit la direction du texte.                         |
| [Identifiant](id-attribute--textbox--vml.md)                                         | Définit un identificateur unique pour la zone de texte.               |
| [Incrustation](msdn-online-vml-inset-attribute.md)                                 | Spécifie les valeurs de marge intérieure pour le texte de zone de texte.            |
| [InsetMode](msdn-online-vml-insetmode-attribute.md)                         | Définit la manière dont une application autorise des valeurs d’incrustation personnalisées. |
| [Disposition-Flow](msdn-online-vml-layout-flow-attribute.md)                     | Détermine le déroulement du texte dans la zone de texte.            |
| [MSO-direction-Alt](msdn-online-vml-mso-direction-alt-attribute.md)         | Définit d’autres directions pour le texte dans les zones de texte.        |
| [MSO-adapter-Shape-to-Text](msdn-online-vml-mso-fit-shape-to-text-attribute.md) | Détermine si une forme sera étirée pour s’ajuster au texte.       |
| [MSO-ajuster le texte à la forme](msdn-online-vml-mso-fit-text-to-shape-attribute.md) | Détermine si le texte est étiré pour s’ajuster à une forme.       |
| [MSO-disposition-Flow-Alt](msdn-online-vml-mso-layout-flow-alt-attribute.md)     | Définit l’autre Flow de disposition pour le texte d’une zone de texte.   |
| [MSO-Next-TextBox](msdn-online-vml-mso-next-textbox-attribute.md)           | Spécifie la zone de texte suivante dans une série.                    |
| [MSO-Rotate](msdn-online-vml-mso-rotate-attribute.md)                       | Détermine si le texte pivote avec une forme pivotée.      |
| [MSO-échelle texte](msdn-online-vml-mso-text-scale-attribute.md)               | Définit le facteur d’échelle pour l’ajustement du texte à des formes.     |
| [SingleClick](msdn-online-vml-singleclick-attribute.md)                     | Détermine si le texte peut être sélectionné à l’aide d’un simple clic. |
| [V-text-anchor](msdn-online-vml-v-text-anchor-attribute.md)                 | Définit l’ancrage vertical du texte dans une zone de texte.       |



 

**Remarques**

Cet élément doit être défini dans un élément [Shape](shape-element--vml.md) .

Voici le code minimal nécessaire pour générer une zone de texte.


```HTML
   <v:oval strokecolor="red" fillcolor="yellow
   style="position:relative;top:50;left:50;width:75;height:50">
   <v:textbox>VML</v:textbox>
   </v:oval>
```



Notez que le texte affiché dans la zone de texte est placé entre les balises de zone de texte. Le texte à l’intérieur des balises peut être modifié par des balises HTML ordinaires.

**Exemple**

-   [Exemple de zone de texte simple](/previous-versions/bb264075(v=vs.85))

 

 