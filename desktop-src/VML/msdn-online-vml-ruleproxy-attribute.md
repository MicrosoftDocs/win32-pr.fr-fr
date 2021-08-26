---
title: RuleProxy VML (attribut)
description: RuleProxy VML (attribut)
ms.assetid: 040e80f8-65b6-491d-812d-421800801374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fe97afee190d87b5e6f8b74d942a72d3bf11914373931e32cbb9459915b7d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099129"
---
# <a name="vml-ruleproxy-attribute"></a>RuleProxy VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si un proxy pour le moteur de règles sera utilisé. En lecture/écriture. **VgTriState**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* ruleproxy = " *expression* " >

**Remarques**

La valeur par défaut est **False**. Si la **valeur est true**, un proxy est utilisé.

*Microsoft Office Attribut extensions*

**Exemple**

Un proxy est utilisé pour traiter la forme.


```HTML
   <v:rect id=myrect fillcolor="red" ruleproxy="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 