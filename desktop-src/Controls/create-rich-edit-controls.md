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
# <a name="how-to-create-rich-edit-controls"></a><span data-ttu-id="0bc3f-103">Comment créer des contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="0bc3f-103">How to Create Rich Edit Controls</span></span>

<span data-ttu-id="0bc3f-104">Pour créer un contrôle Rich Edit, appelez la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , en spécifiant la classe Rich Edit Window.</span><span class="sxs-lookup"><span data-stu-id="0bc3f-104">To create a rich edit control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the rich edit window class.</span></span> <span data-ttu-id="0bc3f-105">Pour Microsoft Rich Edit 4,1 (Msftedit.dll), spécifiez \_ la classe que dans msftedit comme classe de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0bc3f-105">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT\_CLASS as the window class.</span></span> <span data-ttu-id="0bc3f-106">Pour toutes les versions précédentes, spécifiez la \_ classe RichEdit.</span><span class="sxs-lookup"><span data-stu-id="0bc3f-106">For all previous versions, specify RICHEDIT\_CLASS.</span></span> <span data-ttu-id="0bc3f-107">Pour plus d’informations, consultez [versions de Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="0bc3f-107">For more information, see [Versions of Rich Edit](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="0bc3f-108">Les contrôles RichEdit prennent en charge la plupart des styles de fenêtre utilisés avec les contrôles d’édition, ainsi que des styles supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0bc3f-108">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="0bc3f-109">Vous devez spécifier le style de fenêtre [**\_ multiligne es**](edit-control-styles.md) si vous souhaitez autoriser plus d’une ligne de texte dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="0bc3f-109">You should specify the [**ES\_MULTILINE**](edit-control-styles.md) window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="0bc3f-110">Pour plus d’informations, consultez [styles de contrôle RichEdit](rich-edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="0bc3f-110">For more information, see [Rich Edit Control Styles](rich-edit-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0bc3f-111">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="0bc3f-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0bc3f-112">Technologies</span><span class="sxs-lookup"><span data-stu-id="0bc3f-112">Technologies</span></span>

-   [<span data-ttu-id="0bc3f-113">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="0bc3f-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0bc3f-114">Prérequis</span><span class="sxs-lookup"><span data-stu-id="0bc3f-114">Prerequisites</span></span>

-   <span data-ttu-id="0bc3f-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="0bc3f-115">C/C++</span></span>
-   <span data-ttu-id="0bc3f-116">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="0bc3f-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0bc3f-117">Instructions</span><span class="sxs-lookup"><span data-stu-id="0bc3f-117">Instructions</span></span>

### <a name="create-a-rich-edit-control"></a><span data-ttu-id="0bc3f-118">Créer un contrôle RichEdit</span><span class="sxs-lookup"><span data-stu-id="0bc3f-118">Create a Rich Edit Control</span></span>

<span data-ttu-id="0bc3f-119">L’exemple de fonction suivant crée un contrôle RichEdit et l’initialise avec du texte.</span><span class="sxs-lookup"><span data-stu-id="0bc3f-119">The following example function creates a rich edit control and initializes it with some text.</span></span>


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



<span data-ttu-id="0bc3f-120">Dans Microsoft Visual Studio 2005 et versions ultérieures, il est possible d’ajouter un contrôle Rich Edit à un modèle de boîte de dialogue en faisant glisser le contrôle à partir de la boîte à outils.</span><span class="sxs-lookup"><span data-stu-id="0bc3f-120">In Microsoft Visual Studio 2005 and later, it is possible to add a rich edit control into a dialog template by dragging the control from the toolbox.</span></span> <span data-ttu-id="0bc3f-121">Toutefois, cette opération dans l’éditeur de boîtes de dialogue ne garantit pas que la bibliothèque requise sera chargée avant la création du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0bc3f-121">However, doing this in the dialog editor does not ensure that the required library will be loaded before the control is created.</span></span> <span data-ttu-id="0bc3f-122">Il est nécessaire d’appeler la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour charger Riched32.dll, Riched20.dll ou Msftedit.dll avant la création de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0bc3f-122">It is necessary to call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Riched32.dll, Riched20.dll, or Msftedit.dll before the dialog is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bc3f-123">Notes</span><span class="sxs-lookup"><span data-stu-id="0bc3f-123">Remarks</span></span>

<span data-ttu-id="0bc3f-124">Pour utiliser les styles visuels avec ces contrôles, une application doit inclure un manifeste et doit appeler la fonction [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) au début du programme.</span><span class="sxs-lookup"><span data-stu-id="0bc3f-124">To use visual styles with these controls, an application must include a manifest and must call the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function at the beginning of the program.</span></span> <span data-ttu-id="0bc3f-125">Pour plus d’informations sur les styles visuels, consultez [styles visuels](themes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0bc3f-125">For information on visual styles, see [Visual Styles](themes-overview.md).</span></span> <span data-ttu-id="0bc3f-126">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0bc3f-126">For information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bc3f-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0bc3f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bc3f-128">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="0bc3f-128">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="0bc3f-129">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="0bc3f-129">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 