---
title: ID, attribut (VML)
description: ID, attribut (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463326"
---
# <a name="id-attribute-vml"></a>ID, attribut (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Fournit un identificateur unique pour un élément. En lecture/écriture. **Chaîne**.

**S’applique à**

Tous les éléments VML.

**Syntaxe de balise**

<v : *ElementName* ID = " *IDname* " >

**Syntaxe du script**

*ElementName* . ID = " *IDname* "

*expression* = *ElementName*. ID

**Remarques**

Utilisez **ID** pour faire référence à un élément spécifique. Une fois que vous avez créé une forme et donné un ID, vous pouvez utiliser le nom de l’ID lorsque vous souhaitez manipuler l’élément.

L' **ID** est obligatoire pour utiliser l’élément [Typedeforme](msdn-online-vml-shapetype-element.md) .

Lorsque VML est généré par Microsoft Office, si un nom de modèle objet est assigné à la forme, **ID** est défini sur ce nom. Si le nom du modèle objet n’est pas défini, le nom est généré à l’aide du *SPID* (ID de forme interne) plus un préfixe (S pour forme, M pour la forme principale, T pour Typedeforme).

*Attribut standard VML*.

**Exemple**

Pour modifier les attributs d’une forme, vous devez d’abord attribuer un ID à la forme. par exemple, « myRect ».


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



[Exemple d’attribut d’ID](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 