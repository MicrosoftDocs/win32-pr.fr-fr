---
title: PreferRelative VML (attribut)
description: PreferRelative VML (attribut)
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa425321c1937c4df1bb766c554dbd73cc384b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031334"
---
# <a name="vml-preferrelative-attribute"></a>PreferRelative VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si la taille d’origine d’un objet est enregistrée après le reformatage. En lecture/écriture. **VgTriState**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :preferrelative = " *expression* " >

**Remarques**

La valeur par défaut est **False**. Si la **valeur est true**, la taille d’origine de l’objet sera stockée et tout redimensionnement sera basé sur un pourcentage de cette taille d’origine. Dans le cas contraire, chaque redimensionnement réinitialisera l’échelle à 100%.

*Attribut extensions Microsoft Office*

**Exemple**

Si la forme est redimensionnée, la taille d’origine ne sera pas stockée.


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 