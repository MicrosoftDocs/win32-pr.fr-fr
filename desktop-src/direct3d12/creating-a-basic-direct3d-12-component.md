---
title: Création d’un composant Direct3D 12 de base
description: Cette rubrique décrit le déroulement des appels pour créer un composant Direct3D 12 de base.
ms.assetid: A0FB108B-15C1-42AD-9277-D5CB63FA8329
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: d0c7ead9ce67ee23a0668304a006d6cd67fb3d67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404349"
---
# <a name="creating-a-basic-direct3d-12-component"></a>Création d’un composant Direct3D 12 de base

> [!NOTE]
> Consultez les exemples de graphiques [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) référentiel pour DirectX 12 qui montrent comment créer des applications nécessitant beaucoup de ressources graphiques pour Windows 10.

Cette rubrique décrit le déroulement des appels pour créer un composant Direct3D 12 de base.

-   [Flow code pour une application simple](#code-flow-for-a-simple-app)
    -   [Initialiser](#initialize)
    -   [Mettre à jour](#update)
    -   [Render](#render)
    -   [Suppression](#destroy)
-   [Exemple de code pour une application simple](#code-example-for-a-simple-app)
    -   [D3D12HelloTriangle de classe](#class-d3d12hellotriangle)
    -   [OnInit ()](#oninit)
    -   [LoadPipeline()](#loadpipeline)
    -   [LoadAssets()](#loadassets)
    -   [OnUpdate ()](#onupdate)
    -   [OnRender ()](#onrender)
    -   [PopulateCommandList()](#populatecommandlist)
    -   [WaitForPreviousFrame()](#waitforpreviousframe)
    -   [OnDestroy ()](#ondestroy)
-   [Rubriques connexes](#related-topics)

## <a name="code-flow-for-a-simple-app"></a>Flow code pour une application simple

La boucle la plus à l’extérieur d’un programme D3D 12 suit un processus graphique très standard :

> [!TIP]
> Les nouvelles fonctionnalités de Direct3D 12 sont suivies d’une note.

-   [Initialiser](#initialize)
-   **Tab**
    -   [Mettre à jour](#update)
    -   [Render](#render)
-   [Suppression](#destroy)

### <a name="initialize"></a>Initialiser

L’initialisation implique d’abord la configuration des variables et des classes globales, et une fonction Initialize doit préparer le pipeline et les ressources.

-   Initialisez le pipeline.
    -   Activez la couche de débogage.
    -   Créez l’appareil.
    -   Créez la file d’attente de commandes.
    -   Créez la chaîne de permutation.
    -   Créez un tas de descripteurs de vue de la cible de rendu (RTV).
        > [!Note]  
        > Un [tas de descripteur](descriptor-heaps.md) peut être considéré comme un tableau de [descripteurs](descriptors.md). Où chaque descripteur décrit complètement un objet au GPU.

    -   Créer des ressources de frame (affichage de la cible de rendu pour chaque frame).
    -   Créez un allocateur de commande.
        > [!Note]  
        > Un allocateur de commande gère le stockage sous-jacent pour les [listes de commandes et les offres groupées](recording-command-lists-and-bundles.md).
         
-   Initialisez les ressources.
    -   Créez une signature racine vide.
        > [!Note]  
        > Une [signature racine](root-signatures.md) graphique définit les ressources qui sont liées au pipeline Graphics.

    -   Compilez les nuanceurs.
    -   Créez la disposition d’entrée de vertex.
    -   Créez une description de l' [objet d’État du pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) , puis créez l’objet.
        > [!Note]  
        > Un objet d’état de pipeline maintient l’état de tous les nuanceurs actuellement définis, ainsi que certains objets d’état de fonction fixes (tels que l' *assembleur d’entrée*, *Tesselator*, *rastériseur* et la *fusion de sortie*).

    -   Créez la liste de commandes.
    -   Fermez la liste de commandes.
    -   Créez et chargez les mémoires tampons de vertex.
    -   Créez les vues de la mémoire tampon de vertex.
    -   Créez une clôture.
        > [!Note]  
        > Une clôture est utilisée pour synchroniser le processeur avec le GPU (consultez [synchronisation multimoteur](./user-mode-heap-synchronization.md)).

    -   Créez un descripteur d’événement.
    -   Attendez la fin du GPU.
        > [!Note]  
        > Vérifiez la clôture !

Reportez-vous à la [classe D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) et [LoadAssets](#loadassets).

### <a name="update"></a>Update

Mettez à jour tout ce qui doit changer depuis la dernière image.

-   Modifiez la constante, le vertex, les mémoires tampons d’index et tout le reste, si nécessaire.

Reportez-vous à [OnUpdate](#onupdate).

### <a name="render"></a>Rendu

Dessinez le nouveau monde.

-   Remplissez la liste de commandes.
    -   Réinitialisez l’allocation de liste de commandes.
        > [!Note]  
        > Réutilisez la mémoire qui est associée à l’allocateur de commande.

         

    -   Réinitialisez la liste de commandes.
    -   Définissez la signature racine graphique.
        > [!Note]  
        > Définit la signature de la racine graphique à utiliser pour la liste de commandes actuelle.

         

    -   Définissez les rectangles de la fenêtre d’affichage et de la ciseaux.
    -   Définissez une barrière de ressources, indiquant que la mémoire tampon d’arrière-plan doit être utilisée comme cible de rendu.
        > [!Note]  
        > Les barrières des ressources sont utilisées pour gérer les transitions de ressources.

         

    -   Enregistrez les commandes dans la liste de commandes.
    -   Indique que la mémoire tampon d’arrière-plan sera utilisée pour être présente après l’exécution de la liste de commandes.
        > [!Note]  
        > Un autre appel pour définir un cloisonnement des ressources.

         

    -   Fermez la liste de commandes pour l’enregistrement supplémentaire.
-   Exécutez la liste de commandes.
-   Présentez le frame.
-   Attendez la fin du GPU.
    > [!Note]  
    > Continuez à mettre à jour et à vérifier la clôture.

Reportez-vous à [OnRender](#onrender).

### <a name="destroy"></a>Détruire

Fermez correctement l’application.

-   Attendez la fin du GPU.
    > [!Note]  
    > Vérification finale de la clôture.

-   Fermez le descripteur d’événement.

Reportez-vous à [OnDestroy](#ondestroy).

## <a name="code-example-for-a-simple-app"></a>Exemple de code pour une application simple

L’exemple suivant étend le déroulement du code ci-dessus pour inclure le code requis pour un exemple de base.

### <a name="class-d3d12hellotriangle"></a>D3D12HelloTriangle de classe

Commencez par définir la classe dans un fichier d’en-tête, y compris une fenêtre d’affichage, un rectangle à ciseaux et une mémoire tampon de vertex à l’aide des structures :

-   [**D3D12 \_ VIEWPORT**](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [**D3D12 \_ Rect**](d3d12-rect.md)
-   [**\_Vue de \_ mémoire tampon de vertex D3D12 \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

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

### <a name="oninit"></a>OnInit ()

Dans le fichier source principal des projets, commencez l’initialisation des objets :

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a>LoadPipeline()

Le code suivant crée les bases pour un pipeline de graphiques. Le processus de création d’appareils et de chaînes de permutation est très similaire à Direct3D 11.

-   Activez la couche de débogage avec des appels à :<dl>

[**D3D12GetDebugInterface**](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [**ID3D12Debug::EnableDebugLayer**](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   Créez l’appareil :<dl>

[**CreateDXGIFactory1**](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   Renseignez une description de la file d’attente de commandes, puis créez la file d’attente de commandes :<dl>

[**Description de la \_ \_ file d’attente de commandes D3D12 \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [**ID3D12Device::CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   Renseignez une description utilise permutation, puis créez la chaîne de permutation : <dl>

[**Description de la \_ chaîne de permutation dxgi \_ \_**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [**IDXGIFactory::CreateSwapChain**](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   Renseignez une description du tas. Créez ensuite un tas de descripteur : <dl>

[**\_Description du tas du descripteur D3D12 \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [**ID3D12Device::CreateDescriptorHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   Créez la vue de la cible de rendu : <dl>

[**\_Handle de \_ descripteur de processeur CD3DX12 \_**](cd3dx12-cpu-descriptor-handle.md)  
    [**GetCPUDescriptorHandleForHeapStart**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**IDXGISwapChain :: GetBuffer**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [**ID3D12Device::CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   Créez l’allocateur de commande : [**ID3D12Device :: CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).

Dans les étapes ultérieures, les listes de commandes sont obtenues à partir de l’allocateur de commande et envoyées à la file d’attente de commandes.

Charger les dépendances du pipeline de rendu (Notez que la création d’un périphérique de distorsion logicielle est entièrement facultative).


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



### <a name="loadassets"></a>LoadAssets()

Le chargement et la préparation des ressources sont un processus long. La plupart de ces étapes sont similaires à D3D 11, bien que d’autres soient nouvelles dans D3D 12.

Dans Direct3D 12, l’état de pipeline requis est attaché à une liste de commandes via un [objet d’état de pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO). Cet exemple montre comment créer un PSO. Vous pouvez stocker l’PSO en tant que variable membre et le réutiliser autant de fois que nécessaire.

Un tas de descripteur définit les vues et comment accéder aux ressources (par exemple, une vue de cible de rendu).

À l’aide de l’allocateur de liste de commandes et d’PSO, vous pouvez créer la liste de commandes réelle, qui sera exécutée ultérieurement.

Les API et les processus suivants sont appelés successivement.

-   Créez une signature racine vide à l’aide de la structure d’assistance disponible : <dl>

[**Description de la \_ signature racine CD3DX12 \_ \_**](cd3dx12-root-signature-desc.md)  
    [**D3D12SerializeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [**ID3D12Device::CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   Chargez et compilez les nuanceurs : [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).
-   Créez la disposition d’entrée du vertex : description de l' [**\_ \_ élément \_ d’entrée D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).
-   Renseignez une description de l’état du pipeline, à l’aide des structures d’assistance disponibles, puis créez l’état du pipeline Graphics : <dl>

[**Description de l' \_ \_ État du pipeline GRAPHICs D3D12 \_ \_**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [**CD3DX12 \_ rastériseur \_ desc**](cd3dx12-rasterizer-desc.md)  
    [**CD3DX12 \_ Blend \_ desc**](cd3dx12-blend-desc.md)  
    [**ID3D12Device::CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   Créer, puis fermer, une liste de commandes : <dl>

[**ID3D12Device::CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [**ID3D12GraphicsCommandList :: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   Créez la mémoire tampon de vertex : [**ID3D12Device :: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).
-   Copiez les données de vertex dans la mémoire tampon de vertex :<dl>

[**ID3D12Resource :: Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [**ID3D12Resource :: DEMAPPAGE**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   Initialisez la vue de mémoire tampon de vertex : [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).
-   Créez et initialisez la clôture : [**ID3D12Device :: CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).
-   Créez un handle d’événement à utiliser avec la synchronisation de frames.
-   Attendez la fin du GPU.


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



### <a name="onupdate"></a>OnUpdate ()

Pour un exemple simple, rien n’est mis à jour.


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a>OnRender ()

Pendant la configuration, la variable membre **m \_ commandList** a été utilisée pour enregistrer et exécuter toutes les commandes de configuration. Vous pouvez maintenant réutiliser ce membre dans la boucle de rendu principale.

Le rendu implique un appel pour remplir la liste de commandes, puis la liste de commandes peut être exécutée et la mémoire tampon suivante dans la chaîne de permutation présentée :

-   Remplissez la liste de commandes.
-   Exécutez la commande list : [**ID3D12CommandQueue :: ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).
-   [**IDXGISwapChain1 ::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) le frame.
-   Attendez la fin de l’exécution du GPU.


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



### <a name="populatecommandlist"></a>PopulateCommandList()

Vous devez réinitialiser l’allocateur de liste de commandes et la liste de commandes elle-même avant de pouvoir les réutiliser. Dans les scénarios plus avancés, il peut être judicieux de réinitialiser l’allocateur à chaque trame. La mémoire est associée à l’allocateur qui ne peut pas être libéré immédiatement après l’exécution d’une liste de commandes. Cet exemple montre comment réinitialiser l’allocateur après chaque frame.

À présent, réutilisez la liste de commandes pour le frame actuel. Rattachez la fenêtre d’affichage à la liste de commandes (qui doit être effectuée chaque fois qu’une liste de commandes est réinitialisée, et avant l’exécution de la liste de commandes), indiquez que la ressource sera utilisée en tant que cible de rendu, enregistrer les commandes, puis indiquer que la cible de rendu sera utilisée lors de l’exécution de la liste de commandes.

Le remplissage des listes de commandes appelle à son tour les méthodes et les processus suivants :

-   Réinitialisez l’allocateur de commande et la liste des commandes : <dl>

[**ID3D12CommandAllocator :: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [**ID3D12GraphicsCommandList :: Reset**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   Définissez la signature racine, les rectangles de la fenêtre d’affichage et des ciseaux : <dl>

[**ID3D12GraphicsCommandList::SetGraphicsRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [**ID3D12GraphicsCommandList::RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [**ID3D12GraphicsCommandList::RSSetScissorRects**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   Indique que la mémoire tampon d’arrière-plan doit être utilisée comme cible de rendu : <dl>

[**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   Enregistrez les commandes :<dl>

[**ID3D12GraphicsCommandList::ClearRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [**ID3D12GraphicsCommandList::IASetPrimitiveTopology**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [**ID3D12GraphicsCommandList::IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [**ID3D12GraphicsCommandList ::D rawInstanced**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   Indiquez que la mémoire tampon d’arrière-plan sera maintenant utilisée pour présenter : [**ID3D12GraphicsCommandList :: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).
-   Fermez la liste de commandes : [**ID3D12GraphicsCommandList :: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).


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



### <a name="waitforpreviousframe"></a>WaitForPreviousFrame()

Le code suivant illustre une utilisation plus simple des délimiteurs.

> [!Note]  
> L’attente de la fin d’une trame est trop inefficace pour la plupart des applications.

 

Les API et les processus suivants sont appelés dans l’ordre :

-   [**ID3D12CommandQueue :: signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [**ID3D12Fence::GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [**ID3D12Fence::SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   Attendez l’événement.
-   Mettez à jour l’index de frame : [**IDXGISwapChain3 :: GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).


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



### <a name="ondestroy"></a>OnDestroy ()

Fermez correctement l’application.

-   Attendez la fin du GPU.
-   Fermez l’événement.


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comprendre Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Exemples fonctionnels](working-samples.md)
</dt> </dl>

 

 
