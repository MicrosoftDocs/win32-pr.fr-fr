---
title: Comment utiliser les méthodes de tabulation dans TOM
description: L’exemple suivant fournit des fonctions C qui illustrent l’utilisation des méthodes d’onglet dans le modèle d’objet de texte (TOM).
ms.assetid: C74B4E43-615D-48B9-9884-F626BAF31F74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9851b30fdf58c0d4200600c0c4c83c7f9a00a555
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "103841997"
---
# <a name="how-to-use-tab-methods-in-tom"></a><span data-ttu-id="9a845-103">Comment utiliser les méthodes de tabulation dans TOM</span><span class="sxs-lookup"><span data-stu-id="9a845-103">How to Use Tab Methods in TOM</span></span>

<span data-ttu-id="9a845-104">L’exemple suivant fournit des fonctions C qui illustrent l’utilisation des méthodes d’onglet dans le modèle d’objet de texte (TOM).</span><span class="sxs-lookup"><span data-stu-id="9a845-104">The following example provides C functions that illustrate the use of the tab methods in the Text Object Model (TOM).</span></span> <span data-ttu-id="9a845-105">Il est supposé que la plupart des applications incluent une barre d’outils qui indique la position actuelle et le type des onglets pour le paragraphe actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="9a845-105">It is assumed that most applications include a toolbar that shows the current position and type of the tabs for the currently selected paragraph.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9a845-106">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="9a845-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9a845-107">Technologies</span><span class="sxs-lookup"><span data-stu-id="9a845-107">Technologies</span></span>

-   [<span data-ttu-id="9a845-108">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="9a845-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9a845-109">Prérequis</span><span class="sxs-lookup"><span data-stu-id="9a845-109">Prerequisites</span></span>

-   <span data-ttu-id="9a845-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="9a845-110">C/C++</span></span>
-   <span data-ttu-id="9a845-111">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="9a845-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9a845-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="9a845-112">Instructions</span></span>

### <a name="use-a-tab-method"></a><span data-ttu-id="9a845-113">Utiliser une méthode Tab</span><span class="sxs-lookup"><span data-stu-id="9a845-113">Use a Tab Method</span></span>

<span data-ttu-id="9a845-114">L’exemple de code suivant montre comment mettre à jour une barre d’outils avec les détails de l’onglet actuel.</span><span class="sxs-lookup"><span data-stu-id="9a845-114">The following code example demonstrates how to update a toolbar with the current tab details.</span></span>


```C++
HRESULT UpdateToolbar(ITextSelection *pSel)
{
    HRESULT hr       = S_OK;        
    ITextPara *pPara = 0;
    
    float f;
    long tbt;            // tab type
    long tbp;

    hr = pSel->GetPara(&pPara);
    
    if (FAILED(hr))
        goto cleanup;    // Paragraph properties are not supported
    
    f = (float) -1.0;    // Start at beginning
    
    while (pPara->GetTab(tbgoNext, &f, &tbt, NULL) == S_OK)
    {
            // Do something like draw tab icon on toolbar here
            // DrawTabPicture(f, tbt);
    }
    
cleanup:

    if (pPara)
        pPara->Release();
        
    return hr;
    
}
```



### <a name="copy-tab-information"></a><span data-ttu-id="9a845-115">Copier les informations de l’onglet</span><span class="sxs-lookup"><span data-stu-id="9a845-115">Copy Tab Information</span></span>

<span data-ttu-id="9a845-116">L’exemple suivant montre comment copier uniquement les informations d’onglet d’une interface [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) vers une autre.</span><span class="sxs-lookup"><span data-stu-id="9a845-116">The following example shows how to copy only the tab information from one [**ITextPara**](/windows/desktop/api/Tom/nn-tom-itextpara) interface to another.</span></span> <span data-ttu-id="9a845-117">Il accepte deux paramètres : **ITextPara** \* *pParaFrom* (le paragraphe à partir duquel copier les tabulations) et **ITextPara** \* *pParaFrom* (le paragraphe dans lequel copier les tabulations).</span><span class="sxs-lookup"><span data-stu-id="9a845-117">It takes two parameters: **ITextPara** \* *pParaFrom* (the paragraph from which to copy tabs) and **ITextPara** \* *pParaFrom* (the paragraph to which to copy tabs).</span></span>


```C++
HRESULT CopyOnlyTabs(ITextPara *pParaFrom, ITextPara *pParaTo)
{
    float f;
    short tbt;
    short style;
     
    pParaTo->ClearAllTabs();
    
    f = (float) -1.0;
    
    while (pParaFrom->GetTab(tbgoNext, &f, &tbt, &style) == S_OK)
        pParaTo->AddTab(f, tbt, style);
        
    return S_OK;                
    
}
```



## <a name="related-topics"></a><span data-ttu-id="9a845-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a845-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a845-119">Utilisation du modèle d’objet de texte</span><span class="sxs-lookup"><span data-stu-id="9a845-119">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="9a845-120">Utilisation de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="9a845-120">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="9a845-121">[Démonstration des contrôles communs Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="9a845-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




