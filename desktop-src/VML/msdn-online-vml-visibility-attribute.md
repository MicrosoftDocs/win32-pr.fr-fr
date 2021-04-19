---
title: Attribut de visibilité VML
description: Attribut de visibilité VML
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106527555"
---
# <a name="vml-visibility-attribute"></a>Attribut de visibilité VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si une forme est affichée. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* style = "Visibility : *expression* " >

**Syntaxe du script**

*Element* . style. Visibility = "*expression*"

*expression* = *Element*. style. Visibility

**Remarques**

L’attribut **Visibility** est semblable à l’attribut de **visibilité** HTML standard pour les styles.

Ces valeurs comprennent :



| Valeur    | Description                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| visible  | La forme est visible.                                                                                                                                                                   |
| hidden   | La forme n’est pas visible, mais elle fait toujours partie du déroulement des objets dans le navigateur. Les événements de souris ne sont pas traités.                                                                  |
| inherit  | Par défaut. L’état de visibilité est hérité du parent de la forme. Microsoft Office applications utilisent uniquement **inherit** et **Hidden**; toutes les autres valeurs sont mappées à **inherit**. |
| réduire | Utilisé pour les applications de modification graphique qui peuvent réduire des groupes de formes ; par exemple, les plans.                                                                                     |



 

*Attribut standard VML*

**Exemple**

Le code suivant crée une forme, mais la masque. Les autres objets du document s’entourent, ce qui laisse un espace de la même taille que la forme.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



[Exemple d’attribut Visibility](/previous-versions/bb264100(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 