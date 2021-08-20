---
title: Exposer des éléments de la zone de liste Owner-Drawn
description: Les développeurs d’applications n’ont pas besoin d’implémenter IAccessible pour exposer les éléments d’une zone de liste owner-drawn dont le style est LBS \_ HASSTRINGS car Microsoft Active Accessibility expose les éléments dans les zones de liste avec ce style.
ms.assetid: d54ce297-ce8a-46c0-a86d-4acffa1eda27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fed68477680376373da6c16f59b3fb556b6a435f15f04daae8f3f1262829dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115272"
---
# <a name="exposing-owner-drawn-list-box-items"></a>Exposer des éléments de la zone de liste Owner-Drawn

Les développeurs d’applications n’ont pas besoin d’implémenter [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour exposer les éléments d’une zone de liste owner-drawn dont le style est **lbs \_ HASSTRINGS** car Microsoft Active Accessibility expose les éléments dans les zones de liste avec ce style. Les éléments d’une zone de liste owner-drawn avec le style **\_ HASSTRINGS** s’affichent sous forme de texte. Toutefois, ce style est également utilisé avec les zones de liste owner-drawn qui n’affichent pas de texte afin que les éléments de la zone de liste soient exposés par Microsoft Active Accessibility.

Pour permettre à Microsoft Active Accessibility d’exposer les éléments d’une zone de liste owner-drawn qui n’affiche pas de texte :

-   Utilisez le style **lbs \_ HASSTRINGS** lors de la création de la zone de liste.
-   Créez un équivalent textuel qui nomme ou décrit chaque élément de la zone de liste.
-   Lorsque vous ajoutez des éléments à la zone de liste owner-drawn, utilisez le message [lb \_ ADDSTRING](../controls/lb-addstring.md) pour ajouter le texte que vous souhaitez que Microsoft Active Accessibility exposer. Ce texte n’est pas affiché, donc il ne fait pas partie des données owner-drawn. Ajoutez les données de l’élément owner-drawn à l’aide du message [lb \_ SETITEMDATA](../controls/lb-setitemdata.md) .

Lorsque vous utilisez la méthode ci-dessus, notez les points suivants :

-   Si vous utilisez le style de **\_ Tri lbs** , la zone de liste est triée à l’aide des chaînes fournies et non de la procédure de rappel [WM \_ COMPAREITEM](../controls/wm-compareitem.md) .
-   Avec les zones de liste de variables owner-drawn créées avec le style **lbs \_ OWNERDRAWVARIABLE**, utilisez une variable globale ou un autre mécanisme pour suivre le moment où le **membre ItemData** du [measureitemstruct,](/windows/win32/api/winuser/ns-winuser-measureitemstruct) est valide. La variable globale est nécessaire car le système envoie le message [WM \_ MEASUREITEM](../controls/wm-measureitem.md) dès que la chaîne est ajoutée, mais avant que les données d’élément soient attachées, et à ce stade, le membre **ItemData** n’est pas valide.
-   Pour modifier la chaîne d’un élément dans une zone de liste avec le style **\_ HASSTRINGS lbs** , supprimez l’élément avec le message [lb \_ DELETESTRING](../controls/lb-deletestring.md) et ajoutez la nouvelle chaîne avec le \_ message lb ADDSTRING.

 

 