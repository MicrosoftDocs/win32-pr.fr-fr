---
title: Fichier de définition d’apparence
description: Fichier de définition d’apparence
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- apparences de Lecteur Windows Media, fichiers de définition d’apparence
- apparences, fichiers de définition d’apparence
- fichiers pour les apparences, définition d’apparence
- fichiers de définition d’apparence, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bf162870596968872c4f146772c9e62277f5b2ccb660270794248786a71355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995239"
---
# <a name="skin-definition-file"></a>Fichier de définition d’apparence

Les fichiers de définition d’apparence contiennent les instructions de base pour ce que fait l’apparence et où d’autres fichiers utilisés par l’apparence peuvent être trouvés. Il ne peut y avoir qu’un seul fichier de définition d’apparence pour une apparence, et il a une extension de nom de fichier. WMS.

Les instructions contenues dans le fichier de définition d’apparence sont écrites en Extensible Markup Language (XML), qui est semblable à HTML. Si vous avez utilisé du code HTML pour créer des pages Web, vous constaterez que le XML vous semble familier.

Le XML dans le fichier de définition d’apparence utilise un ensemble de balises d’élément spéciales pour définir des parties de l’interface utilisateur de l’apparence. Par exemple, l’élément [Button](button-element.md) définit le comportement d’un bouton, son emplacement et son aspect.

Chaque balise d’élément a des attributs spécifiques. Par exemple, l’élément [Button](button-element.md) a un attribut **image** qui définit l’emplacement où se trouve l’image du bouton. Cela est similaire au code HTML, où l’élément BODY aura un attribut **bgcolor** qui définit la couleur d’arrière-plan de la page html. Des informations détaillées sur tous les éléments d’apparence et leurs attributs sont incluses dans la section [référence de programmation](skin-programming-reference.md) de l’apparence.

XML comporte quelques règles simples que vous devez connaître pour créer des apparences. Contrairement au HTML, XML vous oblige à suivre les règles exactement.

## <a name="enclose-elements-with-angle-brackets"></a>Placer les éléments entre crochets pointus

Tous les éléments sont encadrés par des crochets pointus ; par exemple, l’élément **Button** est typé comme suit :


```C++
<BUTTON>

```



Vous n’avez pas besoin de taper le mot « BUTTON » en majuscules, mais la Convention de saisie des noms d’élément en majuscules est utilisée dans l’exemple de code de ce kit de développement logiciel (SDK).

## <a name="put-attributes-before-the-closing-bracket"></a>Placer les attributs avant le crochet fermant

Tous les attributs d’un élément particulier doivent être inclus avant le Chevron fermant. Un attribut se compose du nom d’attribut suivi d’un signe égal (=) et de la valeur de l’attribut entre guillemets.


```C++
<BUTTON image="mypic.jpg">

```



Vous n’avez pas besoin de taper le mot « image » en minuscules, mais la Convention de saisie des noms d’attribut en minuscules est utilisée dans l’exemple de code de ce kit de développement logiciel (SDK). Notez également que la valeur de l’attribut est placée entre guillemets.

## <a name="opening-and-closing-elements"></a>Éléments d’ouverture et de fermeture

Certains éléments sont regroupés dans un autre élément. Par exemple, l’élément **BUTTONGROUP** n’a pas beaucoup de sens, sauf si vous utilisez un ou plusieurs éléments **BUTTONELEMENT** avec celui-ci. Pour que le regroupement soit clair, vous devez disposer d’une balise d’ouverture et de fermeture pour chaque élément. La balise d’ouverture est simplement le nom de l’élément et tous les attributs associés, entourés par des crochets pointus. La balise de fermeture est le nom de l’élément, précédé d’une barre oblique (/), puis placé entre crochets pointus. Par exemple, la balise d’ouverture de l’élément **BUTTONGROUP** se présente comme suit :


```C++
<BUTTONGROUP>

```



La balise de fermeture **BUTTONGROUP** ressemble à ceci :


```C++
</BUTTONGROUP>

```



Vous devez placer les balises **BUTTONELEMENT** entre les balises d’élément **BUTTONGROUP** d’ouverture et de fermeture. Par exemple :


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a>Fermeture des éléments

Si un élément n’a pas d’autres éléments à l’intérieur de celui-ci, vous devez placer une barre oblique à la fin du nom de l’élément juste avant le crochet pointu fermant. Par exemple, dans le code ci-dessus, chaque élément **BUTTONELEMENT** a une barre oblique pour indiquer qu’il n’y a pas d’autres éléments imbriqués dans celui-ci.

En d’autres termes, vous devez avoir une balise d’élément de fermeture ou fermer votre élément avec une barre oblique.

Cette erreur est correcte :


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Ce n’est pas correct :


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



Cela n’est pas non plus correct :


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



La section suivante fournit plus d’informations sur les fichiers de définition d’apparence :

-   [Structure du fichier de définition d’apparence](skin-definition-file-structure.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichiers d’apparence**](skin-files.md)
</dt> </dl>

 

 




