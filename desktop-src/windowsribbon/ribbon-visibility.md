---
title: Affichage du ruban
description: L’infrastructure de ruban Windows expose un ensemble de propriétés qui permettent à une application de spécifier le mode d’affichage de l’interface utilisateur du ruban au moment de l’exécution.
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Ruban Windows, personnalisation des couleurs
- Ruban, personnalisation des couleurs
- personnalisation des couleurs du ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090c77c5b47afd673bc7132a87e3de336683d876
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031532"
---
# <a name="displaying-the-ribbon"></a><span data-ttu-id="f908f-106">Affichage du ruban</span><span class="sxs-lookup"><span data-stu-id="f908f-106">Displaying the Ribbon</span></span>

<span data-ttu-id="f908f-107">L’infrastructure de ruban Windows expose un ensemble de propriétés qui permettent à une application de spécifier le mode d’affichage de l’interface utilisateur du ruban au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f908f-107">The Windows Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon UI is displayed at run time.</span></span>

-   [<span data-ttu-id="f908f-108">Introduction</span><span class="sxs-lookup"><span data-stu-id="f908f-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="f908f-109">Réduire le ruban</span><span class="sxs-lookup"><span data-stu-id="f908f-109">Minimize the Ribbon</span></span>](#minimize-the-ribbon)
-   [<span data-ttu-id="f908f-110">Masquer le ruban</span><span class="sxs-lookup"><span data-stu-id="f908f-110">Hide the Ribbon</span></span>](#hide-the-ribbon)
-   [<span data-ttu-id="f908f-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="f908f-111">Example</span></span>](#example)
-   [<span data-ttu-id="f908f-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f908f-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="f908f-113">Introduction</span><span class="sxs-lookup"><span data-stu-id="f908f-113">Introduction</span></span>

<span data-ttu-id="f908f-114">Pour maximiser la zone disponible pour l’espace de document (ou le port d’affichage) d’une application de Framework de ruban, une application peut spécifier si l’interface utilisateur du ruban est visible ou masquée et, lorsqu’elle est visible, si le ruban est dans un état développé ou réduit.</span><span class="sxs-lookup"><span data-stu-id="f908f-114">To maximize the area available for the document space (or view port) of a Ribbon framework application, an application can specify whether the ribbon UI is visible or hidden and, when visible, whether the ribbon is in an expanded or collapsed state.</span></span>

<span data-ttu-id="f908f-115">Les [clés de propriété de Framework](windowsribbon-reference-properties-framework.md) répertoriées dans le tableau suivant sont utilisées pour définir de manière explicite les caractéristiques d’affichage de l’interface utilisateur du ruban dans une application de l’infrastructure du ruban.</span><span class="sxs-lookup"><span data-stu-id="f908f-115">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to explicitly set the display characteristics of the ribbon UI in a Ribbon framework application.</span></span> <span data-ttu-id="f908f-116">Ces propriétés n’ont aucun effet sur l’affichage du contrôle contextuel [contexte](windowsribbon-controls-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="f908f-116">These properties have no effect on the display of the [Context Popup](windowsribbon-controls-contextpopup.md) control.</span></span>



| <span data-ttu-id="f908f-117">État d’affichage</span><span class="sxs-lookup"><span data-stu-id="f908f-117">Display State</span></span>         | <span data-ttu-id="f908f-118">Clé de propriété du ruban</span><span class="sxs-lookup"><span data-stu-id="f908f-118">Ribbon Property Key</span></span>                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f908f-119">Développé ou réduit</span><span class="sxs-lookup"><span data-stu-id="f908f-119">Expanded or collapsed</span></span> | [<span data-ttu-id="f908f-120">IU-au-dessus \_ \_ minimisé</span><span class="sxs-lookup"><span data-stu-id="f908f-120">UI\_PKEY\_Minimized</span></span>](windowsribbon-reference-properties-uipkey-minimized.md) |
| <span data-ttu-id="f908f-121">Visible ou masqué</span><span class="sxs-lookup"><span data-stu-id="f908f-121">Visible or hidden</span></span>     | [<span data-ttu-id="f908f-122">IU de l’interface utilisateur \_ \_ visible</span><span class="sxs-lookup"><span data-stu-id="f908f-122">UI\_PKEY\_Viewable</span></span>](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a><span data-ttu-id="f908f-123">Réduire le ruban</span><span class="sxs-lookup"><span data-stu-id="f908f-123">Minimize the Ribbon</span></span>

<span data-ttu-id="f908f-124">Une application de Framework de ruban peut définir dynamiquement l’État réduit de la barre de commandes du ruban en affectant à la clé de propriété [ \_ \_ minimisé de l’interface utilisateur](windowsribbon-reference-properties-uipkey-minimized.md) la valeur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="f908f-124">A Ribbon framework application can dynamically set the minimized state of the ribbon command bar by setting the value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="f908f-125">État d’affichage</span><span class="sxs-lookup"><span data-stu-id="f908f-125">Display State</span></span> | <span data-ttu-id="f908f-126">Valeur de la clé de propriété</span><span class="sxs-lookup"><span data-stu-id="f908f-126">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="f908f-127">Développé</span><span class="sxs-lookup"><span data-stu-id="f908f-127">Expanded</span></span>      | <span data-ttu-id="f908f-128">**false**</span><span class="sxs-lookup"><span data-stu-id="f908f-128">**false**</span></span>          |
| <span data-ttu-id="f908f-129">Collapsed</span><span class="sxs-lookup"><span data-stu-id="f908f-129">Collapsed</span></span>     | <span data-ttu-id="f908f-130">**true**</span><span class="sxs-lookup"><span data-stu-id="f908f-130">**true**</span></span>           |



 

<span data-ttu-id="f908f-131">Lorsque l’interface utilisateur du ruban est dans un État réduit, la ligne de l’onglet du ruban reste visible et entièrement fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="f908f-131">When the ribbon UI is in a minimized state, the ribbon Tab row remains visible and fully functional.</span></span>

<span data-ttu-id="f908f-132">La capture d’écran suivante montre le ruban dans un État réduit.</span><span class="sxs-lookup"><span data-stu-id="f908f-132">The following screen shot shows the ribbon in the minimized state.</span></span>

![capture d’écran montrant l’interface utilisateur du ruban réduite.](images/overviews/ribbon-minimized.png)

> [!Note]  
> <span data-ttu-id="f908f-134">L’infrastructure du ruban expose cette fonctionnalité à l’utilisateur final via la sélection « réduire le ruban » du menu contextuel du ruban.</span><span class="sxs-lookup"><span data-stu-id="f908f-134">The Ribbon framework exposes this functionality to the end user through the "Minimize the Ribbon" selection of the ribbon context menu.</span></span>

 

## <a name="hide-the-ribbon"></a><span data-ttu-id="f908f-135">Masquer le ruban</span><span class="sxs-lookup"><span data-stu-id="f908f-135">Hide the Ribbon</span></span>

<span data-ttu-id="f908f-136">Une application de Framework de ruban peut définir dynamiquement l’État affichable de la barre de commandes du ruban en affectant à la clé de propriété [ \_ \_ affichable de l’interface utilisateur](windowsribbon-reference-properties-uipkey-viewable.md) la valeur **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="f908f-136">A Ribbon framework application can dynamically set the viewable state of the ribbon command bar by setting the value of the [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="f908f-137">État d’affichage</span><span class="sxs-lookup"><span data-stu-id="f908f-137">Display State</span></span> | <span data-ttu-id="f908f-138">Valeur de la clé de propriété</span><span class="sxs-lookup"><span data-stu-id="f908f-138">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="f908f-139">Visible</span><span class="sxs-lookup"><span data-stu-id="f908f-139">Visible</span></span>       | <span data-ttu-id="f908f-140">**false**</span><span class="sxs-lookup"><span data-stu-id="f908f-140">**false**</span></span>          |
| <span data-ttu-id="f908f-141">Hidden</span><span class="sxs-lookup"><span data-stu-id="f908f-141">Hidden</span></span>        | <span data-ttu-id="f908f-142">**true**</span><span class="sxs-lookup"><span data-stu-id="f908f-142">**true**</span></span>           |



 

<span data-ttu-id="f908f-143">Contrairement à la propriété [ \_ \_ minimisée de l’interface utilisateur](windowsribbon-reference-properties-uipkey-minimized.md) , le paramétrage de l’interface utilisateur de l’IU sur **faux** rend l’interface ruban invisible et complètement inutilisable pour un utilisateur final. [ \_ \_](windowsribbon-reference-properties-uipkey-viewable.md)</span><span class="sxs-lookup"><span data-stu-id="f908f-143">In contrast to the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property, setting [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) to **false** renders the ribbon UI invisible and completely unusable to an end user.</span></span>

<span data-ttu-id="f908f-144">La capture d’écran suivante montre le ruban dans un état masqué.</span><span class="sxs-lookup"><span data-stu-id="f908f-144">The following screen shot shows the ribbon in the hidden state.</span></span>

![capture d’écran montrant l’interface utilisateur du ruban masquée.](images/overviews/ribbon-viewable.png)

## <a name="example"></a><span data-ttu-id="f908f-146">Exemple</span><span class="sxs-lookup"><span data-stu-id="f908f-146">Example</span></span>

<span data-ttu-id="f908f-147">L’exemple suivant montre comment définir l’état de l’interface utilisateur du ruban au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f908f-147">The following example demonstrates how to set the state of the ribbon UI at run time.</span></span>

<span data-ttu-id="f908f-148">Dans ce cas, la fonction [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) est utilisée pour développer ou réduire l’interface ruban en fonction de l’État bascule d’un [bouton bascule](windowsribbon-controls-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="f908f-148">In this case, the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) function is used to expand or collapse the ribbon UI based on the toggle state of a [Toggle Button](windowsribbon-controls-togglebutton.md).</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a Command is executed 
//           by the user. 
//           This example demonstrates a handler for a Toggle Button
//           that sets the minimized state of the ribbon UI.
//
//  NOTES: g_pFramework is a global pointer to an IUIFramework object 
//         that is assigned when the Ribbon framework is initialized.
//
//         g_pRibbon is a global pointer to the IUIRibbon object
//         that is assigned when the Ribbon framework is initialized.
//
STDMETHODIMP CCommandHandler::Execute(
    UINT nCmdID,
    UI_EXECUTIONVERB verb,
    __in_opt const PROPERTYKEY* key,
    __in_opt const PROPVARIANT* ppropvarValue,
    __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
    HRESULT hr = E_FAIL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        switch (nCmdID)
        {
            // Minimize ribbon Command handler.
            case IDR_CMD_MINIMIZE:
                if (g_pFramework)
                {
                    IPropertyStore *pPropertyStore = NULL;
                    hr = g_pRibbon->QueryInterface(__uuidof(IPropertyStore), 
                                                   (void**)&pPropertyStore);
                    if (SUCCEEDED(hr))
                    {
                        if (ppropvarValue != NULL)
                        {
                            // Is the ToggleButton state on or off?
                            BOOL fToggled;
                            hr = UIPropertyToBoolean(*key, *ppropvarValue, &fToggled);

                            if (SUCCEEDED(hr))
                            {
                                // Set the ribbon display state based on the toggle state.
                                PROPVARIANT propvar;
                                PropVariantInit(&propvar);
                                UIInitPropertyFromBoolean(UI_PKEY_Minimized, 
                                                          fToggled, 
                                                          &propvar);
                                hr = pPropertyStore->SetValue(UI_PKEY_Minimized, 
                                                              propvar);
                                pPropertyStore->Commit();
                            }
                            pPropertyStore->Release();
                        }
                    }
                }
                break;
        }
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f908f-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f908f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f908f-150">Propriétés du ruban</span><span class="sxs-lookup"><span data-stu-id="f908f-150">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 