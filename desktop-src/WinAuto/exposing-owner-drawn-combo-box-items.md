---
title: Exposer des éléments de zone de liste déroulante Owner-Drawn
description: Les développeurs d’applications n’ont pas besoin d’implémenter IAccessible pour exposer les éléments d’une zone de liste déroulante owner-drawn avec le style CBS \_ HASSTRINGS car Microsoft Active Accessibility expose les éléments des zones de liste déroulante avec ce style.
ms.assetid: 9ff14b2f-ae09-4839-b281-fba46addaf5f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364dccaf21927e2d0092fc744d501f47830c6eeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095562"
---
# <a name="exposing-owner-drawn-combo-box-items"></a>Exposer des éléments de zone de liste déroulante Owner-Drawn

Les développeurs d’applications n’ont pas besoin d’implémenter [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour exposer les éléments d’une zone de liste déroulante owner-drawn avec le style **CBS \_ HASSTRINGS** car Microsoft Active Accessibility expose les éléments des zones de liste déroulante avec ce style. Les éléments d’une zone de liste déroulante owner-drawn avec le style **CBS \_ HASSTRINGS** sont affichés sous forme de texte. Toutefois, ce style est également utilisé avec les zones de liste déroulante owner-drawn qui n’affichent pas de texte afin que les éléments de zone de liste déroulante soient exposés par Microsoft Active Accessibility.

Pour permettre à Microsoft Active Accessibility d’exposer les éléments d’une zone de liste déroulante owner-drawn qui n’affiche pas de texte :

-   Utilisez le style **CBS \_ HASSTRINGS** lors de la création de la zone de liste déroulante.
-   Créez un équivalent textuel qui nomme ou décrit chaque élément de la zone de liste déroulante.
-   Lorsque vous ajoutez des éléments à la zone de liste déroulante owner-drawn, utilisez le \_ message CB ADDSTRING pour ajouter le texte que vous souhaitez que Microsoft Active Accessibility exposer. Ce texte n’est pas affiché, donc il ne doit pas faire partie des données owner-drawn. Ajoutez les données de l’élément owner-drawn à l’aide du \_ message CB SETITEMDATA.

Lorsque vous utilisez la méthode ci-dessus, notez les points suivants :

-   Si vous utilisez le style de **\_ Tri CBS** , la zone de liste déroulante est triée à l’aide des chaînes fournies et non de la procédure de rappel [WM \_ COMPAREITEM](../controls/wm-compareitem.md) .
-   Avec les zones de liste déroulante de variables owner-drawn créées avec le style **CBS \_ OWNERDRAWVARIABLE**, utilisez une variable globale ou un autre mécanisme pour effectuer le suivi lorsque le membre **ItemData** du [measureitemstruct,](/windows/win32/api/winuser/ns-winuser-measureitemstruct) est valide. La variable globale est requise car le système envoie le message [WM \_ MEASUREITEM](../controls/wm-measureitem.md) dès que la chaîne est ajoutée, mais avant que les données d’élément soient attachées, et à ce stade, le membre **ItemData** n’est pas valide.
-   Pour modifier la chaîne d’un élément dans une zone de liste déroulante avec le style **CBS \_ HASSTRINGS** , supprimez l’élément avec le message [CB \_ DELETESTRING](../controls/cb-deletestring.md) et ajoutez la nouvelle chaîne avec le message [CB \_ ADDSTRING](../controls/cb-addstring.md) .

 

 