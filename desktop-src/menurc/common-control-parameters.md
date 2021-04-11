---
title: Paramètres de contrôle communs
description: La syntaxe générale d’une instruction de définition de ressource de contrôle est décrite ci-dessous.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314915"
---
# <a name="common-control-parameters"></a>Paramètres de contrôle communs

La syntaxe générale d’une instruction de définition de ressource de contrôle est décrite ci-dessous. La signification de chaque paramètre est indiquée ci-dessous. Parfois, une instruction utilise un paramètre différemment ou peut ignorer un paramètre. La variation spécifique à l’instruction est décrite dans la documentation de l’instruction.

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*financière*
</dt> <dd>

Texte à afficher avec le contrôle. Le texte est positionné dans le contrôle ou adjacent au contrôle.

Ce paramètre doit contenir zéro, un ou plusieurs caractères placés entre guillemets doubles ("). Les chaînes se terminent automatiquement par un caractère null et sont converties en Unicode dans le fichier de ressources résultant.

Par défaut, les caractères figurant entre les guillemets doubles sont des caractères ANSI et les séquences d’échappement sont interprétées comme des séquences d’échappement d’octets. Si la chaîne est précédée du préfixe « L », la chaîne est une chaîne à caractères larges et les séquences d’échappement sont interprétées comme des séquences d’échappement à 2 octets qui spécifient des caractères Unicode. Si un guillemet double est requis dans le texte, vous devez inclure deux guillemets doubles.

Un caractère perluète (&) dans le texte indique que le caractère suivant est utilisé comme caractère mnémonique pour le contrôle. Lorsque le contrôle est affiché, l’esperluette n’est pas affichée, mais le caractère mnémonique est souligné. L’utilisateur peut choisir le contrôle en appuyant sur la touche correspondant au caractère mnémonique souligné. Pour utiliser la esperluette comme caractère dans une chaîne, insérez deux esperluette (&&).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*identifi*
</dt> <dd>

Identificateur de contrôle. Cette valeur doit être un entier non signé 16 bits compris entre 0 et 65 535 ou une expression arithmétique simple qui prend une valeur comprise dans cette plage.

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordonnée X du côté gauche du contrôle par rapport au côté gauche de la boîte de dialogue. Cette valeur doit être un entier non signé 16 bits compris entre 0 et 65 535. La coordonnée est exprimée en unités de boîte de dialogue et est relative à l’origine de la boîte de dialogue, de la fenêtre ou du contrôle contenant le contrôle spécifié.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordonnée Y du côté supérieur du contrôle par rapport au haut de la boîte de dialogue. Cette valeur doit être un entier non signé 16 bits compris entre 0 et 65 535. La coordonnée est exprimée en unités de boîte de dialogue par rapport à l’origine de la boîte de dialogue, de la fenêtre ou du contrôle contenant le contrôle spécifié.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Largeur*
</dt> <dd>

Largeur du contrôle. Cette valeur doit être un entier non signé 16 bits compris entre 1 et 65 535. La largeur est en unités de 1/4 caractères.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*celle*
</dt> <dd>

Hauteur du contrôle. Cette valeur doit être un entier non signé 16 bits compris entre 1 et 65 535. La hauteur est en unités de 1/8 caractères.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Styles de contrôle. Utilisez l’opérateur de bits or ( \| ) pour combiner les styles. Pour plus d’informations, consultez [styles de fenêtre](../winmsg/window-styles.md).

</dd> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*style étendu*
</dt> <dd>

Styles de fenêtre étendus. Vous devez spécifier *style* pour spécifier *le style étendu*. Pour plus d’informations, consultez [**ExStyle**](exstyle-statement.md).

</dd> <dt>

<span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*
</dt> <dd>

Expression numérique indiquant l’ID utilisé pour identifier le contrôle pendant le traitement de [**\_ l’aide WM**](../shell/wm-help.md) .

</dd> <dt>

<span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*
</dt> <dd>

Données spécifiques au contrôle pour le contrôle. Lorsqu’une boîte de dialogue est créée et qu’un contrôle de cette boîte de dialogue, qui contient des données spécifiques au contrôle, est créé, un pointeur vers ces données est passé dans la procédure de fenêtre du contrôle via le *lParam* du message [**WM \_ Create**](../winmsg/wm-create.md) pour ce contrôle.

</dd> </dl>

## <a name="remarks"></a>Notes

Les unités de la boîte de dialogue horizontale sont 1/4 de l’unité de largeur de base du dialogue. Les unités verticales sont 1/8 de l’unité de hauteur de la boîte de dialogue. Les unités de base de la boîte de dialogue en cours sont calculées à partir de la hauteur et de la largeur de la police système actuelle. La fonction [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) retourne les unités de base de la boîte de dialogue en pixels. Les coordonnées sont relatives à l’origine de la boîte de dialogue.

 

 