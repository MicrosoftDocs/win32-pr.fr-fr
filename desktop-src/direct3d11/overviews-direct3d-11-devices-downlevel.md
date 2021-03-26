---
title: Direct3D 11 sur du matériel de niveau inférieur
description: Cette section explique comment Direct3D 11 est conçu pour prendre en charge le matériel nouveau ou existant, de DirectX 9 à DirectX 11.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104565741"
---
# <a name="direct3d-11-on-downlevel-hardware"></a><span data-ttu-id="f4e4d-103">Direct3D 11 sur du matériel de niveau inférieur</span><span class="sxs-lookup"><span data-stu-id="f4e4d-103">Direct3D 11 on Downlevel Hardware</span></span>

<span data-ttu-id="f4e4d-104">Cette section explique comment Direct3D 11 est conçu pour prendre en charge le matériel nouveau ou existant, de DirectX 9 à DirectX 11.</span><span class="sxs-lookup"><span data-stu-id="f4e4d-104">This section discusses how Direct3D 11 is designed to support both new and existing hardware, from DirectX 9 to DirectX 11.</span></span>

<span data-ttu-id="f4e4d-105">Ce diagramme montre comment Direct3D 11 prend en charge les matériels nouveaux et existants.</span><span class="sxs-lookup"><span data-stu-id="f4e4d-105">This diagram shows how Direct3D 11 supports new and existing hardware.</span></span>

![diagramme du matériel pris en charge par Direct3D 11](images/d3d11-on-downlevel-hardware.png)

<span data-ttu-id="f4e4d-107">Avec Direct3D 11, un nouveau paradigme est présenté sous le nom des niveaux de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f4e4d-107">With Direct3D 11, a new paradigm is introduced called feature levels.</span></span> <span data-ttu-id="f4e4d-108">Un niveau de fonctionnalité est un ensemble bien défini de fonctionnalités GPU.</span><span class="sxs-lookup"><span data-stu-id="f4e4d-108">A feature level is a well defined set of GPU functionality.</span></span> <span data-ttu-id="f4e4d-109">À l’aide d’un niveau de fonctionnalité, vous pouvez cibler une application Direct3D à exécuter sur une version de niveau inférieur du matériel Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f4e4d-109">Using a feature level, you can target a Direct3D application to run on a downlevel version of Direct3D hardware.</span></span>

<span data-ttu-id="f4e4d-110">La section de [référence 10Level9](d3d11-graphics-reference-10level9.md) répertorie les différences entre la façon dont les différentes méthodes [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) et [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) se comportent à différents niveaux de fonctionnalités 10Level9.</span><span class="sxs-lookup"><span data-stu-id="f4e4d-110">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="f4e4d-111">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="f4e4d-111">In this section</span></span>



| <span data-ttu-id="f4e4d-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f4e4d-112">Topic</span></span>                                                                                                                  | <span data-ttu-id="f4e4d-113">Description</span><span class="sxs-lookup"><span data-stu-id="f4e4d-113">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4e4d-114">Niveaux de fonctionnalités Direct3D</span><span class="sxs-lookup"><span data-stu-id="f4e4d-114">Direct3D feature levels</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | <span data-ttu-id="f4e4d-115">Cette rubrique traite des niveaux de fonctionnalité Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f4e4d-115">This topic discusses Direct3D feature levels.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="f4e4d-116">Exceptions</span><span class="sxs-lookup"><span data-stu-id="f4e4d-116">Exceptions</span></span>](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | <span data-ttu-id="f4e4d-117">Cette rubrique décrit les exceptions lors de l’utilisation de Direct3D 11 sur du matériel de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="f4e4d-117">This topic describes exceptions when using Direct3D 11 on downlevel hardware.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="f4e4d-118">Nuanceurs de calcul sur du matériel de niveau inférieur</span><span class="sxs-lookup"><span data-stu-id="f4e4d-118">Compute Shaders on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | <span data-ttu-id="f4e4d-119">Cette rubrique explique comment utiliser les [nuanceurs de calcul](direct3d-11-advanced-stages-compute-shader.md) dans une application Direct3D 11 sur un matériel Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="f4e4d-119">This topic discusses how to make use of [compute shaders](direct3d-11-advanced-stages-compute-shader.md) in a Direct3D 11 app on Direct3D 10 hardware.</span></span><br/>             |
| [<span data-ttu-id="f4e4d-120">Prévention des SRVs de nuanceurs de pixels NULL indésirables</span><span class="sxs-lookup"><span data-stu-id="f4e4d-120">Preventing Unwanted NULL Pixel Shader SRVs</span></span>](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | <span data-ttu-id="f4e4d-121">Cette rubrique explique comment contourner le pilote recevant des vues de nuanceur de ressource (SRVs) **null** , même lorsque les SRVs non **null** sont liés à l’étape nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="f4e4d-121">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span><br/> |



 

## <a name="how-to-topics-about-feature-levels"></a><span data-ttu-id="f4e4d-122">Rubriques relatives aux niveaux de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="f4e4d-122">How to topics about feature levels</span></span>



| <span data-ttu-id="f4e4d-123">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f4e4d-123">Topic</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="f4e4d-124">Description</span><span class="sxs-lookup"><span data-stu-id="f4e4d-124">Description</span></span>                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="f4e4d-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Procédure : obtention du niveau de fonctionnalité de l’appareil](overviews-direct3d-11-devices-downlevel-get.md)</span><span class="sxs-lookup"><span data-stu-id="f4e4d-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[How To: Get the Device Feature Level](overviews-direct3d-11-devices-downlevel-get.md)</span></span><br/> | <span data-ttu-id="f4e4d-126">Comment obtenir un niveau de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f4e4d-126">How to get a feature level.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f4e4d-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4e4d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4e4d-128">Appareils</span><span class="sxs-lookup"><span data-stu-id="f4e4d-128">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





