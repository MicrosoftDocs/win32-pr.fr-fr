---
title: Comment interagir avec la sélection actuelle
description: L’utilisateur peut sélectionner du texte dans un contrôle RichEdit à l’aide de la souris ou du clavier.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6e60ef0ba4aa9a8034256c8c272950f4983d16c0195737065563b378e14202
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434639"
---
# <a name="how-to-interact-with-the-current-selection"></a>Comment interagir avec la sélection actuelle

L’utilisateur peut sélectionner du texte dans un contrôle RichEdit à l’aide de la souris ou du clavier. La *sélection actuelle* correspond à la plage de caractères sélectionnés ou à la position du point d’insertion si aucun caractère n’est sélectionné. Une application peut obtenir des informations sur la sélection actuelle, la définir, déterminer quand elle change et afficher ou masquer la mise en surbrillance de la sélection.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="interact-with-the-current-selection"></a>Interagir avec la sélection actuelle

Pour déterminer la sélection actuelle dans un contrôle RichEdit, utilisez le message [**em \_ EXGETSEL**](em-exgetsel.md) . Pour définir la sélection actuelle, utilisez le message [**em \_ EXSETSEL**](em-exsetsel.md) . La structure [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) est utilisée avec les deux messages et spécifie une plage de caractères. Pour récupérer des informations sur le contenu de la sélection actuelle, vous pouvez utiliser le message [**em \_ SELECTIONTYPE**](em-selectiontype.md) .

Une application peut détecter à quel moment la sélection actuelle change en traitant le code de notification en [ \_ selChange](en-selchange.md) . Le code de notification spécifie une structure [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) qui contient des informations sur la nouvelle sélection. Un contrôle RichEdit envoie ce code de notification uniquement si vous l’activez à l’aide du message [**em \_ SETEVENTMASK**](em-seteventmask.md) .

Par défaut, un contrôle RichEdit affiche et masque la mise en surbrillance de la sélection quand elle gagne et perd le focus. Vous pouvez afficher ou masquer la sélection à tout moment en utilisant le message [**em \_ HIDESELECTION**](em-hideselection.md) . Par exemple, une application peut fournir une boîte de dialogue de recherche pour rechercher du texte dans un contrôle RichEdit. L’application peut sélectionner du texte correspondant sans fermer la boîte de dialogue. dans ce cas, elle doit utiliser le message de **em \_ HIDESELECTION** pour mettre en surbrillance la sélection.

Comme avec les contrôles d’édition, vous pouvez spécifier le style de fenêtre [**es \_ NOHIDESEL**](edit-control-styles.md) pour empêcher un contrôle RichEdit de masquer la mise en surbrillance de la sélection lorsqu’elle perd le focus.

En guise d’alternative à l’utilisation des messages [**em \_ EXGETSEL**](em-exgetsel.md) et [**em \_ EXSETSEL**](em-exsetsel.md) , vous pouvez récupérer et définir la sélection actuelle à l’aide des messages de contrôle d’édition em [**\_ GETSEL**](em-getsel.md) et [**em \_ SETSEL**](em-setsel.md) . Le **\_ GETSEL** message packs de caractères 2 16 bits indexe dans sa valeur de retour de 32 bits et, par conséquent, fonctionne uniquement pour les sélections qui se trouvent entièrement dans le premier 64 Ko. Toutefois, un contrôle RichEdit ne contiendra jamais plus de 32 Ko de texte, sauf si vous étendez cette limite à l’aide du message [**em \_ LIMITTEXT**](em-limittext.md) ou [**em \_ EXLIMITTEXT**](em-exlimittext.md) . Pour les sélections qui s’étendent au-delà du premier 64 Ko de texte, le message **em \_ GETSEL** retourne-1. Dans ce cas, vous pouvez toujours utiliser les valeurs retournées dans *wParam* et *lParam* pour rechercher les caractères de début et de fin de la sélection.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




