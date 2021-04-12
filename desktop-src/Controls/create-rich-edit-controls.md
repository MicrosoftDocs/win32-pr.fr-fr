---
title: Comment créer des contrôles RichEdit
description: Pour créer un contrôle Rich Edit, appelez la fonction CreateWindowEx, en spécifiant la classe Rich Edit Window.
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031908"
---
# <a name="how-to-create-rich-edit-controls"></a>Comment créer des contrôles RichEdit

Pour créer un contrôle Rich Edit, appelez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe Rich Edit Window. Pour Microsoft Rich Edit 4,1 (Msftedit.dll), spécifiez \_ la classe que dans msftedit comme classe de fenêtre. Pour toutes les versions précédentes, spécifiez la \_ classe RichEdit. Pour plus d’informations, consultez [versions de Rich Edit](about-rich-edit-controls.md).

Les contrôles RichEdit prennent en charge la plupart des styles de fenêtre utilisés avec les contrôles d’édition, ainsi que des styles supplémentaires. Vous devez spécifier le style de fenêtre [**\_ multiligne es**](edit-control-styles.md) si vous souhaitez autoriser plus d’une ligne de texte dans le contrôle. Pour plus d’informations, consultez [styles de contrôle RichEdit](rich-edit-control-styles.md).

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="create-a-rich-edit-control"></a>Créer un contrôle RichEdit

L’exemple de fonction suivant crée un contrôle RichEdit et l’initialise avec du texte.


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



Dans Microsoft Visual Studio 2005 et versions ultérieures, il est possible d’ajouter un contrôle Rich Edit à un modèle de boîte de dialogue en faisant glisser le contrôle à partir de la boîte à outils. Toutefois, cette opération dans l’éditeur de boîtes de dialogue ne garantit pas que la bibliothèque requise sera chargée avant la création du contrôle. Il est nécessaire d’appeler la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour charger Riched32.dll, Riched20.dll ou Msftedit.dll avant la création de la boîte de dialogue.

## <a name="remarks"></a>Notes

Pour utiliser les styles visuels avec ces contrôles, une application doit inclure un manifeste et doit appeler la fonction [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) au début du programme. Pour plus d’informations sur les styles visuels, consultez [styles visuels](themes-overview.md). Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de contrôles RichEdit](using-rich-edit-controls.md)
</dt> <dt>

[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 