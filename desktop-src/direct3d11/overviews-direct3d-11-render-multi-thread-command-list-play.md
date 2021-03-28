---
title: Comment lire une liste de commandes
description: Cette rubrique montre comment lire une liste de commandes.
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990624"
---
# <a name="how-to-play-back-a-command-list"></a><span data-ttu-id="96c40-103">Comment : lire une liste de commandes</span><span class="sxs-lookup"><span data-stu-id="96c40-103">How to: Play Back a Command List</span></span>

<span data-ttu-id="96c40-104">Une [liste](overviews-direct3d-11-render-multi-thread-command-list.md) de commandes est une liste enregistrée de commandes de rendu.</span><span class="sxs-lookup"><span data-stu-id="96c40-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="96c40-105">Utilisez une liste de commandes pour pré-enregistrer les commandes de dessin et les relire ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="96c40-105">Use a command list to pre-record drawing commands and play them back later.</span></span> <span data-ttu-id="96c40-106">Cette rubrique montre comment lire une liste de [commandes](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="96c40-106">This topic shows how to play back a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="96c40-107">Une liste de commandes peut être utilisée pour fractionner les tâches de rendu entre les threads.</span><span class="sxs-lookup"><span data-stu-id="96c40-107">A command list can be used to split rendering tasks between threads.</span></span>

<span data-ttu-id="96c40-108">Cette section décrit comment lire une liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="96c40-108">This section describes how to play back a command list.</span></span> <span data-ttu-id="96c40-109">Pour enregistrer une liste de commandes, consultez [Comment : enregistrer une liste de commandes](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span><span class="sxs-lookup"><span data-stu-id="96c40-109">For recording a command list, see [How to: Record a Command List](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span></span>

<span data-ttu-id="96c40-110">**Pour lire une liste de commandes**</span><span class="sxs-lookup"><span data-stu-id="96c40-110">**To play back a command list**</span></span>

-   <span data-ttu-id="96c40-111">Appelez [**ID3D11DeviceContext :: ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) et transmettez un objet [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) valide.</span><span class="sxs-lookup"><span data-stu-id="96c40-111">Call [**ID3D11DeviceContext::ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) and pass a valid [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) object.</span></span>
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

<span data-ttu-id="96c40-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) doit être exécuté dans le [contexte immédiat](overviews-direct3d-11-devices-intro.md) pour que les commandes enregistrées soient exécutées sur l’unité de traitement graphique (GPU).</span><span class="sxs-lookup"><span data-stu-id="96c40-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) must be executed on the [immediate context](overviews-direct3d-11-devices-intro.md) for recorded commands to be run on the graphics processing unit (GPU).</span></span> <span data-ttu-id="96c40-113">Utilisez le contexte immédiat pour alimenter les commandes vers le GPU en vue de leur exécution, utilisez un contexte différé pour enregistrer les commandes de lecture dans une autre liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="96c40-113">Use the immediate context to feed commands to the GPU for execution, use a deferred context to record commands for playback onto another command list.</span></span> <span data-ttu-id="96c40-114">Lorsque vous appelez **ExecuteCommandList** sur un autre contexte différé, vous créez une liste de commandes différée « fusionnée ».</span><span class="sxs-lookup"><span data-stu-id="96c40-114">When you call **ExecuteCommandList** onto another deferred context, you create a ‘merged’ deferred command list.</span></span> <span data-ttu-id="96c40-115">Pour exécuter les commandes sur la liste de commandes différée fusionnée, vous devez les exécuter dans le contexte immédiat.</span><span class="sxs-lookup"><span data-stu-id="96c40-115">To run the commands on the merged deferred command list, you need to execute them on the immediate context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96c40-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96c40-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96c40-117">Liste des commandes</span><span class="sxs-lookup"><span data-stu-id="96c40-117">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="96c40-118">Comment utiliser Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="96c40-118">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




