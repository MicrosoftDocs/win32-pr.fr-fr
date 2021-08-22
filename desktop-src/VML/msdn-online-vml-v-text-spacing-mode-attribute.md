---
title: Attribut VML V-Text-Spacing-mode
description: Attribut VML V-Text-Spacing-mode
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42137e8c8ec401548c4e0b027a50f34813fc7b45b04c4568011617906ac8e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057657"
---
# <a name="vml-v-text-spacing-mode-attribute"></a>Attribut VML V-Text-Spacing-mode

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le mode pour letterSpacing. En lecture/écriture. **Chaîne**.

**S’applique à**

[TextPath](msdn-online-vml-textpath-element.md)

**Syntaxe de balise**

<v : *Element* style = "v-Text-Spacing-mode : *expression* " >

**Syntaxe du script**

*Element* . style. v-Text-Spacing-mode = "*expression*"

*expression* = *Element*. style. v-Text-Spacing-mode

**Remarques**

Les valeurs incluent

-   **resserrer** (par défaut)
-   **suivre**

Cet attribut détermine si l’espace sera supprimé entre chaque lettre (resserrer) ou ajoutée entre chaque lettre (suivi). La quantité de modification de l’letterSpacing est définie par l’attribut [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) .

*Attribut standard VML*

**Exemple**

L’letterSpacing entre chaque lettre est augmentée de 200 unités.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 