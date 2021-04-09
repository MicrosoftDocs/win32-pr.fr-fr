---
title: Attribut maître VML
description: Attribut maître VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102316"
---
# <a name="vml-master-attribute"></a>Attribut maître VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si un élément **Typedeforme** est un élément principal. En lecture/écriture. **VgTriState**.

**S’applique à**

[Typedeforme](msdn-online-vml-shapetype-element.md)

**Syntaxe de balise**

<v : *Element* o :Master = " *expression* " >

**Remarques**

Si la **valeur est true**, la forme **Typedeforme** est restituée par le moteur de rendu. La valeur par défaut est **False**.

*Attribut extensions Microsoft Office*

**Exemple**

L’élément **Typedeforme** est une forme maîtresse.


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 