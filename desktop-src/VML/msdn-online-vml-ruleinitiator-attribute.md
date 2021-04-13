---
title: RuleInitiator VML (attribut)
description: RuleInitiator VML (attribut)
ms.assetid: 2c9b1131-b088-4b70-b132-bdb4296433ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80201ad80fbb8dc5bbff2e8ed4e0b8db2863fdad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316356"
---
# <a name="vml-ruleinitiator-attribute"></a>RuleInitiator VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si un moteur de règles sera utilisé. En lecture/écriture. **VgTriState**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :ruleinitiator = " *expression* " >

**Remarques**

La valeur par défaut est **False**. Si la valeur est **true**, un moteur de règles est utilisé.

*Attribut extensions Microsoft Office*

**Exemple**

La forme est traitée par un moteur de règles.


```HTML
   <v:rect id=myrect fillcolor="red" rulesinitiator="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 