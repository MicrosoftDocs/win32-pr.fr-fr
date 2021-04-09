---
title: Attribut VML Path
description: Attribut VML Path
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842694"
---
# <a name="vml-path-attribute"></a>Attribut VML Path

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Spécifie la ligne qui compose les bords d’une forme. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* path = " *expression* " >

**Syntaxe du script**

*Element* . Path = "*expression*"

*expression* = *Element*. Path

**Remarques**

Si une forme contient l’élément [path](msdn-online-vml-path-element.md) , les commandes Path de l’élément Path ont priorité sur la valeur de l’attribut Shape. Pour plus d’informations sur le jeu de commandes utilisé pour les chemins d’accès, consultez la rubrique relative à l’élément **path** .

*Attribut standard VML*

**Exemple**

Un chemin d’accès carré fermé est défini dans la chaîne de l’attribut path. Un point initial est défini avec `m` (utilisé pour la commande **MoveTo** ) à 1, 1 et une ligne est dessinée avec `l` (la lettre « L » utilisée pour la commande **LineTo**) à partir de la position de départ (1,1) vers les trois autres points (dans l’ordre) : 1 200 ; 200 200 ; 200, 1. La ligne est fermée avec `x` (**Fermer**) et se termine par `e` (**fin**). Notez que les coordonnées sont fournies dans l’espace de coordonnées relatif et que la taille réelle est déterminée par la **largeur** et la **hauteur**.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemple d’attribut path](/previous-versions/bb264089(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 