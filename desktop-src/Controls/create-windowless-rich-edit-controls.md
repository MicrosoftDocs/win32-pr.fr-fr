---
title: Comment fournir des contrôles RichEdit sans fenêtre avec des fonctionnalités de fenêtre
description: La fonctionnalité de fenêtre offre la possibilité de recevoir des messages et la propriété d’un contexte de périphérique dans lequel dessiner. Les contrôles RichEdit sans fenêtre reçoivent cette fonctionnalité par le biais d’une paire d’interfaces ITextServices et ITextHost.
ms.assetid: 085CBC61-50AE-4F74-8C6A-436176DE0031
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce987630c21b1e15a2237066b39dd264125a857
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103940777"
---
# <a name="how-to-provide-windowless-rich-edit-controls-with-window-functionality"></a><span data-ttu-id="bdac5-104">Comment fournir des contrôles RichEdit sans fenêtre avec des fonctionnalités de fenêtre</span><span class="sxs-lookup"><span data-stu-id="bdac5-104">How to Provide Windowless Rich Edit Controls with Window Functionality</span></span>

<span data-ttu-id="bdac5-105">La fonctionnalité de fenêtre offre la possibilité de recevoir des messages et la propriété d’un contexte de périphérique dans lequel dessiner.</span><span class="sxs-lookup"><span data-stu-id="bdac5-105">Window functionality includes the ability to receive messages and the ownership of a device context into which to draw.</span></span> <span data-ttu-id="bdac5-106">Les contrôles RichEdit sans fenêtre reçoivent cette fonctionnalité par le biais d’une paire d’interfaces : [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) et [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span><span class="sxs-lookup"><span data-stu-id="bdac5-106">Windowless rich edit controls receive this functionality by way of a pair of interfaces: [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bdac5-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="bdac5-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bdac5-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="bdac5-108">Technologies</span></span>

-   [<span data-ttu-id="bdac5-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="bdac5-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="bdac5-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="bdac5-110">Prerequisites</span></span>

-   <span data-ttu-id="bdac5-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="bdac5-111">C/C++</span></span>
-   <span data-ttu-id="bdac5-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="bdac5-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="bdac5-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="bdac5-113">Instructions</span></span>

### <a name="establish-the-window-functionality"></a><span data-ttu-id="bdac5-114">Établir les fonctionnalités de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="bdac5-114">Establish the Window Functionality</span></span>

<span data-ttu-id="bdac5-115">L’exemple de code suivant montre comment créer l’hôte de texte et les services de texte.</span><span class="sxs-lookup"><span data-stu-id="bdac5-115">The following example code demonstrates how to create the text host and text services.</span></span>


```
    HRESULT hr;
    
    IUnknown* pUnk               = NULL;
    ITextServices* pTextServices = NULL;
    
    // Create an instance of the application-defined object that implements the ITextHost interface.
    TextHost* pTextHost = new TextHost();
    
    if (pTextHost == NULL) 
        goto errorHandler;

    // Create an instance of the text services object.
    hr = CreateTextServices(NULL, pTextHost, &pUnk);
    
    if (FAILED(hr))
        goto errorHandler;
        
    // Retrieve the IID_ITextServices interface identifier from Msftedit.dll. 
    IID* pIID_ITS = (IID*) (VOID*) GetProcAddress(hmodRichEdit, "IID_ITextServices");
               
    // Retrieve the ITextServices interface.    
    hr = pUnk->QueryInterface(*pIID_ITS, (void **)&pTextServices);
    
    if (FAILED(hr))
        goto errorHandler;
```



## <a name="remarks"></a><span data-ttu-id="bdac5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="bdac5-116">Remarks</span></span>

<span data-ttu-id="bdac5-117">Le paramètre *hmodRichEdit* dans l’exemple de code est un handle vers le module Msftedit.dll, et il est supposé que ce descripteur a déjà été récupéré par un appel à la fonction **GetModuleHandle** .</span><span class="sxs-lookup"><span data-stu-id="bdac5-117">The *hmodRichEdit* parameter in the code example is a handle to the Msftedit.dll module, and it is assumed that this handle has already been retrieved by a call to the **GetModuleHandle** function.</span></span>

## <a name="complete-example"></a><span data-ttu-id="bdac5-118">Exemple complet</span><span class="sxs-lookup"><span data-stu-id="bdac5-118">Complete example</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdac5-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bdac5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdac5-120">Utilisation de contrôles RichEdit sans fenêtre</span><span class="sxs-lookup"><span data-stu-id="bdac5-120">Using Windowless Rich Edit Controls</span></span>](using-windowless-rich-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="bdac5-121">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="bdac5-121">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="bdac5-122">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="bdac5-122">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




