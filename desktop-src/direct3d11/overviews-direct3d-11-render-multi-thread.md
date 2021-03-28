---
title: MultiThreading
description: Direct3D 11 implémente la prise en charge de la création et du rendu d’objets à l’aide de plusieurs threads.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4de7ca3e7e00ffba0c728aef334f21efc18899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197093"
---
# <a name="multithreading"></a><span data-ttu-id="7276e-103">MultiThreading</span><span class="sxs-lookup"><span data-stu-id="7276e-103">MultiThreading</span></span>

<span data-ttu-id="7276e-104">Direct3D 11 implémente la prise en charge de la création et du rendu d’objets à l’aide de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="7276e-104">Direct3D 11 implements support for object creation and rendering using multiple threads.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7276e-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="7276e-105">In this section</span></span>



| <span data-ttu-id="7276e-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="7276e-106">Topic</span></span>                                                                                                                   | <span data-ttu-id="7276e-107">Description</span><span class="sxs-lookup"><span data-stu-id="7276e-107">Description</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7276e-108">Introduction au multithreading dans Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="7276e-108">Introduction to Multithreading in Direct3D 11</span></span>](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | <span data-ttu-id="7276e-109">Le multithreading est conçu pour améliorer les performances en effectuant un travail à l’aide d’un ou plusieurs threads en même temps.</span><span class="sxs-lookup"><span data-stu-id="7276e-109">Multithreading is designed to improve performance by performing work using one or more threads at the same time.</span></span> <br/>                                                                                                         |
| [<span data-ttu-id="7276e-110">Création d’objets avec multithread</span><span class="sxs-lookup"><span data-stu-id="7276e-110">Object Creation with Multithreading</span></span>](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | <span data-ttu-id="7276e-111">Utilisez l’interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) pour créer des ressources et des objets, utilisez le [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) pour le [rendu](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="7276e-111">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span><br/> |
| [<span data-ttu-id="7276e-112">Rendu immédiat et différé</span><span class="sxs-lookup"><span data-stu-id="7276e-112">Immediate and Deferred Rendering</span></span>](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | <span data-ttu-id="7276e-113">Direct3D 11 prend en charge deux types de rendu : immédiat et différé.</span><span class="sxs-lookup"><span data-stu-id="7276e-113">Direct3D 11 supports two types of rendering: immediate and deferred.</span></span> <span data-ttu-id="7276e-114">Les deux sont implémentés à l’aide de l’interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="7276e-114">Both are implemented by using the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span><br/>                                                      |
| [<span data-ttu-id="7276e-115">Liste des commandes</span><span class="sxs-lookup"><span data-stu-id="7276e-115">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | <span data-ttu-id="7276e-116">Une liste de commandes est une séquence de commandes GPU qui peut être enregistrée et lue.</span><span class="sxs-lookup"><span data-stu-id="7276e-116">A command list is a sequence of GPU commands that can be recorded and played back.</span></span> <span data-ttu-id="7276e-117">Une liste de commandes peut améliorer les performances en réduisant la quantité de surcharge générée par le Runtime.</span><span class="sxs-lookup"><span data-stu-id="7276e-117">A command list may improve performance by reducing the amount of overhead generated by the runtime.</span></span><br/>                                    |
| [<span data-ttu-id="7276e-118">Différences de threads entre les versions Direct3D</span><span class="sxs-lookup"><span data-stu-id="7276e-118">Threading Differences between Direct3D Versions</span></span>](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | <span data-ttu-id="7276e-119">De nombreux modèles de programmation multithread utilisent des primitives de synchronisation (telles que des mutex) pour créer des sections critiques et empêcher l’accès à du code par plusieurs threads à la fois.</span><span class="sxs-lookup"><span data-stu-id="7276e-119">Many multi-threaded programming models make use of synchronization primitives (such as mutexes) to create critical sections and prevent code from being accessed by more than one thread at a time.</span></span><br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="7276e-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7276e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7276e-121">Procédure : vérifier la prise en charge des pilotes</span><span class="sxs-lookup"><span data-stu-id="7276e-121">How To: Check for Driver Support</span></span>](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[<span data-ttu-id="7276e-122">Rendu</span><span class="sxs-lookup"><span data-stu-id="7276e-122">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





