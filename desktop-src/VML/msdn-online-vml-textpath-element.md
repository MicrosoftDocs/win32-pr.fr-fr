---
title: VML TextPath, élément
description: VML TextPath, élément
ms.assetid: dcc3b723-4c5c-4069-93c7-c41737292109
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08707ae79bf297e6094228b26ae118c57a03c736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511076"
---
# <a name="vml-textpath-element"></a>VML TextPath, élément

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit un tracé de texte pour une forme.

Les attributs suivants modifient un chemin d’accès de texte.



| Attribut                                                                    | Description                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [FitPath](msdn-online-vml-fitpath-attribute.md)                             | Définit si le texte correspond au tracé d’une forme.                             |
| [FitShape](msdn-online-vml-fitshape-attribute.md)                           | Définit si le texte est adapté aux limites de la forme.                            |
| [Famille de polices](msdn-online-vml-font-family-attribute.md)                     | Spécifie la famille de texte de la police.                                             |
| [Font-size](msdn-online-vml-font-size-attribute.md)                         | Spécifie la taille de police du texte.                                               |
| [Font-style](msdn-online-vml-font-style-attribute.md)                       | Spécifie le style de police du texte.                                              |
| [Font-variant](msdn-online-vml-font-variant-attribute.md)                   | Spécifie la variante de police du texte.                                            |
| [Police-Weight](msdn-online-vml-font-weight-attribute.md)                     | Spécifie l’épaisseur de police du texte.                                             |
| [Police](msdn-online-vml-font-attribute.md)                                   | Spécifie la valeur de police composée de texte.                                     |
| [MSO-texte-Shadow](msdn-online-vml-mso-text-shadow-attribute.md)             | Définit si une ombre est appliquée au texte.                               |
| [Activé](on-attribute--textpath--vml.md)                                        | Définit si le texte est affiché.                                         |
| [Chaîne](msdn-online-vml-string-attribute.md)                               | Définit la chaîne de texte.                                                       |
| [Texte-décoration](msdn-online-vml-text-decoration-attribute.md)             | Définit l’ornement de texte du texte.                                       |
| [Trim](msdn-online-vml-trim-attribute.md)                                   | Définit si l’espace supplémentaire est supprimé au-dessus et au-dessous du texte.               |
| [V-rotation-lettres](msdn-online-vml-v-rotate-letters-attribute.md)           | Détermine si les lettres du texte sont pivotées.                        |
| [V-caractères de même hauteur](msdn-online-vml-v-same-letter-heights-attribute.md) | Détermine si toutes les lettres auront la même hauteur.                      |
| [V-Text-aligner](msdn-online-vml-v-text-align-attribute.md)                   | Définit l’alignement du texte.                                             |
| [En V-Text-KERN](msdn-online-vml-v-text-kern-attribute.md)                     | Détermine si le crénage est activé.                                       |
| [V-texte inversé](msdn-online-vml-v-text-reverse-attribute.md)               | Détermine si l’ordre de la disposition des lignes est inversé.                       |
| [V-texte-espacement-mode](msdn-online-vml-v-text-spacing-mode-attribute.md)     | Définit le mode pour letterSpacing.                                            |
| [V-texte-espacement](msdn-online-vml-v-text-spacing-attribute.md)               | Définit la quantité d’espacement du texte.                                        |
| [Cadencé](msdn-online-vml-xscale-attribute.md)                               | Détermine si un TextPath droit est utilisé à la place du tracé de la forme. |



 

**Remarques**

Cet élément doit être défini dans un élément [Shape](shape-element--vml.md) .

En plus des attributs de remplissage, de chaîne et de style normaux, l’attribut [TextPathOK](msdn-online-vml-textpathok-attribute.md) de [path](msdn-online-vml-path-element.md) doit avoir la valeur **true** et l’attribut [on](on-attribute--textpath--vml.md) de TextPath doit avoir la valeur **true** pour afficher le texte sur un tracé de texte.

Voici le code minimal nécessaire pour afficher du texte sur un tracé.


```HTML
   <v:line from="50 200" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



**Exemples**

-   [Exemple de TextPath simple](/previous-versions/bb264038(v=vs.85))
-   [Exemple de police TextPath dynamique](/previous-versions/bb264042(v=vs.85))
-   [Exemple de courbe TextPath dynamique](/previous-versions/bb264041(v=vs.85))

 

 