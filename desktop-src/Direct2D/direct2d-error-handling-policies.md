---
title: Stratégies de gestion des erreurs Direct2D
description: Cette rubrique décrit les stratégies de gestion des erreurs Direct2D. Elle contient les sections suivantes.
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, gestion des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113333"
---
# <a name="direct2d-error-handling-policies"></a>Stratégies de gestion des erreurs Direct2D

Cette rubrique décrit les stratégies de gestion des erreurs Direct2D. Elle contient les sections suivantes.

-   [Utilisation de HRESULT](#use-of-hresult)
-   [Valeur de retour des fonctions traitées par lot](#return-value-of-batched-functions)
-   [Entrée non valide](#invalid-input)
    -   [Pointeur de sortie](#output-pointer)
    -   [Paramètre obligatoire](#required-parameter)
-   [RECTANGLEs d’entrée NaN et mal ordonnés](#nan-and-poorly-ordered-input-rects)
    -   [NaN comme entrée](#nan-as-input)
    -   [RECTo d’entrée mal ordonnés](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a>Utilisation de HRESULT

Si une fonction n’est pas regroupée par lot et peut avoir un échec au moment de l’exécution, elle doit retourner **HRESULT** pour indiquer un échec. Un échec au moment de l’exécution est un échec qui ne peut pas être évité au moment de la conception, par exemple en cas de mémoire insuffisante.

## <a name="return-value-of-batched-functions"></a>Valeur de retour des fonctions traitées par lot

Les fonctions par lot dans Direct2D sont les fonctions traitées comme une unité unique lorsque [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) est appelé. Il s’agit des commandes de dessin entre [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) et **EndDraw** ou des commandes sur [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink). Pour ces fonctions, des erreurs sont signalées au moment où le lot est terminé. L’erreur est retournée après **EndDraw** pour les commandes de dessin et après **fermeture** pour **GeometrySink**.

RenderTargets arrête le dessin si un état d’erreur est défini, mais une application peut appeler [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) pour réinitialiser l’état d’erreur et reprendre le dessin.

Les fonctions **obtenir** et **définir** n’ont aucune valeur de retour. Toutefois, si une fonction **définie** a une entrée non valide, la couche de débogage génère un message. Dans ce cas, aucun État d’erreur n’est défini et la fonction **Set** ne fait rien.

## <a name="invalid-input"></a>Entrée non valide

Direct2D déréférence les pointeurs de sortie et les paramètres requis, ce qui entraîne des violations d’accès lorsque les pointeurs ne sont pas valides ou **null**.

### <a name="output-pointer"></a>Pointeur de sortie

Direct2D déréférence un pointeur de sortie et l’assigne à **null** immédiatement lors de l’entrée dans la fonction. Cela provoque une violation d’accès si un appelant passe **null** comme pointeur vers la valeur de retour. Cette stratégie s’applique également aux tableaux de pointeurs. Pour les autres paramètres de sortie, tels qu’un struct, le déréférencement se produit plus tard et entraîne également une violation d’accès. Toutefois, il existe des méthodes qui ont des pointeurs de sortie facultatifs (autrement dit, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) qui n’entraînent pas de violation d’accès.

### <a name="required-parameter"></a>Paramètre obligatoire

Si **null** est passé à une fonction nécessitant une valeur valide, la fonction déréférence le pointeur incorrect qui entraîne une violation d’accès. Pour les paramètres d’entrée facultatifs, la valeur **null** est une valeur valide qui produit une valeur par défaut raisonnable.

## <a name="nan-and-poorly-ordered-input-rects"></a>RECTANGLEs d’entrée NaN et mal ordonnés

Dans Direct2D, NaN est considéré comme une entrée valide et les RECTos d’entrée mal ordonnés sont triés.

### <a name="nan-as-input"></a>NaN comme entrée

NaN est considéré comme une entrée valide, bien qu’il résulte généralement de la primitive qui contient le dessin NaN not Drawing. L’API Direct2D ne fournit pas de filtrage explicite de NaN pour valider l’entrée.

### <a name="poorly-ordered-input-rects"></a>RECTo d’entrée mal ordonnés

Les RECTos d’entrée mal classés sont triés de sorte que les angles supérieur, gauche et inférieur sont correctement spécifiés. Pour la sortie, les rectangles vides se présentent comme suit : {Infinity, Infinity, FloatMax, FloatMax}.

 

 