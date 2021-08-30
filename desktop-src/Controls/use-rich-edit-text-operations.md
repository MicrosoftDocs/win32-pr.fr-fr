---
title: Utilisation des opérations de modification de texte enrichi
description: Une application peut envoyer des messages pour récupérer ou Rechercher du texte dans un contrôle RichEdit. Vous pouvez récupérer le texte sélectionné ou une plage de texte spécifiée.
ms.assetid: 95D88F9A-3DD1-48E4-B6FF-3168F2D25846
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91018dfd2c13c589530b9e3d5abe5399a8128bb5904e66c5aceacb692ae0d0ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132078"
---
# <a name="how-to-use-rich-edit-text-operations"></a>Utilisation des opérations de modification de texte enrichi

Une application peut envoyer des messages pour récupérer ou Rechercher du texte dans un contrôle RichEdit. Vous pouvez récupérer le texte sélectionné ou une plage de texte spécifiée.

Pour obtenir le texte sélectionné dans un contrôle Rich Edit, utilisez le message [**em \_ GETSELTEXT**](em-getseltext.md) . Le texte est copié dans le tableau de caractères spécifié. Vous devez vous assurer que le tableau est suffisamment grand pour contenir le texte sélectionné, plus un caractère null de fin.

Pour récupérer une plage de texte spécifiée, utilisez le message [**em \_ GETTEXTRANGE**](em-gettextrange.md) . La structure [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) utilisée avec ce message spécifie la plage de texte à récupérer et pointe vers un tableau de caractères qui reçoit le texte. Là encore, l’application doit s’assurer que le tableau est suffisamment grand pour le texte spécifié, plus un caractère null de fin.

Vous pouvez rechercher une chaîne dans un contrôle Rich Edit à l’aide des [**messages \_ em TexteCherché**](em-findtext.md) ou [**em \_ FINDTEXTEX**](em-findtextex.md) , ou de leurs équivalents Unicode, [**em \_ FINDTEXTW**](em-findtextw.md) et [**em \_ FINDTEXTEXW**](em-findtextexw.md). La structure [**TexteCherché**](/windows/win32/api/richedit/ns-richedit-findtexta) utilisée avec les versions non étendues spécifie la plage de texte à rechercher et la chaîne à rechercher. Les versions étendues utilisent une structure [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , qui spécifie les mêmes informations et reçoit également les points de début et de fin de la plage de caractères du texte trouvé. Vous pouvez également spécifier des options comme si la recherche respecte la casse.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="use-a-rich-edit-text-operation"></a>Utiliser une opération Rich Text Edit

L’exemple de fonction suivant recherche le texte spécifié dans le texte sélectionné dans un contrôle Rich Edit qui prend en charge Unicode. Si la cible est trouvée, elle devient la nouvelle sélection.


```C++
BOOL FindTextInSelection(HWND hRich, WCHAR* target)
{
    CHARRANGE selectionRange;
    
    SendMessage(hRich, EM_EXGETSEL, 0, (LPARAM)&selectionRange);
    
    FINDTEXTEX ftex;
    
    ftex.lpstrText  = target;
    ftex.chrg.cpMin = selectionRange.cpMin;
    ftex.chrg.cpMax = selectionRange.cpMax;
    
    LRESULT lr = SendMessage(hRich, EM_FINDTEXTEXW, (WPARAM)FR_DOWN, (LPARAM) &ftex);
    
    if (lr >= 0)
    {
        LRESULT lr1 = SendMessage(hRich, EM_EXSETSEL, 0, (LPARAM)&ftex.chrgText);
        
        SendMessage(hRich, EM_HIDESELECTION, (LPARAM)FALSE, 0);
        
        return TRUE;
    }
    
    return FALSE;
    
}
```



## <a name="remarks"></a>Remarques

Microsoft Rich Edit 3,0 prend également en charge la fonction de l’éditeur de méthode d’entrée (IME) HexToUnicode, qui permet à un utilisateur d’effectuer une conversion entre des valeurs hexadécimales et Unicode à l’aide de touches d’accès rapide. Pour plus d’informations, consultez [HEXTOUNICODE IME](/windows/desktop/Intl/hextounicode-ime).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Windows démonstration des contrôles communs (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 