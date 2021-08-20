---
description: Cet article contient des conseils sur l’estimation du vecteur de mouvement avec les API vidéo Direct3D 12.
ms.assetid: ''
title: Estimation de mouvement vidéo Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 0a49f7d3ec5e68ee6151b706be65866f1e156d6f876909c99b485356fb4df21c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064116"
---
# <a name="direct3d-video-motion-estimation"></a>Estimation de mouvement vidéo Direct3D

Cet article contient des conseils sur l’estimation du vecteur de mouvement avec les API vidéo Direct3D 12. cette fonctionnalité a été introduite dans Windows 10, version 2004 (10,0 ; Build 19041). L’estimation de mouvement est le processus qui consiste à déterminer les vecteurs de mouvement qui décrivent la transformation d’une image 2D à une autre. L’estimation de mouvement est un élément essentiel de l’encodage vidéo et peut être utilisée dans les algorithmes de conversion de fréquence d’images. 

Bien que l’estimation de mouvement puisse être implémentée avec des nuanceurs, l’objectif de la fonctionnalité d’estimation de mouvement D3D12 consiste à exposer l’accélération de fonction fixe pour la recherche de mouvement afin de décharger cette partie du travail à partir de la 3D. Cela se produit souvent sous la forme d’une exposition de l’estimateur de mouvement de l’encodeur vidéo GPU. L’objectif de l’estimation de mouvement D3D12 est le circuit optique, mais il convient de noter que les estimateurs de mouvement d’encodeur peuvent être optimisés pour améliorer la compression.


## <a name="checking-for-support"></a>Vérification de la prise en charge

Déterminez la prise en charge de toutes les fonctionnalités vidéo D3D en appelant [ID3D12VideoDevice :: CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) et en passant une valeur de l’énumération [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) pour spécifier la fonctionnalité pour laquelle la prise en charge est interrogée. Pour interroger la taille de bloc et les résolutions prises en charge pour un format donné, utilisez la valeur **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** et fournissez une structure [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) pour le *pFeatureSupportData* , comme indiqué dans l’exemple ci-dessous. Dans la version actuelle, seul **DXGI_FORMAT_NV12** est pris en charge. par conséquent, le contenu dans d’autres formats devra peut-être être converti et sous-échantillonné pour utiliser l’estimation de mouvement.

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a>Objet de contexte de l’estimateur de mouvement

L’objet [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) conserve le contexte pour les opérations d’estimation de mouvement vidéo. Créez une nouvelle instance de cette interface en appelant [ID3D12VideoDevice1 :: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).

La taille de bloc, la précision et la plage de tailles prises en charge dépendent des valeurs prises en charge par le matériel renvoyé par la vérification de la fonctionnalité de **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** . Vous pouvez sélectionner une plus petite plage de taille que celle prise en charge par le pilote. La plage de tailles indique les tailles d’allocation internes.

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



## <a name="storage-of-motion-vectors"></a>Stockage de vecteurs de mouvement

[ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) stocke les vecteurs de mouvement. Cette interface est utilisée par la structure [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) retournée à partir de [ID3D12VideoEncodeCommandList :: EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion). La texture 2D de sortie résolue est une texture de [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) où R contient le composant horizontal et G contient le composant vertical du vecteur de mouvement. Cette texture est dimensionnée de façon à contenir une paire de composants par bloc. Appelez [ID3D12VideoEncodeCommandList :: ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) pour convertir la sortie de vecteur de mouvement de **EstimateMotion** des formats dépendants du matériel dans un format cohérent défini par les API d’estimation de mouvement vidéo.

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

 **ID3D12VideoMotionVectorHeap** est également utilisé pour fournir des vecteurs d’indication dans la structure [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) .



## <a name="estimate-motion-in-a-command-list"></a>Estimer le mouvement dans une liste de commandes

Appelez [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) à partir d’un [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) pour appeler l’opération d’estimation de mouvement.

L’exemple ci-dessous exécute la recherche de mouvement et résout les vecteurs de mouvement en texture 2D avec [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).  Les ressources D3D12 utilisées comme entrée pour **EstimateMotion** doivent être dans l’état [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) et la ressource écrite par **ResolveMotionVectorHeap** doit être dans l’état [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .

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


## <a name="protected-resources"></a>Ressources protégées

L’estimation Direct3D 12 Motion Vector prend en charge la lecture et l’écriture de ressources DRM protégées matérielles lorsqu’elles sont prises en charge par le pilote. Si les ressources d’entrée sont protégées par DRM sur le matériel, la sortie est également une ressource protégée par DRM. Les méthodes utilisées pour créer l’objet de contexte d’estimation de mouvement et le segment de mémoire du vecteur de mouvement,  [ID3D12VideoDevice1 :: CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) et [ID3D12VideoDevice1 :: CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), acceptent toutes deux un [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) qui est utilisé pour gérer l’accès aux ressources protégées. 

Utilisez [ID3D12VideoMotionEstimator :: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) et [ID3D12VideoMotionVectorHeap :: GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) pour récupérer les objets **ID3D12ProtectedResourceSession** fournis lors de la création des objets.



## <a name="related-topics"></a>Rubriques connexes

* [API vidéo Direct3D 12](direct3d-12-video-apis.md)
* [Guide de programmation Media Foundation](media-foundation-programming-guide.md)
