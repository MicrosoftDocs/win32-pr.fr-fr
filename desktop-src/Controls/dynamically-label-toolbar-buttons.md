---
title: Comment étiqueter dynamiquement des boutons de barre d’outils
description: Vous pouvez assigner du texte à un bouton existant à l’aide du \_ message to SETBUTTONINFO.
ms.assetid: 571C7FB9-2806-47AF-8933-0D3541AE6ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063a3b8be8a23dc8cead219c53989a8ff1a40225dc8411f9e8a1b156b6bb55bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877439"
---
# <a name="how-to-dynamically-label-toolbar-buttons"></a>Comment étiqueter dynamiquement des boutons de barre d’outils

Vous pouvez assigner du texte à un bouton existant à l’aide du message [**to \_ SETBUTTONINFO**](tb-setbuttoninfo.md) .

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

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



## <a name="remarks"></a>Remarques

La modification du texte d’un bouton à l’aide de [**to \_ SETBUTTONINFO**](tb-setbuttoninfo.md) n’affecte pas la chaîne qui est assignée à ce bouton dans la liste des chaînes internes.

Si vous ajoutez une chaîne de bouton de barre d’outils à la liste de texte interne, vous ne pouvez pas récupérer l’index de cette chaîne en appelant [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md)— vous devez utiliser le message [**to \_ GETBUTTON**](tb-getbutton.md) à la place.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolBar](using-toolbar-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




