---
title: Attribut de méthode VML
description: Attribut de méthode VML
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d6b5ae67f94a2fc6e27451fb1a947c8341d1f77c08a721ca7946250cee3b7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124762"
---
# <a name="vml-method-attribute"></a>Attribut de méthode VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit la méthode utilisée pour générer un remplissage dégradé. En lecture/écriture. **VgSigmaType**.

**S’applique à**

[Remplir](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *Element* Method = " *expression* " >

**Syntaxe du script**

*Element* . Method = "*expression*"

*expression* = *Element*. Method

**Remarques**

Ces valeurs comprennent :



| Valeur  | Description          |
|--------|----------------------|
| None   | Aucun remplissage Sigma.       |
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



 

 