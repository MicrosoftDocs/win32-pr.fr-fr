---
title: Création d’objets avec multithread
description: Utilisez l’interface ID3D11Device pour créer des ressources et des objets, utilisez le ID3D11DeviceContext pour le rendu.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939987"
---
# <a name="object-creation-with-multithreading"></a><span data-ttu-id="d86b3-103">Création d’objets avec multithread</span><span class="sxs-lookup"><span data-stu-id="d86b3-103">Object Creation with Multithreading</span></span>

<span data-ttu-id="d86b3-104">Utilisez l’interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) pour créer des ressources et des objets, utilisez le [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) pour le [rendu](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="d86b3-104">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

<span data-ttu-id="d86b3-105">Voici quelques exemples de création de ressources :</span><span class="sxs-lookup"><span data-stu-id="d86b3-105">Here are some examples of how to create resources:</span></span>

-   [<span data-ttu-id="d86b3-106">Comment : créer une mémoire tampon de vertex</span><span class="sxs-lookup"><span data-stu-id="d86b3-106">How to: Create a Vertex Buffer</span></span>](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [<span data-ttu-id="d86b3-107">Comment : créer un tampon d’index</span><span class="sxs-lookup"><span data-stu-id="d86b3-107">How to: Create an Index Buffer</span></span>](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [<span data-ttu-id="d86b3-108">Comment : créer une mémoire tampon constante</span><span class="sxs-lookup"><span data-stu-id="d86b3-108">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [<span data-ttu-id="d86b3-109">Comment : initialiser une texture à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="d86b3-109">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a><span data-ttu-id="d86b3-110">Considérations sur le multithreading</span><span class="sxs-lookup"><span data-stu-id="d86b3-110">Multithreading Considerations</span></span>

<span data-ttu-id="d86b3-111">La quantité de concurrence pour la création et le rendu des ressources que votre application peut atteindre dépend du niveau de prise en charge du multithreading que le pilote implémente.</span><span class="sxs-lookup"><span data-stu-id="d86b3-111">The amount of concurrency of resource creation and rendering that your application can achieve depends on the level of multithreading support that the driver implements.</span></span> <span data-ttu-id="d86b3-112">Si le pilote prend en charge les créations simultanées, l’application doit avoir des problèmes de concurrence moins importante.</span><span class="sxs-lookup"><span data-stu-id="d86b3-112">If the driver supports concurrent creates, then the application should have much less concurrency concerns.</span></span> <span data-ttu-id="d86b3-113">Toutefois, si le pilote ne prend pas en charge la création d’objets simultanés, la quantité d’accès concurrentiel est extrêmement limitée.</span><span class="sxs-lookup"><span data-stu-id="d86b3-113">However, if the driver does not support concurrent object creation, the amount of concurrency is extremely limited.</span></span> <span data-ttu-id="d86b3-114">Pour comprendre la quantité de support disponible dans un pilote, interrogez le pilote sur la valeur du membre **DriverConcurrentCreates** de la structure de thread de données de la [**\_ fonctionnalité \_ \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) .</span><span class="sxs-lookup"><span data-stu-id="d86b3-114">To understand the amount of support available in a driver, query the driver for the value of the **DriverConcurrentCreates** member of the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure.</span></span> <span data-ttu-id="d86b3-115">Pour plus d’informations sur la vérification de la prise en charge des pilotes pour le multithreading, consultez [procédure : vérifier la prise en charge des pilotes](overviews-direct3d-11-render-multi-thread-support.md).</span><span class="sxs-lookup"><span data-stu-id="d86b3-115">For more information about checking for driver support of multithreading, see [How To: Check for Driver Support](overviews-direct3d-11-render-multi-thread-support.md).</span></span>

<span data-ttu-id="d86b3-116">Les opérations simultanées n’entraînent pas nécessairement de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="d86b3-116">Concurrent operations do not necessarily lead to better performance.</span></span> <span data-ttu-id="d86b3-117">Par exemple, la création et le chargement d’une texture sont généralement limités par la bande passante de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d86b3-117">For example, creating and loading a texture is typically limited by memory bandwidth.</span></span> <span data-ttu-id="d86b3-118">La tentative de création et de chargement de plusieurs textures peut ne pas être plus rapide qu’une texture à la fois, même si cela laisse plusieurs cœurs de processeur inactifs.</span><span class="sxs-lookup"><span data-stu-id="d86b3-118">Attempting to create and load multiple textures might be no faster than doing one texture at a time, even if this leaves multiple CPU cores idle.</span></span> <span data-ttu-id="d86b3-119">Toutefois, la création de plusieurs nuanceurs à l’aide de plusieurs threads peut augmenter les performances, car cette opération est moins tributaire des ressources système, telles que la bande passante de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d86b3-119">However, creating multiple shaders using multiple threads can increase performance as this operation is less dependent on system resources such as memory bandwidth.</span></span>

<span data-ttu-id="d86b3-120">Lorsque le pilote et le matériel graphique prennent en charge le multithreading, vous pouvez généralement initialiser plus efficacement les ressources nouvellement créées en passant un pointeur vers les données initiales dans le paramètre *pInitialData* (par exemple, dans un appel à la méthode [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) ).</span><span class="sxs-lookup"><span data-stu-id="d86b3-120">When the driver and graphics hardware support multithreading, you can typically initialize newly created resources more efficiently by passing a pointer to initial data in the *pInitialData* parameter (for example, in a call to the [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) method).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d86b3-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d86b3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d86b3-122">MultiThreading</span><span class="sxs-lookup"><span data-stu-id="d86b3-122">MultiThreading</span></span>](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




