---
title: Prédication
description: Un prédicat est une fonctionnalité qui permet au GPU plutôt qu’au processeur de déterminer de ne pas dessiner, copier ou distribuer un objet.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/20/2020
ms.locfileid: "104548581"
---
# <a name="predication"></a><span data-ttu-id="e585a-103">Prédication</span><span class="sxs-lookup"><span data-stu-id="e585a-103">Predication</span></span>

<span data-ttu-id="e585a-104">Un prédicat est une fonctionnalité qui permet au GPU plutôt qu’au processeur de déterminer de ne pas dessiner, copier ou distribuer un objet.</span><span class="sxs-lookup"><span data-stu-id="e585a-104">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy, or dispatch an object.</span></span>

-   [<span data-ttu-id="e585a-105">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="e585a-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="e585a-106">SetPredication</span><span class="sxs-lookup"><span data-stu-id="e585a-106">SetPredication</span></span>](#setpredication)
-   [<span data-ttu-id="e585a-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e585a-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="e585a-108">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="e585a-108">Overview</span></span>

<span data-ttu-id="e585a-109">L’utilisation classique de la prédicat est avec l’occlusion ; Si un cadre englobant est dessiné et est bloqués, il n’y a évidemment aucun point dans le dessin de l’objet lui-même.</span><span class="sxs-lookup"><span data-stu-id="e585a-109">The typical use of predication is with occlusion; if a bounding box is drawn and is occluded, there is obviously no point in drawing the object itself.</span></span> <span data-ttu-id="e585a-110">Dans ce cas, le dessin de l’objet peut être « prédicat », ce qui permet sa suppression du rendu réel par le GPU.</span><span class="sxs-lookup"><span data-stu-id="e585a-110">In this situation, the drawing of the object can be "predicated", enabling its removal from actual rendering by the GPU.</span></span>

<span data-ttu-id="e585a-111">Dans un premier temps, cela peut paraître redudant au-dessus du test de profondeur standard plus une passe de profondeur.</span><span class="sxs-lookup"><span data-stu-id="e585a-111">At first, this might seem redudant over and above the standard depth test plus an early depth pass.</span></span> <span data-ttu-id="e585a-112">Toutefois, un prédicat peut supprimer la surcharge de l’état de la commande de dessin, ainsi que la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="e585a-112">But predication can remove the overhead of the draw command state itself, plus the rasterization.</span></span> <span data-ttu-id="e585a-113">Tandis qu’un test de profondeur précoce supprime les pixels inutiles, il peut toujours exécuter des nuanceurs de vertex, de coques, de domaines et de géométrie, et appeler l’assembleur d’entrée de fonction fixe, Tesselator et rastériseur.</span><span class="sxs-lookup"><span data-stu-id="e585a-113">While an early depth pass removes unnecessary pixels, it can still execute vertex, hull, domain, and geometry shaders, and invoke the fixed-function input assembler, tesselator, and rasterizer.</span></span> <span data-ttu-id="e585a-114">En dessinant un simple cadre englobant ou un volume englobant similaire &mdash; qui est plus simple à traiter et à pixelliser que le modèle réel, &mdash; vous évitez la pixellisation et le traitement inutiles.</span><span class="sxs-lookup"><span data-stu-id="e585a-114">By drawing a simple bounding box or similar bounding volume&mdash;which is simpler to process and rasterize than the real model&mdash;you avoid unnecessary rasterization and processing.</span></span>

<span data-ttu-id="e585a-115">Contrairement à Direct3D 11, le prédicat est dissocié des requêtes et est développé dans Direct3D 12 pour permettre à une application de définir des prédicats d’objets en fonction de tout raisonnement que le développeur de l’application peut décider (pas seulement d’occlusion).</span><span class="sxs-lookup"><span data-stu-id="e585a-115">Unlike Direct3D 11, predication is decoupled from queries, and is expanded in Direct3D 12 to enable an application to predicate objects based on any reasoning the app developer may decide on (not just occlusion).</span></span>

## <a name="setpredication"></a><span data-ttu-id="e585a-116">SetPredication</span><span class="sxs-lookup"><span data-stu-id="e585a-116">SetPredication</span></span>

<span data-ttu-id="e585a-117">Un prédicat peut être défini en fonction de la valeur de 64 bits dans une mémoire tampon (reportez-vous à [**D3D12 \_ Predicate \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span><span class="sxs-lookup"><span data-stu-id="e585a-117">Predication can be set based on the value of 64-bits within a buffer (refer to [**D3D12\_PREDICATION\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span></span>

<span data-ttu-id="e585a-118">Lorsque le GPU exécute une commande [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) , il aligne la valeur dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e585a-118">When the GPU executes a [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) command it snaps the value in the buffer.</span></span> <span data-ttu-id="e585a-119">Les modifications ultérieures apportées aux données dans la mémoire tampon n’affectent pas rétroactivement l’état de prédicat.</span><span class="sxs-lookup"><span data-stu-id="e585a-119">Future changes to the data in the buffer do not retroactively affect the predication state.</span></span>

<span data-ttu-id="e585a-120">Si la mémoire tampon du paramètre d’entrée a la valeur NULL, la prédicat est désactivé.</span><span class="sxs-lookup"><span data-stu-id="e585a-120">If the input parameter Buffer is NULL, then predication is disabled.</span></span>

<span data-ttu-id="e585a-121">Les indicateurs de prédicat ne sont pas présents dans l’API Direct3D 12 ; les prédicats et sont autorisés sur les listes de commandes directes, de calcul et de copie.</span><span class="sxs-lookup"><span data-stu-id="e585a-121">Predication hints are not present in the Direct3D 12 API; and predication is allowed on direct, compute, and copy command lists.</span></span> <span data-ttu-id="e585a-122">La mémoire tampon source peut être dans n’importe quel type de segment (par défaut, charger, readback, personnalisé).</span><span class="sxs-lookup"><span data-stu-id="e585a-122">The source buffer can be in any heap type (default, upload, readback, custom).</span></span>

<span data-ttu-id="e585a-123">Le runtime principal validera les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e585a-123">The core runtime will validate the following:</span></span>

-   <span data-ttu-id="e585a-124">*AlignedBufferOffset* est un multiple de 8 octets</span><span class="sxs-lookup"><span data-stu-id="e585a-124">*AlignedBufferOffset* is a multiple of 8 bytes</span></span>
-   <span data-ttu-id="e585a-125">La ressource est une mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="e585a-125">The resource is a buffer</span></span>
-   <span data-ttu-id="e585a-126">L’opération est un membre valide de l’énumération</span><span class="sxs-lookup"><span data-stu-id="e585a-126">The operation is a valid member of the enumeration</span></span>
-   <span data-ttu-id="e585a-127">[**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) ne peut pas être appelé à partir d’un bundle</span><span class="sxs-lookup"><span data-stu-id="e585a-127">[**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) cannot be called from within a bundle</span></span>
-   <span data-ttu-id="e585a-128">Le type de liste de commandes prend en charge la prédicat</span><span class="sxs-lookup"><span data-stu-id="e585a-128">The command list type supports predication</span></span>
-   <span data-ttu-id="e585a-129">Le décalage ne dépasse pas la taille de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="e585a-129">The offset does not exceed the buffer size</span></span>

<span data-ttu-id="e585a-130">La couche de débogage génère une erreur si la mémoire tampon source n’est pas dans le [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (ce qui est identique à [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states), et simplement à un alias).</span><span class="sxs-lookup"><span data-stu-id="e585a-130">The debug layer will issue an error if the source buffer is not in the [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (which is the same as [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states), and simply an alias) state.</span></span>

<span data-ttu-id="e585a-131">L’ensemble d’opérations qui peut être prédicat est le suivant :</span><span class="sxs-lookup"><span data-stu-id="e585a-131">The set of operations which can be predicated are:</span></span>

-   [<span data-ttu-id="e585a-132">**DrawInstanced**</span><span class="sxs-lookup"><span data-stu-id="e585a-132">**DrawInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [<span data-ttu-id="e585a-133">**DrawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="e585a-133">**DrawIndexedInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [<span data-ttu-id="e585a-134">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="e585a-134">**Dispatch**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="e585a-135">**CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="e585a-135">**CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="e585a-136">**CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="e585a-136">**CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="e585a-137">**CopyResource**</span><span class="sxs-lookup"><span data-stu-id="e585a-137">**CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="e585a-138">**CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="e585a-138">**CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="e585a-139">**ResolveSubresource**</span><span class="sxs-lookup"><span data-stu-id="e585a-139">**ResolveSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [<span data-ttu-id="e585a-140">**ClearDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="e585a-140">**ClearDepthStencilView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [<span data-ttu-id="e585a-141">**ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="e585a-141">**ClearRenderTargetView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [<span data-ttu-id="e585a-142">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="e585a-142">**ClearUnorderedAccessViewUint**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="e585a-143">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="e585a-143">**ClearUnorderedAccessViewFloat**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="e585a-144">**ExecuteIndirect**</span><span class="sxs-lookup"><span data-stu-id="e585a-144">**ExecuteIndirect**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

<span data-ttu-id="e585a-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) n’est pas prédicat lui-même.</span><span class="sxs-lookup"><span data-stu-id="e585a-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) is not predicated itself.</span></span> <span data-ttu-id="e585a-146">Au lieu de cela, les opérations individuelles de la liste ci-dessus qui sont contenues dans le regroupement sont prédicats.</span><span class="sxs-lookup"><span data-stu-id="e585a-146">Instead, individual operations from the list above which are contained in side of the bundle are predicated.</span></span>

<span data-ttu-id="e585a-147">Les méthodes ID3D12GraphicsCommandList [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) et [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) ne sont pas prédicats.</span><span class="sxs-lookup"><span data-stu-id="e585a-147">The ID3D12GraphicsCommandList methods [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) and [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) are not predicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e585a-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e585a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e585a-149">Compteurs et requêtes</span><span class="sxs-lookup"><span data-stu-id="e585a-149">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="e585a-150">Mesure des performances</span><span class="sxs-lookup"><span data-stu-id="e585a-150">Performance Measurement</span></span>](performance-measurement.md)
</dt> <dt>

[<span data-ttu-id="e585a-151">Parcours des requêtes de prédicat</span><span class="sxs-lookup"><span data-stu-id="e585a-151">Predication queries walk-through</span></span>](predication-queries.md)
</dt> </dl>

 

 




