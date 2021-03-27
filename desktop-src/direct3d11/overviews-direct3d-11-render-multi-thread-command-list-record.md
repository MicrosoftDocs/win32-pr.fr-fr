---
title: Enregistrement d’une liste de commandes
description: Cette rubrique montre comment créer et enregistrer une liste de commandes.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673897"
---
# <a name="how-to-record-a-command-list"></a><span data-ttu-id="3a566-103">Comment : enregistrer une liste de commandes</span><span class="sxs-lookup"><span data-stu-id="3a566-103">How to: Record a Command List</span></span>

<span data-ttu-id="3a566-104">Une [liste](overviews-direct3d-11-render-multi-thread-command-list.md) de commandes est une liste enregistrée de commandes de rendu.</span><span class="sxs-lookup"><span data-stu-id="3a566-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="3a566-105">Cette rubrique montre comment créer et enregistrer une [liste de commandes](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="3a566-105">This topic shows how to create and record a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="3a566-106">Utilisez une liste de commandes pour enregistrer les commandes de rendu et les lire ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3a566-106">Use a command list to record render commands and play them back later.</span></span> <span data-ttu-id="3a566-107">Une liste de commandes est pratique pour fractionner les tâches de rendu entre les threads.</span><span class="sxs-lookup"><span data-stu-id="3a566-107">A command list is convenient for splitting rendering tasks between threads.</span></span>

<span data-ttu-id="3a566-108">**Pour enregistrer une liste de commandes**</span><span class="sxs-lookup"><span data-stu-id="3a566-108">**To record a command list**</span></span>

1.  <span data-ttu-id="3a566-109">Une liste de commandes doit être créée à partir d’un contexte différé, qui contient l’état de l’appareil et les actions de rendu.</span><span class="sxs-lookup"><span data-stu-id="3a566-109">A command list must be created from a deferred context, which contains device state and rendering actions.</span></span> <span data-ttu-id="3a566-110">Pour un appareil donné, créez un contexte différé en appelant [**ID3D11Device :: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="3a566-110">Given a device, create a deferred context by calling [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  <span data-ttu-id="3a566-111">Utilisez le contexte différé pour effectuer le rendu.</span><span class="sxs-lookup"><span data-stu-id="3a566-111">Use the deferred context to render.</span></span>

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    <span data-ttu-id="3a566-112">Cet exemple simple efface une cible de rendu, mais vous pouvez ajouter des commandes de rendu supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3a566-112">This simple example clears a render target, but you could add additional render commands.</span></span>

3.  <span data-ttu-id="3a566-113">Créez/enregistrez une liste de commandes en appelant [**ID3D11DeviceContext :: FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) et en passant un pointeur vers une interface [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) non initialisée.</span><span class="sxs-lookup"><span data-stu-id="3a566-113">Create/record a command list by calling [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) and passing a pointer to an uninitialized [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) interface.</span></span>

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    <span data-ttu-id="3a566-114">Lorsque la méthode retourne une valeur, une liste de commandes est créée, contenant toutes les commandes de rendu et une interface est retournée à l’application.</span><span class="sxs-lookup"><span data-stu-id="3a566-114">When the method returns, a command list is created containing all the render commands and an interface is returned to the application.</span></span>

    <span data-ttu-id="3a566-115">Le paramètre booléen indique au runtime ce qu’il faut faire avec l’état du pipeline dans le contexte différé.</span><span class="sxs-lookup"><span data-stu-id="3a566-115">The boolean parameter tells the runtime what to do with the pipeline state in the deferred context.</span></span> <span data-ttu-id="3a566-116">**True** signifie restaurer l’état du contexte de périphérique dans sa condition de liste de pré-commandes lorsque l’enregistrement est terminé, **false** signifie ne pas modifier l’état après l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3a566-116">**TRUE** means restore the state of the device context to its pre-command list condition when recording is completed, **FALSE** means do not change the state after recording.</span></span> <span data-ttu-id="3a566-117">Cela signifie que le contexte de périphérique reflète les modifications d’État contenues dans la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="3a566-117">This means that the device context will reflect the state changes contained in the command list.</span></span>

<span data-ttu-id="3a566-118">Pour voir un exemple de lecture d’une liste de commandes, consultez [Comment : lire une liste de commandes](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span><span class="sxs-lookup"><span data-stu-id="3a566-118">To see an example for playing back a command list, see [How to: Play Back a Command List](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a566-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a566-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a566-120">Liste des commandes</span><span class="sxs-lookup"><span data-stu-id="3a566-120">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="3a566-121">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="3a566-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




