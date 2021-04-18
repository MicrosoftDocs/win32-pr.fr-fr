---
title: Attribut de méthode VML
description: Attribut de méthode VML
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511899"
---
# <a name="vml-method-attribute"></a>Attribut de méthode VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la méthode utilisée pour générer un remplissage dégradé. En lecture/écriture. **VgSigmaType**.

**S’applique à**

[Complète](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *Element* Method = " *expression* " >

**Syntaxe du script**

*Element* . Method = "*expression*"

*expression* = *Element*. Method

**Remarques**

Ces valeurs comprennent :



| Valeur  | Description          |
|--------|----------------------|
| Aucune   | Aucun remplissage Sigma.       |
| Linéaire | Remplissage Sigma linéaire.   |
| Sigma  | Remplissage Sigma. Par défaut. |
| Quelconque    | Tout remplissage Sigma.      |



 

*Attribut standard VML*

**Exemple**

La forme aura un dégradé linéaire rouge.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 