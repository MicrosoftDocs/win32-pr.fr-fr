---
description: Vous pouvez définir et assigner des étendues d’entrée personnalisées à l’aide de la syntaxe d’expression régulière d’écriture qui est comprise par certains des reconnaissance de l’écriture manuscrite Microsoft.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Référence de syntaxe des expressions régulières
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525296"
---
# <a name="regular-expression-syntax-reference"></a>Référence de syntaxe des expressions régulières

Vous pouvez définir et assigner des étendues d’entrée personnalisées à l’aide de la syntaxe d’expression régulière d’écriture qui est comprise par certains des reconnaissance de l’écriture manuscrite Microsoft. La syntaxe est un sous-ensemble de l' [implémentation du langage des expressions régulières](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) dans le .NET Framework.

Il existe des différences dans la façon dont les expressions régulières d’écriture manuscrite sont utilisées et la façon dont les autres types d’expressions régulières sont utilisés. La syntaxe d’écriture manuscrite est utilisée pour spécifier une chaîne exacte qui sera mise en correspondance par le moteur de reconnaissance et non une sous-chaîne. Par exemple, l’expression régulière s ( \[ a-z \] +) p retourne des correspondances pour « soupe », « stop », « InStep » et « esophagus ». En revanche, une expression régulière d’écriture équivalente telle que s ( ! est \_ ONECHAR) + p correspondrait à « soupe » et à « Stop », mais pas à « InStep » et à « esophagus ».

Les expressions régulières d’écriture manuscrite ne prennent pas en charge les espaces insécables dans les expressions régulières. Autrement dit, vous ne pouvez pas utiliser l’entité « nbsp » dans une expression régulière d’écriture manuscrite.

Les sections suivantes décrivent plus en détail la syntaxe.

## <a name="valid-operators"></a>Opérateurs valides

Les opérateurs suivants sont valides pour la création d’expressions régulières afin de définir des étendues d’entrée pour les reconnaissance de l’écriture manuscrite.



| Opérateur      | Description                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | Opérateur unaire postfix signifiant zéro, une ou plusieurs occurrences de l’opérande.<br/> |
| +<br/>  | Postfix opérateur unaire signifiant une ou plusieurs occurrences de l’opérande.<br/>  |
| ?<br/>  | Opérateur unaire postfix signifiant zéro ou une occurrence de l’opérande.<br/>   |
| \|<br/> | Signification de l’opérateur d’infixe binaire « or ».<br/>                                        |
| ()<br/> | Utilisé pour regrouper des éléments.<br/>                                                       |



 

L’implémentation Microsoft d’expressions régulières pour les reconnaissance de l’écriture manuscrite permet d’obtenir des applications répétées d’opérateurs unaires suffixés. Par exemple, a \* \* = (a \* ) \* = a \* , b ?? = (b ?) ? = b ?. Elles autorisent également les répétitions non consécutives, par exemple : a \* ? \* = ((a \* ) ?) \* = (a \* ) \* = a \* . cela diffère de .NET Framework expressions régulières, qui n’autorisent que le ? opérateur à répéter.

une autre différence par rapport à .NET Framework expressions régulières est que les expressions régulières d’écriture ne prennent pas en charge une expression vide désignée avec une paire de parenthèses vide ().

> [!Note]  
> Seuls les caractères de la page de codes 1252 sont pris en charge pour les expressions régulières d’écriture manuscrite.

 

## <a name="using-input-scopes"></a>Utilisation des étendues d’entrée

Vous pouvez également utiliser l’ensemble d’étendues d’entrée habituelles qui sont définies dans le cadre de la fonction [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) dans vos expressions régulières. Par exemple, la valeur du mois (numérique) est \_ date \_ mois. La syntaxe permettant de spécifier une étendue d’entrée dans le cadre d’une expression régulière consiste à ajouter la valeur énumérée de l’étendue d’entrée à une parenthèse ouvrante et à un point d’exclamation ( !, et à placer une parenthèse fermante,) à la fin. Par exemple :

( ! Est \_ mois de la DATE \_ )

Si vous combinez l' \_ étendue d’entrée par défaut en Oring avec toute autre étendue d’entrée, l’effet est que le module de reconnaissance peut retourner une expression unique prise en charge par le modèle de langage par défaut (par exemple, un mot du dictionnaire système ou une date) avec ou sans ponctuation, ou toute valeur qui remplit le reste de l’expression régulière transmise au module de reconnaissance.

> [!Note]  
> Les membres suivants de [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) ne sont pas pris en charge dans les expressions régulières : est \_ PHRASELIST, IS \_ REGULAREXPRESSION, is \_ SRGS, is \_ XML.

 

## <a name="unsupported-operators"></a>Opérateurs non pris en charge

Les opérateurs d’expression régulière suivants ne sont pas pris en charge lors de la création d’expressions régulières d’écriture manuscrite.



| Opérateur                                     | Description                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| .<br/>                                 | Caractère point.<br/>                                        |
| \[\]<br/>                              | Crochets. Utilisez des parenthèses pour regrouper des éléments.<br/>     |
| {}<br/>                                | Accolades.<br/>                                          |
| (?\# Commentaire) et un \# \[ Commentaire\]<br/> | Comments :<br/>                                                |
| $<br/>                                 | Caractère de signe dollar.<br/>                                   |
| ^<br/>                                 | Caractère de signe insertion.<br/>                                         |
| -<br/>                                 | Caractère tiret. Doit ou ( \| ) rassembler tous les ensembles d’éléments.<br/> |



 

## <a name="escaping-characters"></a>Caractères d'échappement

Les caractères ordinaires, autres que ceux figurant dans le tableau suivant, correspondent à eux-mêmes. Autrement dit, un « a » dans une expression régulière spécifie que l’entrée doit correspondre à un « a ».

Une autre différence importante dans l’écriture d’expressions régulières d’écriture manuscrite est que vous pouvez uniquement échapper un ensemble limité de caractères dans une expression régulière. Le tableau suivant présente le jeu de caractères autorisé qui peut être placé dans une séquence d’échappement. Toute autre tentative d’échappement d’un caractère entraînera la levée d’une erreur par le module de reconnaissance.



| Caractère       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| \\?<br/>  |
| \\(<br/>  |
| \\)<br/>  |
| \\\|<br/> |
| \\\\<br/> |
| \\!<br/>  |
| \\.<br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| \\{<br/>  |
| \\}<br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 