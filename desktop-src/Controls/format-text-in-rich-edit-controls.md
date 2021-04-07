---
title: Comment mettre en forme du texte dans les contrôles RichEdit
description: Une application peut envoyer des messages à un contrôle Rich Edit afin de mettre en forme des caractères et des paragraphes et de récupérer des informations de mise en forme.
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724286"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a>Comment mettre en forme du texte dans les contrôles RichEdit

Une application peut envoyer des messages à un contrôle Rich Edit afin de mettre en forme des caractères et des paragraphes et de récupérer des informations de mise en forme. Les attributs de mise en forme des paragraphes incluent l’alignement, les tabulations, les retraits, la numérotation et les tables simples. Pour les caractères, vous pouvez spécifier le nom de la police, la taille, la couleur et les effets tels que gras, italique et protégé.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="format-text-in-a-rich-edit-control"></a>Mettre en forme du texte dans un contrôle RichEdit

Vous pouvez appliquer la mise en forme des paragraphes à l’aide du message [**em \_ SETPARAFORMAT**](em-setparaformat.md) . Pour déterminer la mise en forme de paragraphe actuelle pour le texte sélectionné, utilisez le message [**em \_ GETPARAFORMAT**](em-getparaformat.md) . La structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) ou [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) est utilisée avec les deux messages pour spécifier les attributs de mise en forme des paragraphes.

Vous pouvez appliquer la mise en forme des caractères à l’aide du message [**em \_ SETCHARFORMAT**](em-setcharformat.md) . Pour déterminer la mise en forme de caractères actuelle pour le texte sélectionné, vous pouvez utiliser le message [**em \_ GETCHARFORMAT**](em-getcharformat.md) . La structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) ou [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) est utilisée avec les deux messages pour spécifier des attributs de caractères.

Vous pouvez également utiliser des messages [**em \_ SETCHARFORMAT**](em-setcharformat.md) et [**em \_ GETCHARFORMAT**](em-getcharformat.md) pour définir et récupérer la mise en forme des caractères du point d’insertion, qui est la mise en forme appliquée à tous les caractères insérés par la suite. Par exemple, si une application définit la mise en forme de caractère par défaut sur gras et que l’utilisateur tape ensuite un caractère, ce caractère est gras.

La mise en forme des caractères du point d’insertion est appliquée au texte nouvellement inséré uniquement si la sélection actuelle est vide (si la sélection actuelle est un point d’insertion). Dans le cas contraire, le nouveau texte prend la mise en forme des caractères du texte qu’il remplace. Si la sélection change, la mise en forme des caractères par défaut change pour correspondre au premier caractère de la nouvelle sélection.

L’effet de caractère protégé est unique en ce qu’il ne modifie pas l’apparence du texte. Si l’utilisateur tente de modifier du texte protégé, un contrôle RichEdit envoie à sa fenêtre parente un code de notification en [ \_ protection](en-protected.md) , ce qui permet à la fenêtre parente d’autoriser ou d’empêcher la modification. Pour recevoir ce code de notification, vous devez l’activer à l’aide du message [**em \_ SETEVENTMASK**](em-seteventmask.md) .

La couleur de premier plan est toujours un attribut de caractère. Dans Microsoft Rich Edit 1,0, la couleur d’arrière-plan n’est qu’une propriété du contrôle Rich Edit. Pour définir la couleur d’arrière-plan par défaut, utilisez le message [**em \_ SETBKGNDCOLOR**](em-setbkgndcolor.md) . Notez que Rich Edit ne prend pas en charge le message [**WM \_ CTLCOLOREDIT**](wm-ctlcoloredit.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




