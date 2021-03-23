---
title: Glossaire Direct3D 12
description: Ces termes sont distincts de Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548591"
---
# <a name="direct3d-12-glossary"></a><span data-ttu-id="a8814-103">Glossaire Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a8814-103">Direct3D 12 glossary</span></span>

<span data-ttu-id="a8814-104">Ces termes sont distincts de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="a8814-104">These terms are distinctive of Direct3D 12.</span></span>

<dl> <dt>

<span data-ttu-id="a8814-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**liant**</span><span class="sxs-lookup"><span data-stu-id="a8814-105"><span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-106">Processus d’attachement de la mémoire au pipeline Graphics.</span><span class="sxs-lookup"><span data-stu-id="a8814-106">The process of attaching memory to the graphics pipeline.</span></span> <span data-ttu-id="a8814-107">La liaison de ressources, par exemple, implique la liaison d’une ressource, telle qu’une texture au pipeline, pour une utilisation lors du rendu d’un objet.</span><span class="sxs-lookup"><span data-stu-id="a8814-107">Resource binding, for example, involves the binding of a resource such as a texture to the pipeline, for use in rendering an object.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**mémoire tampon**</span><span class="sxs-lookup"><span data-stu-id="a8814-108"><span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**buffer**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-109">Type de ressource D3D synonyme d’une allocation de mémoire contiguë.</span><span class="sxs-lookup"><span data-stu-id="a8814-109">A type of D3D resource that is synonymous with a contiguous memory allocation.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**lots**</span><span class="sxs-lookup"><span data-stu-id="a8814-110"><span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**bundle**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-111">Mémoire tampon de commande que l’unité de traitement graphique (GPU) peut exécuter uniquement directement par le biais d’une *liste de commandes directe*.</span><span class="sxs-lookup"><span data-stu-id="a8814-111">A command buffer that the graphics processing unit (GPU) can execute only directly via a *direct command list*.</span></span> <span data-ttu-id="a8814-112">Un bundle hérite de tous les États GPU (à l’exception de l' *objet d’état de pipeline* actuellement défini et de la topologie primitive).</span><span class="sxs-lookup"><span data-stu-id="a8814-112">A bundle inherits all GPU state (except for the currently set *pipeline state object* and primitive topology).</span></span>

</dd> <dt>

<span data-ttu-id="a8814-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**allocateur de commande**</span><span class="sxs-lookup"><span data-stu-id="a8814-113"><span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**command allocator**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-114">Allocations de mémoire sous-jacentes dans lesquelles sont stockées les commandes GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-114">The underlying memory allocations in which GPU commands are stored.</span></span> <span data-ttu-id="a8814-115">L’objet d’allocation de commande s’applique à la fois à des *listes de commandes directes* et à des *offres groupées*.</span><span class="sxs-lookup"><span data-stu-id="a8814-115">The command allocator object applies to both *direct command lists* and *bundles*.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**Liste des commandes**</span><span class="sxs-lookup"><span data-stu-id="a8814-116"><span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**command list**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-117">Une liste de commandes correspond à un ensemble de commandes que le GPU exécute.</span><span class="sxs-lookup"><span data-stu-id="a8814-117">A command list corresponds to a set of commands which the GPU executes.</span></span> <span data-ttu-id="a8814-118">Celles-ci incluent des commandes telles que la définition d’État, de dessin, d’effacement et de copie.</span><span class="sxs-lookup"><span data-stu-id="a8814-118">These include commands such as to set state, draw, clear, and copy.</span></span> <span data-ttu-id="a8814-119">L’interface de la liste de commandes D3D12 est très différente de l’interface de la liste de commandes D3D11.</span><span class="sxs-lookup"><span data-stu-id="a8814-119">The D3D12 command list interface is significantly different than the D3D11 command list interface.</span></span> <span data-ttu-id="a8814-120">L’interface de la liste de commandes D3D12 contient des API similaires aux API de rendu de contexte de périphérique D3D11.</span><span class="sxs-lookup"><span data-stu-id="a8814-120">The D3D12 command list interface contains APIs similar to the D3D11 device context rendering APIs.</span></span>

<span data-ttu-id="a8814-121">Une liste de commandes D3D12 ne mappe pas les ressources et ne les annule pas, ne modifie pas les mappages de vignettes, ne redimensionne pas les pools de mosaïques, ne récupère pas les données de requête et n’envoie jamais des commandes au GPU en vue de leur exécution.</span><span class="sxs-lookup"><span data-stu-id="a8814-121">A D3D12 command list does not map or unmap resources, change tile mappings, resize tile pools, get query data, nor does it ever implicitly submit commands to the GPU for execution.</span></span>

<span data-ttu-id="a8814-122">Contrairement aux contextes différés de D3D11, les listes de commandes D3D12 prennent uniquement en charge deux niveaux d’indirection.</span><span class="sxs-lookup"><span data-stu-id="a8814-122">Unlike D3D11 deferred contexts, D3D12 command lists only support two levels of indirection.</span></span> <span data-ttu-id="a8814-123">Une *liste de commandes directe* correspond à une mémoire tampon de commande que le GPU peut exécuter.</span><span class="sxs-lookup"><span data-stu-id="a8814-123">A *direct command list* corresponds to a command buffer which the GPU can execute.</span></span> <span data-ttu-id="a8814-124">Une *offre groupée* ne peut être exécutée que directement via une liste de commandes directe.</span><span class="sxs-lookup"><span data-stu-id="a8814-124">A *bundle* can be executed only directly via a direct command list.</span></span>

<span data-ttu-id="a8814-125">Une liste de commandes directe n’hérite d’aucun État GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-125">A direct command list does not inherit any GPU state.</span></span> <span data-ttu-id="a8814-126">Un bundle hérite de tous les États GPU (à l’exception de l’objet d’état de pipeline actuellement défini et de la topologie primitive).</span><span class="sxs-lookup"><span data-stu-id="a8814-126">A bundle inherits all GPU state (except for the currently set pipeline state object and primitive topology).</span></span>

<span data-ttu-id="a8814-127">La mémoire pour une liste de commandes est définie par l' *allocateur de commande*.</span><span class="sxs-lookup"><span data-stu-id="a8814-127">Memory for a command list is set by the *command allocator*.</span></span> <span data-ttu-id="a8814-128">L’objectif des listes de commandes est qu’elles peuvent être envoyées à un GPU sous la forme d’une demande de rendu unique.</span><span class="sxs-lookup"><span data-stu-id="a8814-128">The purpose of command lists is that they can be submitted to a GPU as a single rendering request.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**file d’attente de commandes**</span><span class="sxs-lookup"><span data-stu-id="a8814-129"><span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**command queue**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-130">Une file d’attente de *commandes répertorie* les exécutions successives du GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-130">A queue of *command lists* that the GPU executes in succession.</span></span> <span data-ttu-id="a8814-131">Les applications doivent envoyer explicitement des *listes de commandes* à une file d’attente de commandes pour exécution.</span><span class="sxs-lookup"><span data-stu-id="a8814-131">Applications must explicitly submit *command lists* to a command queue for execution.</span></span> <span data-ttu-id="a8814-132">En général, il existe trois files d’attente de commandes : les graphiques 3D, Compute et Copy, qui correspondent au pipeline graphique 3D, au moteur de calcul et à un ou plusieurs moteurs de copie sur le GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-132">Typically there are three command queues: 3D graphics, compute and copy, corresponding to the 3D graphics pipeline, the compute engine, and one or more copy engines, on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**pixellisation conservatrice**</span><span class="sxs-lookup"><span data-stu-id="a8814-133"><span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**conservative rasterization**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-134">La pixellisation conservatrice est un mode de fonctionnement pour l’étape de rastérisation du pipeline graphique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="a8814-134">Conservative rasterization is a mode of operation for the rasterizer stage of the Direct3D graphics pipeline.</span></span> <span data-ttu-id="a8814-135">Il désactive la pixellisation standard basée sur les échantillons et pixellise à la place un pixel qui est couvert par n’importe quelle quantité par une primitive.</span><span class="sxs-lookup"><span data-stu-id="a8814-135">It disables the standard sample-based rasterization, and will instead rasterize a pixel that is covered by any amount by a primitive.</span></span> <span data-ttu-id="a8814-136">Une distinction importante est que, alors que toute couverture produit un pixel pixellisé, cette couverture ne peut pas être caractérisée par le matériel. par conséquent, la couverture apparaît toujours en binaire dans un nuanceur de pixels : entièrement couvertes ou non couvertes.</span><span class="sxs-lookup"><span data-stu-id="a8814-136">One important distinction is that, while any coverage at all produces a rasterized pixel, that coverage cannot be characterized by the hardware, so coverage always appears binary to a pixel shader: either fully covered or not covered.</span></span> <span data-ttu-id="a8814-137">Il est laissé au code du nuanceur de pixels pour déterminer de façon analytique la couverture réelle.</span><span class="sxs-lookup"><span data-stu-id="a8814-137">It is left to the pixel shader code to analytically determine the actual coverage.</span></span>

<span data-ttu-id="a8814-138">La pixellisation conservatrice peut être utile avec des problèmes tels que la détection des collisions et des collisions, compartimentage et l’élimination des occlusions, où la couleur d’un pixel est plus certaine et les cas limites peuvent être éliminés.</span><span class="sxs-lookup"><span data-stu-id="a8814-138">Conservative rasterization can help with such problems as collision and hit detection, binning, and occlusion culling, where the color of a pixel is more certain and edge cases can be eliminated.</span></span> <span data-ttu-id="a8814-139">Consultez [pixellisation conservatrice](conservative-rasterization.md).</span><span class="sxs-lookup"><span data-stu-id="a8814-139">See [Conservative Rasterization](conservative-rasterization.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8814-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Vue de la mémoire tampon constante (CBV)**</span><span class="sxs-lookup"><span data-stu-id="a8814-140"><span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Constant Buffer View (CBV)**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-141">Les mémoires tampons constantes contiennent des données constantes de nuanceur, telles qu’une vue caméra, des matrices de projection et des matrices universelles.</span><span class="sxs-lookup"><span data-stu-id="a8814-141">Constant buffers contain shader constant data, such as a camera view, projection matrices, and world matrices.</span></span> <span data-ttu-id="a8814-142">Une « vue de mémoire tampon constante » est la vue spécifique au format de la mémoire tampon telle qu’elle est affichée par le pipeline Graphics.</span><span class="sxs-lookup"><span data-stu-id="a8814-142">A "constant buffer view" is the format-specific view of the buffer as seen by the graphics pipeline.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**tas par défaut**</span><span class="sxs-lookup"><span data-stu-id="a8814-143"><span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**default heap**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-144">Segment de mémoire en mode utilisateur qui se concentre sur la prise en charge des types de ressources GPU persistants, y compris les ressources écrites par GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-144">A user-mode heap that is focused on supporting persistent GPU resource types, including GPU-written resources.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**Description**</span><span class="sxs-lookup"><span data-stu-id="a8814-145"><span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-146">Les descripteurs sont l’unité principale de liaison pour une seule ressource dans D3D12.</span><span class="sxs-lookup"><span data-stu-id="a8814-146">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span> <span data-ttu-id="a8814-147">Un descripteur est un bloc de données relativement petit, qui décrit entièrement un objet au GPU, dans un format spécifique au GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-147">A descriptor is a relatively small block of data that fully describes an object to the GPU, in a GPU specific format.</span></span> <span data-ttu-id="a8814-148">Il existe de nombreux types différents de descripteurs : les vues des ressources de nuanceur (SRVs), les vues d’accès non ordonnées (UAVs), les vues de mémoire tampon constante (CBVs) et les échantillonneurs sont quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="a8814-148">There are many different types of descriptors: Shader Resource Views (SRVs), Unordered Access Views (UAVs), Constant Buffer Views (CBVs), and Samplers are a few examples.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**tas du descripteur**</span><span class="sxs-lookup"><span data-stu-id="a8814-149"><span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**descriptor heap**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-150">Un tas de descripteur est une collection d’allocations contiguës de descripteurs, une allocation pour chaque descripteur.</span><span class="sxs-lookup"><span data-stu-id="a8814-150">A descriptor heap is a collection of contiguous allocations of descriptors, one allocation for every descriptor.</span></span> <span data-ttu-id="a8814-151">Le point principal d’un tas de descripteur doit englober l’essentiel de l’allocation de mémoire nécessaire pour stocker les spécifications de descripteur des types d’objets que les nuanceurs référencent dans le cadre d’une fenêtre de rendu aussi grande que possible (idéalement une image entière de rendu ou plus).</span><span class="sxs-lookup"><span data-stu-id="a8814-151">The primary point of a descriptor heap is to encompass the bulk of memory allocation required for storing the descriptor specifications of object types that shaders reference for as large of a window of rendering as possible (ideally an entire frame of rendering or more).</span></span>

</dd> <dt>

<span data-ttu-id="a8814-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**tableau du descripteur**</span><span class="sxs-lookup"><span data-stu-id="a8814-152"><span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**descriptor table**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-153">Une table de descripteur est logiquement un tableau de descripteurs.</span><span class="sxs-lookup"><span data-stu-id="a8814-153">A descriptor table is logically an array of descriptors.</span></span> <span data-ttu-id="a8814-154">Chaque table de descripteur stocke des descripteurs d’un ou plusieurs types, notamment SRVs, UAVe, CBVs et échantillonneurs.</span><span class="sxs-lookup"><span data-stu-id="a8814-154">Each descriptor table stores descriptors of one or more types, including SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="a8814-155">Une table de descripteurs n’est pas une allocation de mémoire, il s’agit simplement d’un décalage et d’une longueur dans un tas de descripteur.</span><span class="sxs-lookup"><span data-stu-id="a8814-155">A descriptor table is not an allocation of memory, it is simply an offset and length into a descriptor heap.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**liste de commandes directe**</span><span class="sxs-lookup"><span data-stu-id="a8814-156"><span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**direct command list**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-157">Mémoire tampon de commande que le GPU peut exécuter.</span><span class="sxs-lookup"><span data-stu-id="a8814-157">A command buffer that the GPU can execute.</span></span> <span data-ttu-id="a8814-158">Une liste de commandes directe n’hérite d’aucun État GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-158">A direct command list doesn't inherit any GPU state.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**peindre**</span><span class="sxs-lookup"><span data-stu-id="a8814-159"><span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**fence**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-160">Mécanisme de synchronisation du GPU et de l’UC.</span><span class="sxs-lookup"><span data-stu-id="a8814-160">A mechanism to synchronize the GPU and CPU.</span></span> <span data-ttu-id="a8814-161">Le GPU et le processeur peuvent être demandés à attendre une clôture, en attendant que l’autre processeur rattrape son retard.</span><span class="sxs-lookup"><span data-stu-id="a8814-161">Both the GPU and CPU can be instructed to wait at a fence, waiting in effect for the other processor to catch up.</span></span> <span data-ttu-id="a8814-162">Consultez [synchronisation multimoteur](./user-mode-heap-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="a8814-162">See [Multi-engine synchronization](./user-mode-heap-synchronization.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8814-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**risque, suivi des risques**</span><span class="sxs-lookup"><span data-stu-id="a8814-163"><span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**hazard, hazard tracking**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-164">Un risque se produit lorsqu’une ressource a été utilisée à un usage unique et que l’application a l’intention de la réutiliser à d’autres fins.</span><span class="sxs-lookup"><span data-stu-id="a8814-164">A hazard occurs when a resource has been used for one purpose, and the app intends to reuse it for another purpose.</span></span> <span data-ttu-id="a8814-165">Pour réutiliser la ressource, les caches intermédiaires doivent être vidés ou invalidés, les exigences de compression doivent être cohérentes avec la deuxième utilisation, et la ressource doit être dans l’État requis pour éviter de lire la ressource une fois qu’elle a été écrite et invalidée dans le but prévu.</span><span class="sxs-lookup"><span data-stu-id="a8814-165">In order to use the resource again, intermediate caches will need to be flushed or invalidated, compression requirements will need to be consistent with the second use, and the resource should be in the required state to avoid reading the resource after it has been written to and invalidated for the intended purpose.</span></span>

<span data-ttu-id="a8814-166">Le processus de gestion des ressources et d’évitement de ces problèmes de synchronisation est appelé suivi des risques.</span><span class="sxs-lookup"><span data-stu-id="a8814-166">The process of maintaining resources and avoiding these sync issues is known as hazard tracking.</span></span> <span data-ttu-id="a8814-167">S’il n’y a aucun suivi de risque par le pilote, l’application est responsable de cette tâche.</span><span class="sxs-lookup"><span data-stu-id="a8814-167">If there is no hazard tracking by the driver, then the app is responsible for this.</span></span> <span data-ttu-id="a8814-168">Dans la plupart des versions antérieures de DirectX, le suivi des dangers était géré par le pilote.</span><span class="sxs-lookup"><span data-stu-id="a8814-168">In most earlier versions of DirectX, hazard tracking was handled by the driver.</span></span> <span data-ttu-id="a8814-169">Pour améliorer les performances, les méthodes sans suivi des risques sont disponibles dans DirectX 12.</span><span class="sxs-lookup"><span data-stu-id="a8814-169">To improve performance, methods without hazard tracking are available in DirectX 12.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**HLSL (High-Level Shader Language)**</span><span class="sxs-lookup"><span data-stu-id="a8814-170"><span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level Shader Language (HLSL)**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-171">Un langage informatique, similaire mais distinct de nombreuses façons à partir de C, utilisé pour écrire le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a8814-171">A computer language, similar but distinct in many ways from C, that is used to write shader code.</span></span> <span data-ttu-id="a8814-172">Les nuanceurs vertex, pixel, Geometry, Compute, Domain et coque sont tous écrits en HLSL.</span><span class="sxs-lookup"><span data-stu-id="a8814-172">Vertex, pixel, geometry, compute, domain, and hull shaders are all written using HLSL.</span></span> <span data-ttu-id="a8814-173">Un compilateur convertit la source HLSL en un format binaire que le GPU doit consommer.</span><span class="sxs-lookup"><span data-stu-id="a8814-173">A compiler converts the HLSL source into a binary format for the GPU to consume.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multimoteur**</span><span class="sxs-lookup"><span data-stu-id="a8814-174"><span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-175">Les différentes instances et types de moteurs dans une seule unité GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-175">The different instances and types of engines in a single GPU.</span></span> <span data-ttu-id="a8814-176">Les types de moteurs sont les suivants : Graphics, Compute et Copy.</span><span class="sxs-lookup"><span data-stu-id="a8814-176">The types of engines include: graphics, compute, and copy.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span><span class="sxs-lookup"><span data-stu-id="a8814-177"><span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-178">Une configuration matérielle où il existe plusieurs cartes graphiques.</span><span class="sxs-lookup"><span data-stu-id="a8814-178">A hardware configuration where there is more than one graphics adapter.</span></span> <span data-ttu-id="a8814-179">Les adaptateurs distincts sont parfois appelés des nœuds.</span><span class="sxs-lookup"><span data-stu-id="a8814-179">The separate adapters are sometimes referred to as nodes.</span></span> <span data-ttu-id="a8814-180">Avoir plusieurs GPU peut faire en sorte que la tâche de les synchroniser avec l’UC, et l’autre, est considérablement plus complexe qu’avec une seule GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-180">Having multiple GPUs can make the task of synchronizing them with the CPU, and each other, considerably more complex than with a single GPU.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Objet d’État du pipeline (PSO)**</span><span class="sxs-lookup"><span data-stu-id="a8814-181"><span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Pipeline State object (PSO)**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-182">Partie significative de l’état du GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-182">A significant portion of the state of the GPU.</span></span> <span data-ttu-id="a8814-183">Cet État comprend tous les nuanceurs actuellement définis et certains objets d’état de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="a8814-183">This state includes all currently set shaders and certain fixed-function state objects.</span></span> <span data-ttu-id="a8814-184">La seule façon de modifier les États contenus dans l’objet de pipeline est de modifier l’objet de pipeline actuellement lié.</span><span class="sxs-lookup"><span data-stu-id="a8814-184">The only way to change states contained within the pipeline object is to change the currently bound pipeline object.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**prédication**</span><span class="sxs-lookup"><span data-stu-id="a8814-185"><span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predication**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-186">Un prédicat est une fonctionnalité qui permet au GPU plutôt qu’au processeur de déterminer de ne pas dessiner, copier ou distribuer un objet.</span><span class="sxs-lookup"><span data-stu-id="a8814-186">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span> <span data-ttu-id="a8814-187">Par exemple, si un cadre englobant d’un objet est entièrement bloqués par un autre objet ou si la perspective a réduit l’objet à une valeur inférieure à la taille d’un pixel, il est possible qu’il n’y ait aucun point de tentative de dessin de l’objet masqué.</span><span class="sxs-lookup"><span data-stu-id="a8814-187">For example, if a bounding box of an object is totally occluded by another object or perspective has reduced the object to less than the size of a pixel, there may be no point in attempting to draw the hidden object at all.</span></span> <span data-ttu-id="a8814-188">Consultez [predicate](predication.md).</span><span class="sxs-lookup"><span data-stu-id="a8814-188">See [Predication](predication.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8814-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Vue de l’ordre du rastériseur (ROV)**</span><span class="sxs-lookup"><span data-stu-id="a8814-189"><span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Rasterizer Order View (ROV)**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-190">Les pipelines graphiques standard peuvent avoir des difficultés à converser correctement ensemble plusieurs textures qui contiennent de la transparence.</span><span class="sxs-lookup"><span data-stu-id="a8814-190">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="a8814-191">Les objets tels que les clôtures de câble, les fumées, les incendies, les végétations et les verres de couleur utilisent la transparence pour atteindre l’effet souhaité.</span><span class="sxs-lookup"><span data-stu-id="a8814-191">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="a8814-192">Des problèmes surviennent lorsque plusieurs textures contenant de la transparence sont alignées les unes avec les autres (fumée devant une clôture devant une couche de verre contenant de la végétation, par exemple).</span><span class="sxs-lookup"><span data-stu-id="a8814-192">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="a8814-193">Les vues triées du rastériseur (ROVs) permettent aux algorithmes de transparence des commandes (OIT) sous-jacents d’utiliser les fonctionnalités du matériel pour tenter de résoudre correctement l’ordre de transparence.</span><span class="sxs-lookup"><span data-stu-id="a8814-193">Rasterizer ordered views (ROVs) enable the underlying Order Independent Transparency (OIT) algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="a8814-194">La transparence est gérée par le nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="a8814-194">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="a8814-195">Les vues triées du rastériseur (ROVs) autorisent le code du nuanceur de pixels à marquer des liaisons de vue d’accès non triée (UAV) avec une déclaration qui modifie les exigences normales pour l’ordre des résultats de pipeline graphique pour UAVs.</span><span class="sxs-lookup"><span data-stu-id="a8814-195">Rasterizer Ordered Views (ROVs) allow pixel shader code to mark Unordered Access View (UAV) bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**tas readback**</span><span class="sxs-lookup"><span data-stu-id="a8814-196"><span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**readback heap**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-197">Segment de mémoire en mode utilisateur qui se concentre sur le transfert de données du GPU vers le processeur.</span><span class="sxs-lookup"><span data-stu-id="a8814-197">A user-mode heap that is focused on data transfer from the GPU back to the CPU.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**ressource**</span><span class="sxs-lookup"><span data-stu-id="a8814-198"><span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**resource**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-199">Entité qui fournit des données au pipeline et définit ce qui est rendu au cours de votre scène.</span><span class="sxs-lookup"><span data-stu-id="a8814-199">An entity that provides data to the pipeline and defines what is rendered during your scene.</span></span> <span data-ttu-id="a8814-200">Les ressources peuvent être chargées à partir de votre support de jeu ou créées dynamiquement au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="a8814-200">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="a8814-201">En règle générale, les ressources incluent des données de texture, des données de vertex et des données de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a8814-201">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="a8814-202">La plupart des applications Direct3D créent et détruisent largement les ressources tout au long de leur durée de vie.</span><span class="sxs-lookup"><span data-stu-id="a8814-202">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**barrière des ressources**</span><span class="sxs-lookup"><span data-stu-id="a8814-203"><span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**resource barrier**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-204">Une barrière de ressources informe le pilote que la synchronisation de plusieurs accès à une ressource unique peut être nécessaire, par exemple, la lecture et l’écriture dans la même texture.</span><span class="sxs-lookup"><span data-stu-id="a8814-204">A resource barrier notifies the driver that synchronization of multiple accesses to a single resource may be required, for example, reading and writing to the same texture.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**liaison de ressource**</span><span class="sxs-lookup"><span data-stu-id="a8814-205"><span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**resource binding**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-206">La liaison de ressources est le processus qui consiste à lier des ressources (textures, mémoires tampons de vertex, tampons d’index, etc.) au pipeline Graphics, ce qui permet aux nuanceurs du pipeline de traiter la ressource correcte.</span><span class="sxs-lookup"><span data-stu-id="a8814-206">Resource binding is the process of linking resources (textures, vertex buffers, index buffers, and so on), to the graphics pipeline, enabling the shaders of the pipeline to process the correct resource.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**tas de ressources**</span><span class="sxs-lookup"><span data-stu-id="a8814-207"><span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**resource heaps**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-208">Les tas de ressources sont un terme générique pour les segments de mémoire tampon qui sont mis de côté pour contenir des ressources lors de leur transfert vers et depuis le GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-208">Resource heaps is a generic term for the heaps that are memory buffers set aside to hold resources as they are transferred to and from the GPU.</span></span> <span data-ttu-id="a8814-209">Un transfert vers le GPU requiert un tas de chargement, du GPU au processeur requiert un segment de mémoire readback, et un segment de mémoire persistant pour le GPU à gérer sur plusieurs frames de rendu est appelé un tas par défaut.</span><span class="sxs-lookup"><span data-stu-id="a8814-209">A transfer to the GPU requires an Upload Heap, from the GPU to the CPU requires a Readback Heap, and a persistent heap for the GPU to maintain over multiple rendering frames is called a Default Heap.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**signature racine**</span><span class="sxs-lookup"><span data-stu-id="a8814-210"><span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**root signature**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-211">Les signatures racines définissent toutes les ressources qui doivent être liées aux pipelines graphiques, ou de calcul.</span><span class="sxs-lookup"><span data-stu-id="a8814-211">Root signatures define all the resources that are to be bound to the graphics, or compute, pipelines.</span></span> <span data-ttu-id="a8814-212">Une signature racine est configurée par les listes de commandes App et Links aux ressources dont les nuanceurs ont besoin en général, il existe un graphique et une signature racine de calcul par application.</span><span class="sxs-lookup"><span data-stu-id="a8814-212">A root signature is configured by the app and links command lists to the resources that the shaders require Typically, there is one graphics and one compute root signature per app.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**échantillonneur**</span><span class="sxs-lookup"><span data-stu-id="a8814-213"><span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**sampler**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-214">Un échantillonneur est du code qui lit à partir d’une texture.</span><span class="sxs-lookup"><span data-stu-id="a8814-214">A sampler is code that reads from a texture.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Affichage des ressources du nuanceur (SRV)**</span><span class="sxs-lookup"><span data-stu-id="a8814-215"><span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader Resource View (SRV)**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-216">Moyen spécifique au format d’examiner les données dans une ressource de nuanceur, telle qu’une texture.</span><span class="sxs-lookup"><span data-stu-id="a8814-216">A format-specific way to look at the data in a shader resource, such as a texture.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**tas statique**</span><span class="sxs-lookup"><span data-stu-id="a8814-217"><span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**static heap**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-218">Segment de mémoire en mode utilisateur qui se concentre sur plusieurs ressources de lecture seule GPU qui sont généralement utilisées en même temps et qui ne sont pas souvent modifiées.</span><span class="sxs-lookup"><span data-stu-id="a8814-218">A user-mode heap that is focused on multiple GPU-read-only resources that are typically used at the same time and are not changed frequently.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**chaîne de permutation**</span><span class="sxs-lookup"><span data-stu-id="a8814-219"><span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-220">Les chaînes d’échange contrôlent la rotation de la mémoire tampon d’arrière-plan, formant ainsi la base de l’animation graphique.</span><span class="sxs-lookup"><span data-stu-id="a8814-220">Swap chains control the back buffer rotation, forming the basis of graphics animation.</span></span> <span data-ttu-id="a8814-221">Les chaînes d’échange sont gérées par l’API Set de bas niveau DXGI (consultez [vue d’ensemble d’dxgi](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span><span class="sxs-lookup"><span data-stu-id="a8814-221">Swap chains are handled by the low level API set DXGI (see [DXGI Overview](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a8814-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span><span class="sxs-lookup"><span data-stu-id="a8814-222"><span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-223">Technique de recherche de données multidimensionnelles en mémoire, de sorte que les données de la dimensionnalité proche ont tendance à avoir des adresses à proximité.</span><span class="sxs-lookup"><span data-stu-id="a8814-223">A technique of locating multidimensional data in memory such that data of nearby dimensionality tends to have nearby addresses.</span></span> <span data-ttu-id="a8814-224">En particulier, toutes les données d’une ligne ne se trouvent pas à l’emplacement contigu avant les données de la ligne suivante.</span><span class="sxs-lookup"><span data-stu-id="a8814-224">In particular, all the data for one row is not located contiguously before the data for the next row.</span></span> <span data-ttu-id="a8814-225">Une « Swizzle paramétrable » décrit une méthode standardisée pour décrire des modèles de Swizzle.</span><span class="sxs-lookup"><span data-stu-id="a8814-225">A "Parameterized Swizzle" describes a standardized way to describe swizzle patterns.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**motif**</span><span class="sxs-lookup"><span data-stu-id="a8814-226"><span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**texture**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-227">Type de ressource D3D à plusieurs dimensions et dont la disposition mémoire est optimisée pour l’accès multidimensionnel à partir du GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-227">A type of D3D resource that is multi-dimensional and has a memory layout that is optimized for multi-dimensional access from the GPU.</span></span> <span data-ttu-id="a8814-228">Les textures contiennent souvent l’image brute requise pour le rendu sur une surface, avant l’éclairage et la fusion, mais peut contenir d’autres formes de données telles que des dégradés de couleur et des couleurs de référence.</span><span class="sxs-lookup"><span data-stu-id="a8814-228">Textures often contain the raw image required to render onto a surface, before lighting and blending takes place, but can contain other forms of data such as color gradients and reference colors.</span></span> <span data-ttu-id="a8814-229">Direct3D 12 prend en charge une, deux et trois textures unidimensionnelles.</span><span class="sxs-lookup"><span data-stu-id="a8814-229">Direct3D 12 supports one, two, and three dimensional textures.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**disposé**</span><span class="sxs-lookup"><span data-stu-id="a8814-230"><span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**tile**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-231">Page de la mémoire vidéo, similaire à une page UC/système de mémoire.</span><span class="sxs-lookup"><span data-stu-id="a8814-231">A page of video memory, similar to a CPU/System page of memory.</span></span> <span data-ttu-id="a8814-232">La notation de vignette permet de distinguer le sous-système de mémoire virtuelle du GPU du sous-système de mémoire virtuelle de l’UC.</span><span class="sxs-lookup"><span data-stu-id="a8814-232">The tile notation helps to distinguish the GPU virtual memory subsystem from the CPU virtual memory subsystem.</span></span> <span data-ttu-id="a8814-233">Les GPU offrent des fonctionnalités de mémoire virtuelle similaires à celles de la mémoire virtuelle du système.</span><span class="sxs-lookup"><span data-stu-id="a8814-233">GPUs provide similar virtual memory capabilities as system virtual memory.</span></span> <span data-ttu-id="a8814-234">Certains GPU ont des fonctionnalités de mémoire virtuelle partagées, qui permettent le partage de certaines pages du sous-système de mémoire virtuelle avec l’UC et le GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-234">Some GPUs have shared virtual memory capabilities, which allow for the sharing of some pages of the virtual memory subsystem with both the CPU and GPU.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**ressources en mosaïque**</span><span class="sxs-lookup"><span data-stu-id="a8814-235"><span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-236">Les ressources en mosaïque sont nécessaires, si bien que la mémoire GPU est gaspillée, le stockage des régions de surfaces que l’application connaît n’est pas accessible et le matériel peut comprendre comment filtrer les vignettes adjacentes.</span><span class="sxs-lookup"><span data-stu-id="a8814-236">Tiled resources are needed so less GPU memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span> <span data-ttu-id="a8814-237">Les ressources en mosaïque sont des ressources logiques volumineuses, mais elles nécessitent de petites quantités de mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="a8814-237">Tiled resources are large logical resources, but requiring small amounts of physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Vue d’accès non triée (UAV)**</span><span class="sxs-lookup"><span data-stu-id="a8814-238"><span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unordered Access View (UAV)**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-239">Une vue d’accès non ordonnée dans une ressource (qui comprend des mémoires tampons, des textures et des tableaux de textures sans échantillonnage multiple) autorise un accès en lecture/écriture non ordonné de manière temporelle à partir de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="a8814-239">An unordered access view into a resource (which includes buffers, textures, and texture arrays - without multi-sampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="a8814-240">Cela signifie que ce type de ressource peut être lu/écrit simultanément par plusieurs threads sans générer de conflits de mémoire.</span><span class="sxs-lookup"><span data-stu-id="a8814-240">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**charger le tas**</span><span class="sxs-lookup"><span data-stu-id="a8814-241"><span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**upload heap**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-242">Segment de mémoire en mode utilisateur qui se concentre sur le transfert de données du processeur vers le GPU.</span><span class="sxs-lookup"><span data-stu-id="a8814-242">A user-mode heap that is focused on data transfer from the CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**segment de mémoire en mode utilisateur**</span><span class="sxs-lookup"><span data-stu-id="a8814-243"><span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**user-mode heap**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-244">Collection d’allocations de mémoire volumineuses et contiguës qui sont recyclées sans conscience du composant de noyau : les méthodes d’allocation et de destruction n’appellent pas les méthodes d’allocation et de destruction du noyau dans un état stable.</span><span class="sxs-lookup"><span data-stu-id="a8814-244">A collection of large, contiguous memory allocations that are recycled without any kernel component's awareness: the allocation and destruction methods do not call kernel allocation and destruction methods during steady state.</span></span> <span data-ttu-id="a8814-245">Les tas upload, readback et default sont des variantes de tas en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a8814-245">Upload, Readback, and Default heaps are variants of user mode heaps.</span></span>

</dd> <dt>

<span data-ttu-id="a8814-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**ressources en mosaïque de volume**</span><span class="sxs-lookup"><span data-stu-id="a8814-246"><span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**volume tiled resources**</span></span>
</dt> <dd>

<span data-ttu-id="a8814-247">[Ressources en mosaïque](/windows)en trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="a8814-247">Three-dimensional [tiled resources](/windows).</span></span>

</dd> </dl>

 

 