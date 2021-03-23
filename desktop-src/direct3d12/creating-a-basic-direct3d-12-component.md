---
title: Création d’un composant Direct3D 12 de base
description: Cette rubrique décrit le déroulement des appels pour créer un composant Direct3D 12 de base.
ms.assetid: A0FB108B-15C1-42AD-9277-D5CB63FA8329
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: d0c7ead9ce67ee23a0668304a006d6cd67fb3d67
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "104758859"
---
# <a name="creating-a-basic-direct3d-12-component"></a><span data-ttu-id="7176c-103">Création d’un composant Direct3D 12 de base</span><span class="sxs-lookup"><span data-stu-id="7176c-103">Creating a basic Direct3D 12 component</span></span>

> [!NOTE]
> <span data-ttu-id="7176c-104">Consultez les exemples de graphiques [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) référentiel pour DirectX 12 qui illustrent comment créer des applications nécessitant beaucoup de ressources graphiques pour Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7176c-104">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="7176c-105">Cette rubrique décrit le déroulement des appels pour créer un composant Direct3D 12 de base.</span><span class="sxs-lookup"><span data-stu-id="7176c-105">This topic describes the call flow to create a basic Direct3D 12 component.</span></span>

-   [<span data-ttu-id="7176c-106">Flow code pour une application simple</span><span class="sxs-lookup"><span data-stu-id="7176c-106">Code flow for a simple app</span></span>](#code-flow-for-a-simple-app)
    -   [<span data-ttu-id="7176c-107">Initialiser</span><span class="sxs-lookup"><span data-stu-id="7176c-107">Initialize</span></span>](#initialize)
    -   [<span data-ttu-id="7176c-108">Mettre à jour</span><span class="sxs-lookup"><span data-stu-id="7176c-108">Update</span></span>](#update)
    -   [<span data-ttu-id="7176c-109">Render</span><span class="sxs-lookup"><span data-stu-id="7176c-109">Render</span></span>](#render)
    -   [<span data-ttu-id="7176c-110">Suppression</span><span class="sxs-lookup"><span data-stu-id="7176c-110">Destroy</span></span>](#destroy)
-   [<span data-ttu-id="7176c-111">Exemple de code pour une application simple</span><span class="sxs-lookup"><span data-stu-id="7176c-111">Code example for a simple app</span></span>](#code-example-for-a-simple-app)
    -   [<span data-ttu-id="7176c-112">D3D12HelloTriangle de classe</span><span class="sxs-lookup"><span data-stu-id="7176c-112">class D3D12HelloTriangle</span></span>](#class-d3d12hellotriangle)
    -   [<span data-ttu-id="7176c-113">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="7176c-113">OnInit()</span></span>](#oninit)
    -   [<span data-ttu-id="7176c-114">LoadPipeline()</span><span class="sxs-lookup"><span data-stu-id="7176c-114">LoadPipeline()</span></span>](#loadpipeline)
    -   [<span data-ttu-id="7176c-115">LoadAssets()</span><span class="sxs-lookup"><span data-stu-id="7176c-115">LoadAssets()</span></span>](#loadassets)
    -   [<span data-ttu-id="7176c-116">OnUpdate ()</span><span class="sxs-lookup"><span data-stu-id="7176c-116">OnUpdate()</span></span>](#onupdate)
    -   [<span data-ttu-id="7176c-117">OnRender ()</span><span class="sxs-lookup"><span data-stu-id="7176c-117">OnRender()</span></span>](#onrender)
    -   [<span data-ttu-id="7176c-118">PopulateCommandList()</span><span class="sxs-lookup"><span data-stu-id="7176c-118">PopulateCommandList()</span></span>](#populatecommandlist)
    -   [<span data-ttu-id="7176c-119">WaitForPreviousFrame()</span><span class="sxs-lookup"><span data-stu-id="7176c-119">WaitForPreviousFrame()</span></span>](#waitforpreviousframe)
    -   [<span data-ttu-id="7176c-120">OnDestroy ()</span><span class="sxs-lookup"><span data-stu-id="7176c-120">OnDestroy()</span></span>](#ondestroy)
-   [<span data-ttu-id="7176c-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7176c-121">Related topics</span></span>](#related-topics)

## <a name="code-flow-for-a-simple-app"></a><span data-ttu-id="7176c-122">Flow code pour une application simple</span><span class="sxs-lookup"><span data-stu-id="7176c-122">Code flow for a simple app</span></span>

<span data-ttu-id="7176c-123">La boucle la plus à l’extérieur d’un programme D3D 12 suit un processus graphique très standard :</span><span class="sxs-lookup"><span data-stu-id="7176c-123">The outermost loop of a D3D 12 program follows a very standard graphics process:</span></span>

> [!TIP]
> <span data-ttu-id="7176c-124">Les nouvelles fonctionnalités de Direct3D 12 sont suivies d’une note.</span><span class="sxs-lookup"><span data-stu-id="7176c-124">Features new to Direct3D 12 are followed by a note.</span></span>

-   [<span data-ttu-id="7176c-125">Initialiser</span><span class="sxs-lookup"><span data-stu-id="7176c-125">Initialize</span></span>](#initialize)
-   <span data-ttu-id="7176c-126">**Tab**</span><span class="sxs-lookup"><span data-stu-id="7176c-126">**Repeat**</span></span>
    -   [<span data-ttu-id="7176c-127">Mettre à jour</span><span class="sxs-lookup"><span data-stu-id="7176c-127">Update</span></span>](#update)
    -   [<span data-ttu-id="7176c-128">Render</span><span class="sxs-lookup"><span data-stu-id="7176c-128">Render</span></span>](#render)
-   [<span data-ttu-id="7176c-129">Suppression</span><span class="sxs-lookup"><span data-stu-id="7176c-129">Destroy</span></span>](#destroy)

### <a name="initialize"></a><span data-ttu-id="7176c-130">Initialiser</span><span class="sxs-lookup"><span data-stu-id="7176c-130">Initialize</span></span>

<span data-ttu-id="7176c-131">L’initialisation implique d’abord la configuration des variables et des classes globales, et une fonction Initialize doit préparer le pipeline et les ressources.</span><span class="sxs-lookup"><span data-stu-id="7176c-131">Initialization involves first setting up the global variables and classes, and an initialize function must prepare the pipeline and assets.</span></span>

-   <span data-ttu-id="7176c-132">Initialisez le pipeline.</span><span class="sxs-lookup"><span data-stu-id="7176c-132">Initialize the pipeline.</span></span>
    -   <span data-ttu-id="7176c-133">Activez la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="7176c-133">Enable the debug layer.</span></span>
    -   <span data-ttu-id="7176c-134">Créez l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7176c-134">Create the device.</span></span>
    -   <span data-ttu-id="7176c-135">Créez la file d’attente de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-135">Create the command queue.</span></span>
    -   <span data-ttu-id="7176c-136">Créez la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="7176c-136">Create the swap chain.</span></span>
    -   <span data-ttu-id="7176c-137">Créez un tas de descripteurs de vue de la cible de rendu (RTV).</span><span class="sxs-lookup"><span data-stu-id="7176c-137">Create a render target view (RTV) descriptor heap.</span></span>
        > [!Note]  
        > <span data-ttu-id="7176c-138">Un [tas de descripteur](descriptor-heaps.md) peut être considéré comme un tableau de [descripteurs](descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="7176c-138">A [descriptor heap](descriptor-heaps.md) can be thought of as an array of [descriptors](descriptors.md).</span></span> <span data-ttu-id="7176c-139">Où chaque descripteur décrit complètement un objet au GPU.</span><span class="sxs-lookup"><span data-stu-id="7176c-139">Where each descriptor fully describes an object to the GPU.</span></span>

    -   <span data-ttu-id="7176c-140">Créer des ressources de frame (affichage de la cible de rendu pour chaque frame).</span><span class="sxs-lookup"><span data-stu-id="7176c-140">Create frame resources (a render target view for each frame).</span></span>
    -   <span data-ttu-id="7176c-141">Créez un allocateur de commande.</span><span class="sxs-lookup"><span data-stu-id="7176c-141">Create a command allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="7176c-142">Un allocateur de commande gère le stockage sous-jacent pour les [listes de commandes et les offres groupées](recording-command-lists-and-bundles.md).</span><span class="sxs-lookup"><span data-stu-id="7176c-142">A command allocator manages the underlying storage for [command lists and bundles](recording-command-lists-and-bundles.md).</span></span>
         
-   <span data-ttu-id="7176c-143">Initialisez les ressources.</span><span class="sxs-lookup"><span data-stu-id="7176c-143">Initialize the assets.</span></span>
    -   <span data-ttu-id="7176c-144">Créez une signature racine vide.</span><span class="sxs-lookup"><span data-stu-id="7176c-144">Create an empty root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="7176c-145">Une [signature racine](root-signatures.md) graphique définit les ressources qui sont liées au pipeline Graphics.</span><span class="sxs-lookup"><span data-stu-id="7176c-145">A graphics [root signature](root-signatures.md) defines what resources are bound to the graphics pipeline.</span></span>

    -   <span data-ttu-id="7176c-146">Compilez les nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="7176c-146">Compile the shaders.</span></span>
    -   <span data-ttu-id="7176c-147">Créez la disposition d’entrée de vertex.</span><span class="sxs-lookup"><span data-stu-id="7176c-147">Create the vertex input layout.</span></span>
    -   <span data-ttu-id="7176c-148">Créez une description de l' [objet d’État du pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) , puis créez l’objet.</span><span class="sxs-lookup"><span data-stu-id="7176c-148">Create a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) description, then create the object.</span></span>
        > [!Note]  
        > <span data-ttu-id="7176c-149">Un objet d’état de pipeline maintient l’état de tous les nuanceurs actuellement définis, ainsi que certains objets d’état de fonction fixes (tels que l' *assembleur d’entrée*, *Tesselator*, *rastériseur* et la *fusion de sortie*).</span><span class="sxs-lookup"><span data-stu-id="7176c-149">A pipeline state object maintains the state of all currently set shaders as well as certain fixed function state objects (such as the *input assembler*, *tesselator*, *rasterizer* and *output merger*).</span></span>

    -   <span data-ttu-id="7176c-150">Créez la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-150">Create the command list.</span></span>
    -   <span data-ttu-id="7176c-151">Fermez la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-151">Close the command list.</span></span>
    -   <span data-ttu-id="7176c-152">Créez et chargez les mémoires tampons de vertex.</span><span class="sxs-lookup"><span data-stu-id="7176c-152">Create and load the vertex buffers.</span></span>
    -   <span data-ttu-id="7176c-153">Créez les vues de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="7176c-153">Create the vertex buffer views.</span></span>
    -   <span data-ttu-id="7176c-154">Créez une clôture.</span><span class="sxs-lookup"><span data-stu-id="7176c-154">Create a fence.</span></span>
        > [!Note]  
        > <span data-ttu-id="7176c-155">Une clôture est utilisée pour synchroniser le processeur avec le GPU (consultez [synchronisation multimoteur](./user-mode-heap-synchronization.md)).</span><span class="sxs-lookup"><span data-stu-id="7176c-155">A fence is used to synchronize the CPU with the GPU (see [Multi-engine synchronization](./user-mode-heap-synchronization.md)).</span></span>

    -   <span data-ttu-id="7176c-156">Créez un descripteur d’événement.</span><span class="sxs-lookup"><span data-stu-id="7176c-156">Create an event handle.</span></span>
    -   <span data-ttu-id="7176c-157">Attendez la fin du GPU.</span><span class="sxs-lookup"><span data-stu-id="7176c-157">Wait for the GPU to finish.</span></span>
        > [!Note]  
        > <span data-ttu-id="7176c-158">Vérifiez la clôture !</span><span class="sxs-lookup"><span data-stu-id="7176c-158">Check on the fence!</span></span>

<span data-ttu-id="7176c-159">Reportez-vous à la [classe D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) et [LoadAssets](#loadassets).</span><span class="sxs-lookup"><span data-stu-id="7176c-159">Refer to [class D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) and [LoadAssets](#loadassets).</span></span>

### <a name="update"></a><span data-ttu-id="7176c-160">Update</span><span class="sxs-lookup"><span data-stu-id="7176c-160">Update</span></span>

<span data-ttu-id="7176c-161">Mettez à jour tout ce qui doit changer depuis la dernière image.</span><span class="sxs-lookup"><span data-stu-id="7176c-161">Update everything that should change since the last frame.</span></span>

-   <span data-ttu-id="7176c-162">Modifiez la constante, le vertex, les mémoires tampons d’index et tout le reste, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7176c-162">Modify the constant, vertex, index buffers, and everything else, as necessary.</span></span>

<span data-ttu-id="7176c-163">Reportez-vous à [OnUpdate](#onupdate).</span><span class="sxs-lookup"><span data-stu-id="7176c-163">Refer to [OnUpdate](#onupdate).</span></span>

### <a name="render"></a><span data-ttu-id="7176c-164">Rendu</span><span class="sxs-lookup"><span data-stu-id="7176c-164">Render</span></span>

<span data-ttu-id="7176c-165">Dessinez le nouveau monde.</span><span class="sxs-lookup"><span data-stu-id="7176c-165">Draw the new world.</span></span>

-   <span data-ttu-id="7176c-166">Remplissez la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-166">Populate the command list.</span></span>
    -   <span data-ttu-id="7176c-167">Réinitialisez l’allocation de liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-167">Reset the command list allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="7176c-168">Réutilisez la mémoire qui est associée à l’allocateur de commande.</span><span class="sxs-lookup"><span data-stu-id="7176c-168">Re-use the memory that is associated with the command allocator.</span></span>

         

    -   <span data-ttu-id="7176c-169">Réinitialisez la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-169">Reset the command list.</span></span>
    -   <span data-ttu-id="7176c-170">Définissez la signature racine graphique.</span><span class="sxs-lookup"><span data-stu-id="7176c-170">Set the graphics root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="7176c-171">Définit la signature de la racine graphique à utiliser pour la liste de commandes actuelle.</span><span class="sxs-lookup"><span data-stu-id="7176c-171">Sets the graphics root signature to use for the current command list.</span></span>

         

    -   <span data-ttu-id="7176c-172">Définissez les rectangles de la fenêtre d’affichage et de la ciseaux.</span><span class="sxs-lookup"><span data-stu-id="7176c-172">Set the viewport and scissor rectangles.</span></span>
    -   <span data-ttu-id="7176c-173">Définissez une barrière de ressources, indiquant que la mémoire tampon d’arrière-plan doit être utilisée comme cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="7176c-173">Set a resource barrier, indicating the back buffer is to be used as a render target.</span></span>
        > [!Note]  
        > <span data-ttu-id="7176c-174">Les barrières des ressources sont utilisées pour gérer les transitions de ressources.</span><span class="sxs-lookup"><span data-stu-id="7176c-174">Resource barriers are used to manage resource transitions.</span></span>

         

    -   <span data-ttu-id="7176c-175">Enregistrez les commandes dans la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-175">Record commands into the command list.</span></span>
    -   <span data-ttu-id="7176c-176">Indique que la mémoire tampon d’arrière-plan sera utilisée pour être présente après l’exécution de la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-176">Indicate the back buffer will be used to present after the command list has executed.</span></span>
        > [!Note]  
        > <span data-ttu-id="7176c-177">Un autre appel pour définir un cloisonnement des ressources.</span><span class="sxs-lookup"><span data-stu-id="7176c-177">Another call to set a resource barrier.</span></span>

         

    -   <span data-ttu-id="7176c-178">Fermez la liste de commandes pour l’enregistrement supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="7176c-178">Close the command list to further recording.</span></span>
-   <span data-ttu-id="7176c-179">Exécutez la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-179">Execute the command list.</span></span>
-   <span data-ttu-id="7176c-180">Présentez le frame.</span><span class="sxs-lookup"><span data-stu-id="7176c-180">Present the frame.</span></span>
-   <span data-ttu-id="7176c-181">Attendez la fin du GPU.</span><span class="sxs-lookup"><span data-stu-id="7176c-181">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="7176c-182">Continuez à mettre à jour et à vérifier la clôture.</span><span class="sxs-lookup"><span data-stu-id="7176c-182">Keep updating and checking the fence.</span></span>

<span data-ttu-id="7176c-183">Reportez-vous à [OnRender](#onrender).</span><span class="sxs-lookup"><span data-stu-id="7176c-183">Refer to [OnRender](#onrender).</span></span>

### <a name="destroy"></a><span data-ttu-id="7176c-184">Détruire</span><span class="sxs-lookup"><span data-stu-id="7176c-184">Destroy</span></span>

<span data-ttu-id="7176c-185">Fermez correctement l’application.</span><span class="sxs-lookup"><span data-stu-id="7176c-185">Cleanly close down the app.</span></span>

-   <span data-ttu-id="7176c-186">Attendez la fin du GPU.</span><span class="sxs-lookup"><span data-stu-id="7176c-186">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="7176c-187">Vérification finale de la clôture.</span><span class="sxs-lookup"><span data-stu-id="7176c-187">Final check on the fence.</span></span>

-   <span data-ttu-id="7176c-188">Fermez le descripteur d’événement.</span><span class="sxs-lookup"><span data-stu-id="7176c-188">Close the event handle.</span></span>

<span data-ttu-id="7176c-189">Reportez-vous à [OnDestroy](#ondestroy).</span><span class="sxs-lookup"><span data-stu-id="7176c-189">Refer to [OnDestroy](#ondestroy).</span></span>

## <a name="code-example-for-a-simple-app"></a><span data-ttu-id="7176c-190">Exemple de code pour une application simple</span><span class="sxs-lookup"><span data-stu-id="7176c-190">Code example for a simple app</span></span>

<span data-ttu-id="7176c-191">L’exemple suivant étend le déroulement du code ci-dessus pour inclure le code requis pour un exemple de base.</span><span class="sxs-lookup"><span data-stu-id="7176c-191">The following expands the code flow above to include the code required for a basic sample.</span></span>

### <a name="class-d3d12hellotriangle"></a><span data-ttu-id="7176c-192">D3D12HelloTriangle de classe</span><span class="sxs-lookup"><span data-stu-id="7176c-192">class D3D12HelloTriangle</span></span>

<span data-ttu-id="7176c-193">Commencez par définir la classe dans un fichier d’en-tête, y compris une fenêtre d’affichage, un rectangle à ciseaux et une mémoire tampon de vertex à l’aide des structures :</span><span class="sxs-lookup"><span data-stu-id="7176c-193">First define the class in a header file, including a viewport, scissor rectangle and vertex buffer using the structures:</span></span>

-   [<span data-ttu-id="7176c-194">**D3D12 \_ VIEWPORT**</span><span class="sxs-lookup"><span data-stu-id="7176c-194">**D3D12\_VIEWPORT**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [<span data-ttu-id="7176c-195">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="7176c-195">**D3D12\_RECT**</span></span>](d3d12-rect.md)
-   [<span data-ttu-id="7176c-196">**\_Vue de \_ mémoire tampon de vertex D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7176c-196">**D3D12\_VERTEX\_BUFFER\_VIEW**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

```cpp
#include "DXSample.h"

using namespace DirectX;
using namespace Microsoft::WRL;

class D3D12HelloTriangle : public DXSample
{
public:
    D3D12HelloTriangle(UINT width, UINT height, std::wstring name);

    virtual void OnInit();
    virtual void OnUpdate();
    virtual void OnRender();
    virtual void OnDestroy();

private:
    static const UINT FrameCount = 2;

    struct Vertex
    {
        XMFLOAT3 position;
        XMFLOAT4 color;
    };

    // Pipeline objects.
    D3D12_VIEWPORT m_viewport;
    D3D12_RECT m_scissorRect;
    ComPtr<IDXGISwapChain3> m_swapChain;
    ComPtr<ID3D12Device> m_device;
    ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
    ComPtr<ID3D12CommandAllocator> m_commandAllocator;
    ComPtr<ID3D12CommandQueue> m_commandQueue;
    ComPtr<ID3D12RootSignature> m_rootSignature;
    ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
    ComPtr<ID3D12PipelineState> m_pipelineState;
    ComPtr<ID3D12GraphicsCommandList> m_commandList;
    UINT m_rtvDescriptorSize;

    // App resources.
    ComPtr<ID3D12Resource> m_vertexBuffer;
    D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;

    // Synchronization objects.
    UINT m_frameIndex;
    HANDLE m_fenceEvent;
    ComPtr<ID3D12Fence> m_fence;
    UINT64 m_fenceValue;

    void LoadPipeline();
    void LoadAssets();
    void PopulateCommandList();
    void WaitForPreviousFrame();
};
```

### <a name="oninit"></a><span data-ttu-id="7176c-197">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="7176c-197">OnInit()</span></span>

<span data-ttu-id="7176c-198">Dans le fichier source principal des projets, commencez l’initialisation des objets :</span><span class="sxs-lookup"><span data-stu-id="7176c-198">In the projects main source file, start initializing the objects:</span></span>

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a><span data-ttu-id="7176c-199">LoadPipeline()</span><span class="sxs-lookup"><span data-stu-id="7176c-199">LoadPipeline()</span></span>

<span data-ttu-id="7176c-200">Le code suivant crée les bases pour un pipeline de graphiques.</span><span class="sxs-lookup"><span data-stu-id="7176c-200">The following code creates the basics for a graphics pipeline.</span></span> <span data-ttu-id="7176c-201">Le processus de création d’appareils et de chaînes de permutation est très similaire à Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="7176c-201">The process of creating devices and swap chains is very similar to Direct3D 11.</span></span>

-   <span data-ttu-id="7176c-202">Activez la couche de débogage avec des appels à :</span><span class="sxs-lookup"><span data-stu-id="7176c-202">Enable the debug layer, with calls to:</span></span><dl>

[<span data-ttu-id="7176c-203">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="7176c-203">**D3D12GetDebugInterface**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [<span data-ttu-id="7176c-204">**ID3D12Debug::EnableDebugLayer**</span><span class="sxs-lookup"><span data-stu-id="7176c-204">**ID3D12Debug::EnableDebugLayer**</span></span>](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   <span data-ttu-id="7176c-205">Créez l’appareil :</span><span class="sxs-lookup"><span data-stu-id="7176c-205">Create the device:</span></span><dl>

[<span data-ttu-id="7176c-206">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="7176c-206">**CreateDXGIFactory1**</span></span>](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [<span data-ttu-id="7176c-207">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="7176c-207">**D3D12CreateDevice**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   <span data-ttu-id="7176c-208">Renseignez une description de la file d’attente de commandes, puis créez la file d’attente de commandes :</span><span class="sxs-lookup"><span data-stu-id="7176c-208">Fill out a command queue description, then create the command queue:</span></span><dl>

[<span data-ttu-id="7176c-209">**Description de la \_ \_ file d’attente de commandes D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="7176c-209">**D3D12\_COMMAND\_QUEUE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [<span data-ttu-id="7176c-210">**ID3D12Device::CreateCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="7176c-210">**ID3D12Device::CreateCommandQueue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   <span data-ttu-id="7176c-211">Renseignez une description utilise permutation, puis créez la chaîne de permutation :</span><span class="sxs-lookup"><span data-stu-id="7176c-211">Fill out a swapchain description, then create the swap chain:</span></span> <dl>

[<span data-ttu-id="7176c-212">**Description de la \_ chaîne de permutation dxgi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7176c-212">**DXGI\_SWAP\_CHAIN\_DESC**</span></span>](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [<span data-ttu-id="7176c-213">**IDXGIFactory::CreateSwapChain**</span><span class="sxs-lookup"><span data-stu-id="7176c-213">**IDXGIFactory::CreateSwapChain**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [<span data-ttu-id="7176c-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span><span class="sxs-lookup"><span data-stu-id="7176c-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span></span>](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   <span data-ttu-id="7176c-215">Renseignez une description du tas.</span><span class="sxs-lookup"><span data-stu-id="7176c-215">Fill out a heap description.</span></span> <span data-ttu-id="7176c-216">Créez ensuite un tas de descripteur :</span><span class="sxs-lookup"><span data-stu-id="7176c-216">then create a descriptor heap:</span></span> <dl>

[<span data-ttu-id="7176c-217">**\_Description du tas du descripteur D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7176c-217">**D3D12\_DESCRIPTOR\_HEAP\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [<span data-ttu-id="7176c-218">**ID3D12Device::CreateDescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="7176c-218">**ID3D12Device::CreateDescriptorHeap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [<span data-ttu-id="7176c-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span><span class="sxs-lookup"><span data-stu-id="7176c-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   <span data-ttu-id="7176c-220">Créez la vue de la cible de rendu :</span><span class="sxs-lookup"><span data-stu-id="7176c-220">Create the render target view:</span></span> <dl>

[<span data-ttu-id="7176c-221">**\_Handle de \_ descripteur de processeur CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="7176c-221">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE**</span></span>](cd3dx12-cpu-descriptor-handle.md)  
    [<span data-ttu-id="7176c-222">**GetCPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="7176c-222">**GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="7176c-223">**IDXGISwapChain :: GetBuffer**</span><span class="sxs-lookup"><span data-stu-id="7176c-223">**IDXGISwapChain::GetBuffer**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [<span data-ttu-id="7176c-224">**ID3D12Device::CreateRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="7176c-224">**ID3D12Device::CreateRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   <span data-ttu-id="7176c-225">Créez l’allocateur de commande : [**ID3D12Device :: CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span><span class="sxs-lookup"><span data-stu-id="7176c-225">Create the command allocator: [**ID3D12Device::CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span></span>

<span data-ttu-id="7176c-226">Dans les étapes ultérieures, les listes de commandes sont obtenues à partir de l’allocateur de commande et envoyées à la file d’attente de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-226">In later steps, command lists are obtained from the command allocator and submitted to the command queue.</span></span>

<span data-ttu-id="7176c-227">Charger les dépendances du pipeline de rendu (Notez que la création d’un périphérique de distorsion logicielle est entièrement facultative).</span><span class="sxs-lookup"><span data-stu-id="7176c-227">Load the rendering pipeline dependencies (note that the creation of a software WARP device is entirely optional).</span></span>


```cpp
void D3D12HelloTriangle::LoadPipeline()
{
#if defined(_DEBUG)
    // Enable the D3D12 debug layer.
    {
        
        ComPtr<ID3D12Debug> debugController;
        if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&debugController))))
        {
            debugController->EnableDebugLayer();
        }
    }
#endif

    ComPtr<IDXGIFactory4> factory;
    ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&factory)));

    if (m_useWarpDevice)
    {
        ComPtr<IDXGIAdapter> warpAdapter;
        ThrowIfFailed(factory->EnumWarpAdapter(IID_PPV_ARGS(&warpAdapter)));

        ThrowIfFailed(D3D12CreateDevice(
            warpAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }
    else
    {
        ComPtr<IDXGIAdapter1> hardwareAdapter;
        GetHardwareAdapter(factory.Get(), &hardwareAdapter);

        ThrowIfFailed(D3D12CreateDevice(
            hardwareAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }

    // Describe and create the command queue.
    D3D12_COMMAND_QUEUE_DESC queueDesc = {};
    queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
    queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

    ThrowIfFailed(m_device->CreateCommandQueue(&queueDesc, IID_PPV_ARGS(&m_commandQueue)));

    // Describe and create the swap chain.
    DXGI_SWAP_CHAIN_DESC swapChainDesc = {};
    swapChainDesc.BufferCount = FrameCount;
    swapChainDesc.BufferDesc.Width = m_width;
    swapChainDesc.BufferDesc.Height = m_height;
    swapChainDesc.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
    swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
    swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_DISCARD;
    swapChainDesc.OutputWindow = Win32Application::GetHwnd();
    swapChainDesc.SampleDesc.Count = 1;
    swapChainDesc.Windowed = TRUE;

    ComPtr<IDXGISwapChain> swapChain;
    ThrowIfFailed(factory->CreateSwapChain(
        m_commandQueue.Get(),        // Swap chain needs the queue so that it can force a flush on it.
        &swapChainDesc,
        &swapChain
        ));

    ThrowIfFailed(swapChain.As(&m_swapChain));

    // This sample does not support fullscreen transitions.
    ThrowIfFailed(factory->MakeWindowAssociation(Win32Application::GetHwnd(), DXGI_MWA_NO_ALT_ENTER));

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();

    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
            rtvHandle.Offset(1, m_rtvDescriptorSize);
        }
    }

    ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
}
```



### <a name="loadassets"></a><span data-ttu-id="7176c-228">LoadAssets()</span><span class="sxs-lookup"><span data-stu-id="7176c-228">LoadAssets()</span></span>

<span data-ttu-id="7176c-229">Le chargement et la préparation des ressources sont un processus long.</span><span class="sxs-lookup"><span data-stu-id="7176c-229">Loading and preparing assets is a lengthy process.</span></span> <span data-ttu-id="7176c-230">La plupart de ces étapes sont similaires à D3D 11, bien que d’autres soient nouvelles dans D3D 12.</span><span class="sxs-lookup"><span data-stu-id="7176c-230">Many of these stages are similar to D3D 11, though some are new to D3D 12.</span></span>

<span data-ttu-id="7176c-231">Dans Direct3D 12, l’état de pipeline requis est attaché à une liste de commandes via un [objet d’état de pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO).</span><span class="sxs-lookup"><span data-stu-id="7176c-231">In Direct3D 12, required pipeline state is attached to a command list via a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO).</span></span> <span data-ttu-id="7176c-232">Cet exemple montre comment créer un PSO.</span><span class="sxs-lookup"><span data-stu-id="7176c-232">This example shows how to create a PSO.</span></span> <span data-ttu-id="7176c-233">Vous pouvez stocker l’PSO en tant que variable membre et le réutiliser autant de fois que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7176c-233">You can store the PSO as a member variable and reuse it as many times as needed.</span></span>

<span data-ttu-id="7176c-234">Un tas de descripteur définit les vues et comment accéder aux ressources (par exemple, une vue de cible de rendu).</span><span class="sxs-lookup"><span data-stu-id="7176c-234">A descriptor heap defines the views and how to access resources (for example, a render target view).</span></span>

<span data-ttu-id="7176c-235">À l’aide de l’allocateur de liste de commandes et d’PSO, vous pouvez créer la liste de commandes réelle, qui sera exécutée ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="7176c-235">With the command list allocator and PSO, you can create the actual command list, which will be executed at a later time.</span></span>

<span data-ttu-id="7176c-236">Les API et les processus suivants sont appelés successivement.</span><span class="sxs-lookup"><span data-stu-id="7176c-236">The following APIs and processes are called in succession.</span></span>

-   <span data-ttu-id="7176c-237">Créez une signature racine vide à l’aide de la structure d’assistance disponible :</span><span class="sxs-lookup"><span data-stu-id="7176c-237">Create an empty root signature, using the available helper structure:</span></span> <dl>

[<span data-ttu-id="7176c-238">**Description de la \_ signature racine CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7176c-238">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md)  
    [<span data-ttu-id="7176c-239">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="7176c-239">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [<span data-ttu-id="7176c-240">**ID3D12Device::CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="7176c-240">**ID3D12Device::CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   <span data-ttu-id="7176c-241">Chargez et compilez les nuanceurs : [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span><span class="sxs-lookup"><span data-stu-id="7176c-241">Load and compile the shaders: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span></span>
-   <span data-ttu-id="7176c-242">Créez la disposition d’entrée du vertex : description de l' [**\_ \_ élément \_ d’entrée D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="7176c-242">Create the vertex input layout: [**D3D12\_INPUT\_ELEMENT\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span></span>
-   <span data-ttu-id="7176c-243">Renseignez une description de l’état du pipeline, à l’aide des structures d’assistance disponibles, puis créez l’état du pipeline Graphics :</span><span class="sxs-lookup"><span data-stu-id="7176c-243">Fill out a pipeline state description, using the helper structures available, then create the graphics pipeline state:</span></span> <dl>

[<span data-ttu-id="7176c-244">**Description de l' \_ \_ État du pipeline GRAPHICs D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7176c-244">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [<span data-ttu-id="7176c-245">**CD3DX12 \_ rastériseur \_ desc**</span><span class="sxs-lookup"><span data-stu-id="7176c-245">**CD3DX12\_RASTERIZER\_DESC**</span></span>](cd3dx12-rasterizer-desc.md)  
    [<span data-ttu-id="7176c-246">**CD3DX12 \_ Blend \_ desc**</span><span class="sxs-lookup"><span data-stu-id="7176c-246">**CD3DX12\_BLEND\_DESC**</span></span>](cd3dx12-blend-desc.md)  
    [<span data-ttu-id="7176c-247">**ID3D12Device::CreateGraphicsPipelineState**</span><span class="sxs-lookup"><span data-stu-id="7176c-247">**ID3D12Device::CreateGraphicsPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   <span data-ttu-id="7176c-248">Créer, puis fermer, une liste de commandes :</span><span class="sxs-lookup"><span data-stu-id="7176c-248">Create, then close, a command list:</span></span> <dl>

[<span data-ttu-id="7176c-249">**ID3D12Device::CreateCommandList**</span><span class="sxs-lookup"><span data-stu-id="7176c-249">**ID3D12Device::CreateCommandList**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [<span data-ttu-id="7176c-250">**ID3D12GraphicsCommandList :: Close**</span><span class="sxs-lookup"><span data-stu-id="7176c-250">**ID3D12GraphicsCommandList::Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   <span data-ttu-id="7176c-251">Créez la mémoire tampon de vertex : [**ID3D12Device :: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="7176c-251">Create the vertex buffer: [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>
-   <span data-ttu-id="7176c-252">Copiez les données de vertex dans la mémoire tampon de vertex :</span><span class="sxs-lookup"><span data-stu-id="7176c-252">Copy the vertex data to the vertex buffer:</span></span><dl>

[<span data-ttu-id="7176c-253">**ID3D12Resource :: Map**</span><span class="sxs-lookup"><span data-stu-id="7176c-253">**ID3D12Resource::Map**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [<span data-ttu-id="7176c-254">**ID3D12Resource :: DEMAPPAGE**</span><span class="sxs-lookup"><span data-stu-id="7176c-254">**ID3D12Resource::Unmap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   <span data-ttu-id="7176c-255">Initialisez la vue de mémoire tampon de vertex : [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span><span class="sxs-lookup"><span data-stu-id="7176c-255">Initialize the vertex buffer view: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span></span>
-   <span data-ttu-id="7176c-256">Créez et initialisez la clôture : [**ID3D12Device :: CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span><span class="sxs-lookup"><span data-stu-id="7176c-256">Create and initialize the fence: [**ID3D12Device::CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span></span>
-   <span data-ttu-id="7176c-257">Créez un handle d’événement à utiliser avec la synchronisation de frames.</span><span class="sxs-lookup"><span data-stu-id="7176c-257">Create an event handle for use with frame synchronization.</span></span>
-   <span data-ttu-id="7176c-258">Attendez la fin du GPU.</span><span class="sxs-lookup"><span data-stu-id="7176c-258">Wait for the GPU to finish.</span></span>


```cpp
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_UPLOAD);
        auto desc = CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize);
        ThrowIfFailed(m_device->CreateCommittedResource(
            &heapProps,
            D3D12_HEAP_FLAG_NONE,
            &desc,
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



### <a name="onupdate"></a><span data-ttu-id="7176c-259">OnUpdate ()</span><span class="sxs-lookup"><span data-stu-id="7176c-259">OnUpdate()</span></span>

<span data-ttu-id="7176c-260">Pour un exemple simple, rien n’est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7176c-260">For a simple example, nothing is updated.</span></span>


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a><span data-ttu-id="7176c-261">OnRender ()</span><span class="sxs-lookup"><span data-stu-id="7176c-261">OnRender()</span></span>

<span data-ttu-id="7176c-262">Pendant la configuration, la variable membre **m \_ commandList** a été utilisée pour enregistrer et exécuter toutes les commandes de configuration.</span><span class="sxs-lookup"><span data-stu-id="7176c-262">During set up, the member variable **m\_commandList** was used to record and execute all of the set up commands.</span></span> <span data-ttu-id="7176c-263">Vous pouvez maintenant réutiliser ce membre dans la boucle de rendu principale.</span><span class="sxs-lookup"><span data-stu-id="7176c-263">You can now reuse that member in the main render loop.</span></span>

<span data-ttu-id="7176c-264">Le rendu implique un appel pour remplir la liste de commandes, puis la liste de commandes peut être exécutée et la mémoire tampon suivante dans la chaîne de permutation présentée :</span><span class="sxs-lookup"><span data-stu-id="7176c-264">Rendering involves a call to populate the command list, then the command list can be executed and the next buffer in the swap chain presented:</span></span>

-   <span data-ttu-id="7176c-265">Remplissez la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-265">Populate the command list.</span></span>
-   <span data-ttu-id="7176c-266">Exécutez la commande list : [**ID3D12CommandQueue :: ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="7176c-266">Execute the command list: [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>
-   <span data-ttu-id="7176c-267">[**IDXGISwapChain1 ::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) le frame.</span><span class="sxs-lookup"><span data-stu-id="7176c-267">[**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) the frame.</span></span>
-   <span data-ttu-id="7176c-268">Attendez la fin de l’exécution du GPU.</span><span class="sxs-lookup"><span data-stu-id="7176c-268">Wait on the GPU to finish.</span></span>


```cpp
void D3D12HelloTriangle::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(1, 0));

    WaitForPreviousFrame();
}
```



### <a name="populatecommandlist"></a><span data-ttu-id="7176c-269">PopulateCommandList()</span><span class="sxs-lookup"><span data-stu-id="7176c-269">PopulateCommandList()</span></span>

<span data-ttu-id="7176c-270">Vous devez réinitialiser l’allocateur de liste de commandes et la liste de commandes elle-même avant de pouvoir les réutiliser.</span><span class="sxs-lookup"><span data-stu-id="7176c-270">You must reset the command list allocator and the command list itself before you can reuse them.</span></span> <span data-ttu-id="7176c-271">Dans les scénarios plus avancés, il peut être judicieux de réinitialiser l’allocateur à chaque trame.</span><span class="sxs-lookup"><span data-stu-id="7176c-271">In more advanced scenarios it might make sense to reset the allocator every several frames.</span></span> <span data-ttu-id="7176c-272">La mémoire est associée à l’allocateur qui ne peut pas être libéré immédiatement après l’exécution d’une liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-272">Memory is associated with the allocator that can't be released immediately after executing a command list.</span></span> <span data-ttu-id="7176c-273">Cet exemple montre comment réinitialiser l’allocateur après chaque frame.</span><span class="sxs-lookup"><span data-stu-id="7176c-273">This example shows how to reset the allocator after every frame.</span></span>

<span data-ttu-id="7176c-274">À présent, réutilisez la liste de commandes pour le frame actuel.</span><span class="sxs-lookup"><span data-stu-id="7176c-274">Now, reuse the command list for the current frame.</span></span> <span data-ttu-id="7176c-275">Rattachez la fenêtre d’affichage à la liste de commandes (qui doit être effectuée chaque fois qu’une liste de commandes est réinitialisée, et avant l’exécution de la liste de commandes), indiquez que la ressource sera utilisée en tant que cible de rendu, enregistrer les commandes, puis indiquer que la cible de rendu sera utilisée lors de l’exécution de la liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="7176c-275">Reattach the viewport to the command list (which must be done whenever a command list is reset, and before the command list is executed), indicate that the resource will be in use as a render target, record commands, and then indicate that the render target will be used to present when the command list is done executing.</span></span>

<span data-ttu-id="7176c-276">Le remplissage des listes de commandes appelle à son tour les méthodes et les processus suivants :</span><span class="sxs-lookup"><span data-stu-id="7176c-276">Populating command lists calls the following methods and processes in turn:</span></span>

-   <span data-ttu-id="7176c-277">Réinitialisez l’allocateur de commande et la liste des commandes :</span><span class="sxs-lookup"><span data-stu-id="7176c-277">Reset the command allocator, and command list:</span></span> <dl>

[<span data-ttu-id="7176c-278">**ID3D12CommandAllocator :: Reset**</span><span class="sxs-lookup"><span data-stu-id="7176c-278">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [<span data-ttu-id="7176c-279">**ID3D12GraphicsCommandList :: Reset**</span><span class="sxs-lookup"><span data-stu-id="7176c-279">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   <span data-ttu-id="7176c-280">Définissez la signature racine, les rectangles de la fenêtre d’affichage et des ciseaux :</span><span class="sxs-lookup"><span data-stu-id="7176c-280">Set the root signature, viewport and scissors rectangles:</span></span> <dl>

[<span data-ttu-id="7176c-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span><span class="sxs-lookup"><span data-stu-id="7176c-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [<span data-ttu-id="7176c-282">**ID3D12GraphicsCommandList::RSSetViewports**</span><span class="sxs-lookup"><span data-stu-id="7176c-282">**ID3D12GraphicsCommandList::RSSetViewports**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [<span data-ttu-id="7176c-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span><span class="sxs-lookup"><span data-stu-id="7176c-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   <span data-ttu-id="7176c-284">Indique que la mémoire tampon d’arrière-plan doit être utilisée comme cible de rendu :</span><span class="sxs-lookup"><span data-stu-id="7176c-284">Indicate that the back buffer is to be used as a render target:</span></span> <dl>

[<span data-ttu-id="7176c-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span><span class="sxs-lookup"><span data-stu-id="7176c-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [<span data-ttu-id="7176c-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="7176c-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="7176c-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span><span class="sxs-lookup"><span data-stu-id="7176c-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   <span data-ttu-id="7176c-288">Enregistrez les commandes :</span><span class="sxs-lookup"><span data-stu-id="7176c-288">Record the commands:</span></span><dl>

[<span data-ttu-id="7176c-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="7176c-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [<span data-ttu-id="7176c-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span><span class="sxs-lookup"><span data-stu-id="7176c-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [<span data-ttu-id="7176c-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="7176c-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [<span data-ttu-id="7176c-292">**ID3D12GraphicsCommandList ::D rawInstanced**</span><span class="sxs-lookup"><span data-stu-id="7176c-292">**ID3D12GraphicsCommandList::DrawInstanced**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   <span data-ttu-id="7176c-293">Indiquez que la mémoire tampon d’arrière-plan sera maintenant utilisée pour présenter : [**ID3D12GraphicsCommandList :: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="7176c-293">Indicate the back buffer will now be used to present: [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>
-   <span data-ttu-id="7176c-294">Fermez la liste de commandes : [**ID3D12GraphicsCommandList :: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span><span class="sxs-lookup"><span data-stu-id="7176c-294">Close the command list: [**ID3D12GraphicsCommandList::Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span></span>


```cpp
void D3D12HelloTriangle::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocator->Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
    m_commandList->RSSetViewports(1, &m_viewport);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
    m_commandList->ResourceBarrier(1, &barrier);

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->DrawInstanced(3, 1, 0, 0);

    // Indicate that the back buffer will now be used to present.
    barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
    m_commandList->ResourceBarrier(1, &barrier);

    ThrowIfFailed(m_commandList->Close());
}
```



### <a name="waitforpreviousframe"></a><span data-ttu-id="7176c-295">WaitForPreviousFrame()</span><span class="sxs-lookup"><span data-stu-id="7176c-295">WaitForPreviousFrame()</span></span>

<span data-ttu-id="7176c-296">Le code suivant illustre une utilisation plus simple des délimiteurs.</span><span class="sxs-lookup"><span data-stu-id="7176c-296">The following code shows an over-simplified use of fences.</span></span>

> [!Note]  
> <span data-ttu-id="7176c-297">L’attente de la fin d’une trame est trop inefficace pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="7176c-297">Waiting for a frame to complete is too inefficient for most apps.</span></span>

 

<span data-ttu-id="7176c-298">Les API et les processus suivants sont appelés dans l’ordre :</span><span class="sxs-lookup"><span data-stu-id="7176c-298">The following APIs and processes are called in order:</span></span>

-   [<span data-ttu-id="7176c-299">**ID3D12CommandQueue :: signal**</span><span class="sxs-lookup"><span data-stu-id="7176c-299">**ID3D12CommandQueue::Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [<span data-ttu-id="7176c-300">**ID3D12Fence::GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="7176c-300">**ID3D12Fence::GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [<span data-ttu-id="7176c-301">**ID3D12Fence::SetEventOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="7176c-301">**ID3D12Fence::SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   <span data-ttu-id="7176c-302">Attendez l’événement.</span><span class="sxs-lookup"><span data-stu-id="7176c-302">Wait for the event.</span></span>
-   <span data-ttu-id="7176c-303">Mettez à jour l’index de frame : [**IDXGISwapChain3 :: GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span><span class="sxs-lookup"><span data-stu-id="7176c-303">Update the frame index: [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span></span>


```cpp
void D3D12HelloTriangle::WaitForPreviousFrame()
{
    // WAITING FOR THE FRAME TO COMPLETE BEFORE CONTINUING IS NOT BEST PRACTICE.
    // This is code implemented as such for simplicity. More advanced samples 
    // illustrate how to use fences for efficient resource usage.

    // Signal and increment the fence value.
    const UINT64 fence = m_fenceValue;
    ThrowIfFailed(m_commandQueue->Signal(m_fence.Get(), fence));
    m_fenceValue++;

    // Wait until the previous frame is finished.
    if (m_fence->GetCompletedValue() < fence)
    {
        ThrowIfFailed(m_fence->SetEventOnCompletion(fence, m_fenceEvent));
        WaitForSingleObject(m_fenceEvent, INFINITE);
    }

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();
}
```



### <a name="ondestroy"></a><span data-ttu-id="7176c-304">OnDestroy ()</span><span class="sxs-lookup"><span data-stu-id="7176c-304">OnDestroy()</span></span>

<span data-ttu-id="7176c-305">Fermez correctement l’application.</span><span class="sxs-lookup"><span data-stu-id="7176c-305">Cleanly close down the app.</span></span>

-   <span data-ttu-id="7176c-306">Attendez la fin du GPU.</span><span class="sxs-lookup"><span data-stu-id="7176c-306">Wait for the GPU to finish.</span></span>
-   <span data-ttu-id="7176c-307">Fermez l’événement.</span><span class="sxs-lookup"><span data-stu-id="7176c-307">Close the event.</span></span>


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a><span data-ttu-id="7176c-308">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7176c-308">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7176c-309">Comprendre Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7176c-309">Understanding Direct3D 12</span></span>](directx-12-getting-started.md)
</dt> <dt>

[<span data-ttu-id="7176c-310">Exemples fonctionnels</span><span class="sxs-lookup"><span data-stu-id="7176c-310">Working Samples</span></span>](working-samples.md)
</dt> </dl>

 

 
