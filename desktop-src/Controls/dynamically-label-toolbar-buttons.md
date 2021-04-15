---
title: Comment étiqueter dynamiquement des boutons de barre d’outils
description: Vous pouvez assigner du texte à un bouton existant à l’aide du \_ message to SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dbf6cbefffa799f60909859c99d3e8c2d65e8e
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104462799"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Comment étiqueter dynamiquement des boutons de barre d’outils

Vous pouvez assigner du texte à un bouton existant à l’aide du message [**to \_ SETBUTTONINFO**](tb-setbuttoninfo.md) .

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="dynamically-label-a-toolbar-button"></a>Étiqueter dynamiquement un bouton de barre d’outils

L’exemple suivant montre comment modifier le texte du troisième bouton dans les exemples précédents de **Save** to **Save As**.


```C++
LRESULT RelabelButton(HWND hWndToolbar)
{
    TBBUTTONINFO tbInfo;
    
    tbInfo.cbSize  = sizeof(TBBUTTONINFO);
    tbInfo.dwMask  = TBIF_TEXT;
    tbInfo.pszText = L"Save As";
    
    return SendMessage(hWndToolbar, TB_SETBUTTONINFO, (WPARAM)IDM_SAVE, (LPARAM)&tbInfo);
}
```



## <a name="remarks"></a>Notes

La modification du texte d’un bouton à l’aide de [**to \_ SETBUTTONINFO**](tb-setbuttoninfo.md) n’affecte pas la chaîne qui est assignée à ce bouton dans la liste des chaînes internes.

Si vous ajoutez une chaîne de bouton de barre d’outils à la liste de texte interne, vous ne pouvez pas récupérer l’index de cette chaîne en appelant [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md)— vous devez utiliser le message [**to \_ GETBUTTON**](tb-getbutton.md) à la place.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolBar](using-toolbar-controls.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




