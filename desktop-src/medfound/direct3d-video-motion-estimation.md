---
description: Cet article contient des conseils sur l’estimation du vecteur de mouvement avec les API vidéo Direct3D 12.
ms.assetid: ''
title: Estimation de mouvement vidéo Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 7fdb6146e1bb77c673eb89d944bcf42a8babce49
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "106538419"
---
# <a name="direct3d-video-motion-estimation"></a><span data-ttu-id="24fd7-103">Estimation de mouvement vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="24fd7-103">Direct3D video motion estimation</span></span>

<span data-ttu-id="24fd7-104">Cet article contient des conseils sur l’estimation du vecteur de mouvement avec les API vidéo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="24fd7-104">This article contains guidance for motion vector estimation with Direct3D 12 video APIs.</span></span> <span data-ttu-id="24fd7-105">Cette fonctionnalité a été introduite dans Windows 10, version 2004 (10,0 ; Build 19041).</span><span class="sxs-lookup"><span data-stu-id="24fd7-105">This feature was introduced in Windows 10, version 2004 (10.0; Build 19041).</span></span> <span data-ttu-id="24fd7-106">L’estimation de mouvement est le processus qui consiste à déterminer les vecteurs de mouvement qui décrivent la transformation d’une image 2D à une autre.</span><span class="sxs-lookup"><span data-stu-id="24fd7-106">Motion estimation is the process of determining motion vectors that describe the transformation from one 2D image to another.</span></span> <span data-ttu-id="24fd7-107">L’estimation de mouvement est un élément essentiel de l’encodage vidéo et peut être utilisée dans les algorithmes de conversion de fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="24fd7-107">Motion estimation is an essential part of video encoding and can be used in frame rate conversion algorithms.</span></span> 

<span data-ttu-id="24fd7-108">Bien que l’estimation de mouvement puisse être implémentée avec des nuanceurs, l’objectif de la fonctionnalité d’estimation de mouvement D3D12 consiste à exposer l’accélération de fonction fixe pour la recherche de mouvement afin de décharger cette partie du travail à partir de la 3D.</span><span class="sxs-lookup"><span data-stu-id="24fd7-108">While motion estimation can be implemented with shaders, the purpose of the D3D12 Motion Estimation feature is to expose fixed function acceleration for motion searching to offload this part of the work from 3D.</span></span> <span data-ttu-id="24fd7-109">Cela se produit souvent sous la forme d’une exposition de l’estimateur de mouvement de l’encodeur vidéo GPU.</span><span class="sxs-lookup"><span data-stu-id="24fd7-109">Often this comes in the form of exposing the GPU video encoder motion estimator.</span></span> <span data-ttu-id="24fd7-110">L’objectif de l’estimation de mouvement D3D12 est le circuit optique, mais il convient de noter que les estimateurs de mouvement d’encodeur peuvent être optimisés pour améliorer la compression.</span><span class="sxs-lookup"><span data-stu-id="24fd7-110">The goal of D3D12 Motion estimation is optical flow, but it should be noted that encoder motion estimators may be optimized for improving compression.</span></span>


## <a name="checking-for-support"></a><span data-ttu-id="24fd7-111">Vérification de la prise en charge</span><span class="sxs-lookup"><span data-stu-id="24fd7-111">Checking for Support</span></span>

<span data-ttu-id="24fd7-112">Déterminez la prise en charge de toutes les fonctionnalités vidéo D3D en appelant [ID3D12VideoDevice :: CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) et en passant une valeur de l’énumération [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) pour spécifier la fonctionnalité pour laquelle la prise en charge est interrogée.</span><span class="sxs-lookup"><span data-stu-id="24fd7-112">Determine support for all D3D video features by calling [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) and passing in a value from the [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify the feature for which support is being queried.</span></span> <span data-ttu-id="24fd7-113">Pour interroger la taille de bloc et les résolutions prises en charge pour un format donné, utilisez la valeur **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** et fournissez une structure [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) pour le *pFeatureSupportData* , comme indiqué dans l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="24fd7-113">To query the supported block size and resolutions for a given format, use the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** value and supply a [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) structure for the *pFeatureSupportData* as shown in the example below.</span></span> <span data-ttu-id="24fd7-114">Dans la version actuelle, seul **DXGI_FORMAT_NV12** est pris en charge. par conséquent, le contenu dans d’autres formats devra peut-être être converti et sous-échantillonné pour utiliser l’estimation de mouvement.</span><span class="sxs-lookup"><span data-stu-id="24fd7-114">In the current release, only **DXGI_FORMAT_NV12** is supported, so content in other formats may need to be color converted and downsampled to use motion estimation.</span></span>

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a><span data-ttu-id="24fd7-115">Objet de contexte de l’estimateur de mouvement</span><span class="sxs-lookup"><span data-stu-id="24fd7-115">The motion estimator context object</span></span>

<span data-ttu-id="24fd7-116">L’objet [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) conserve le contexte pour les opérations d’estimation de mouvement vidéo.</span><span class="sxs-lookup"><span data-stu-id="24fd7-116">The [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) object maintains context for video motion estimation operations.</span></span> <span data-ttu-id="24fd7-117">Créez une nouvelle instance de cette interface en appelant [ID3D12VideoDevice1 :: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span><span class="sxs-lookup"><span data-stu-id="24fd7-117">Create a new instance of this interface by calling [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span></span>

<span data-ttu-id="24fd7-118">La taille de bloc, la précision et la plage de tailles prises en charge dépendent des valeurs prises en charge par le matériel renvoyé par la vérification de la fonctionnalité de **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** .</span><span class="sxs-lookup"><span data-stu-id="24fd7-118">The selected block size, precision, and supported size range would depend on values supported by hardware returned from the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** feature check.</span></span> <span data-ttu-id="24fd7-119">Vous pouvez sélectionner une plus petite plage de taille que celle prise en charge par le pilote.</span><span class="sxs-lookup"><span data-stu-id="24fd7-119">You can select a smaller size range than the driver supports.</span></span> <span data-ttu-id="24fd7-120">La plage de tailles indique les tailles d’allocation internes.</span><span class="sxs-lookup"><span data-stu-id="24fd7-120">Size range informs internal allocation sizes.</span></span>

```c++
D3D12_VIDEO_MOTION_ESTIMATOR_DESC motionEstimatorDesc = { 
    0, //NodeIndex
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionEstimator> spVideoMotionEstimator;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionEstimator(
    &motionEstimatorDesc, 
    nullptr,
    IID_PPV_ARGS(&spVideoMotionEstimator)));
```



## <a name="storage-of-motion-vectors"></a><span data-ttu-id="24fd7-121">Stockage des vecteurs de mouvement</span><span class="sxs-lookup"><span data-stu-id="24fd7-121">Storage of motion vectors</span></span>

<span data-ttu-id="24fd7-122">[ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) stocke les vecteurs de mouvement.</span><span class="sxs-lookup"><span data-stu-id="24fd7-122">The [ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) stores motion vectors.</span></span> <span data-ttu-id="24fd7-123">Cette interface est utilisée par la structure [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) retournée à partir de [ID3D12VideoEncodeCommandList :: EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion).</span><span class="sxs-lookup"><span data-stu-id="24fd7-123">This interface is used by the [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) structure returned from [ID3D12VideoEncodeCommandList::EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion).</span></span> <span data-ttu-id="24fd7-124">La texture 2D de sortie résolue est une texture de [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) où R contient le composant horizontal et G contient le composant vertical du vecteur de mouvement.</span><span class="sxs-lookup"><span data-stu-id="24fd7-124">The resolved output 2D texture is a [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) texture where R holds the horizontal component and G holds the vertical component of the motion vector.</span></span> <span data-ttu-id="24fd7-125">Cette texture est dimensionnée de façon à contenir une paire de composants par bloc.</span><span class="sxs-lookup"><span data-stu-id="24fd7-125">This texture is sized to hold one pair of components per block.</span></span> <span data-ttu-id="24fd7-126">Appelez [ID3D12VideoEncodeCommandList :: ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) pour convertir la sortie de vecteur de mouvement de **EstimateMotion** des formats dépendants du matériel dans un format cohérent défini par les API d’estimation de mouvement vidéo.</span><span class="sxs-lookup"><span data-stu-id="24fd7-126">Call [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) to translates the motion vector output of **EstimateMotion** from hardware-dependent formats into a consistent format defined by the video motion estimation APIs.</span></span>

```c++
D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC MotionVectorHeapDesc = { 
    0, // NodeIndex 
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionVectorHeap> spVideoMotionVectorHeap;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionVectorHeap(
    &MotionVectorHeapDesc, 
    nullptr, 
    IID_PPV_ARGS(&spVideoMotionVectorHeap)));
```

```cpp
    CD3DX12_RESOURCE_DESC::Tex2D(
        DXGI_FORMAT_R16G16_SINT, 
        Align(1920, 16) / 16, // This example uses a 16x16 block size. Pixel width and height
        Align(1080, 16) / 16, // are adjusted to store the vectors for those blocks.
        1, // ArraySize
        1  // MipLevels
        );

    ATL::CComPtr< ID3D12Resource > spResolvedMotionVectors;
    VERIFY_SUCCEEDED(pDevice->CreateCommittedResource(
        &Properties,
        D3D12_HEAP_FLAG_NONE,
        &resolvedMotionVectorDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        IID_PPV_ARGS(&spResolvedMotionVectors)));
```

 <span data-ttu-id="24fd7-127">**ID3D12VideoMotionVectorHeap** est également utilisé pour fournir des vecteurs d’indication dans la structure [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) .</span><span class="sxs-lookup"><span data-stu-id="24fd7-127">**ID3D12VideoMotionVectorHeap** is also used to supply hint vectors in the [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) structure.</span></span>



## <a name="estimate-motion-in-a-command-list"></a><span data-ttu-id="24fd7-128">Estimer le mouvement dans une liste de commandes</span><span class="sxs-lookup"><span data-stu-id="24fd7-128">Estimate motion in a command list</span></span>

<span data-ttu-id="24fd7-129">Appelez [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) à partir d’un [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) pour appeler l’opération d’estimation de mouvement.</span><span class="sxs-lookup"><span data-stu-id="24fd7-129">Call the [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) from a [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) to invoke the motion estimation operation.</span></span>

<span data-ttu-id="24fd7-130">L’exemple ci-dessous exécute la recherche de mouvement et résout les vecteurs de mouvement en texture 2D avec [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span><span class="sxs-lookup"><span data-stu-id="24fd7-130">The example below executes the motion search and resolves the motion vectors to the 2D texture with [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>  <span data-ttu-id="24fd7-131">Les ressources D3D12 utilisées comme entrée pour **EstimateMotion** doivent être dans l’état [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) et la ressource écrite par **ResolveMotionVectorHeap** doit être dans l’état [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .</span><span class="sxs-lookup"><span data-stu-id="24fd7-131">D3D12 Resources used as input to **EstimateMotion** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state and the resource written to by **ResolveMotionVectorHeap** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state.</span></span>

```cpp
const D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT outputArgs = {spVideoMotionVectorHeap};

const D3D12_VIDEO_MOTION_ESTIMATOR_INPUT inputArgs = {
    spCurrentResource,
    0,
    spReferenceResource,
    0,
    nullptr // pHintMotionVectorHeap
    };

spCommandList->EstimateMotion(spVideoMotionEstimator, &outputArgs, &inputArgs);

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT outputArgs = { 
    spResolvedMotionVectors,
    {}};

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT inputArgs = {
    spVideoMotionVectorHeap,
    1920,
    1080
    };

spCommandList->ResolveMotionVectorHeap(&outputArgs, &inputArgs);
        
VERIFY(spCommandList->Close());

// Execute Commandlist.
ID3D12CommandList *ppCommandLists[1] = { spCommandList.p };
spCommandQueue->ExecuteCommandLists(1, ppCommandLists);
```


## <a name="protected-resources"></a><span data-ttu-id="24fd7-132">Ressources protégées</span><span class="sxs-lookup"><span data-stu-id="24fd7-132">Protected resources</span></span>

<span data-ttu-id="24fd7-133">L’estimation Direct3D 12 Motion Vector prend en charge la lecture et l’écriture de ressources DRM protégées matérielles lorsqu’elles sont prises en charge par le pilote.</span><span class="sxs-lookup"><span data-stu-id="24fd7-133">Direct3D 12 motion vector estimation supports reading from and writing to hardware DRM protected resources when supported by the driver.</span></span> <span data-ttu-id="24fd7-134">Si les ressources d’entrée sont protégées par DRM sur le matériel, la sortie est également une ressource protégée par DRM. Les méthodes utilisées pour créer l’objet de contexte d’estimation de mouvement et le segment de mémoire du vecteur de mouvement,  [ID3D12VideoDevice1 :: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) et [ID3D12VideoDevice1 :: CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), acceptent toutes deux un [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) qui est utilisé pour gérer l’accès aux ressources protégées.</span><span class="sxs-lookup"><span data-stu-id="24fd7-134">If the input resources are hardware DRM protected, the output is also a hardware DRM protected resource.The methods used to create the motion estimation context object and the motion vector heap,  [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) and [ID3D12VideoDevice1::CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), both accept a [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) that is used to manage access to protected resources.</span></span> 

<span data-ttu-id="24fd7-135">Utilisez [ID3D12VideoMotionEstimator :: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) et [ID3D12VideoMotionVectorHeap :: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) pour récupérer les objets **ID3D12ProtectedResourceSession** fournis lors de la création des objets.</span><span class="sxs-lookup"><span data-stu-id="24fd7-135">Use [ID3D12VideoMotionEstimator::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) and [ID3D12VideoMotionVectorHeap::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) to retrieve the **ID3D12ProtectedResourceSession** objects provided when the objects were created.</span></span>



## <a name="related-topics"></a><span data-ttu-id="24fd7-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24fd7-136">Related topics</span></span>

* [<span data-ttu-id="24fd7-137">API vidéo Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="24fd7-137">Direct3D 12 Video APIs</span></span>](direct3d-12-video-apis.md)
* [<span data-ttu-id="24fd7-138">Guide de programmation Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24fd7-138">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
