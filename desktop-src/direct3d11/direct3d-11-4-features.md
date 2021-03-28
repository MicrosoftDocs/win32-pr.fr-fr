---
title: Fonctionnalités Direct3D 11,4
description: Les fonctionnalités suivantes ont été ajoutées dans Direct3D 11,4.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941149"
---
# <a name="direct3d-114-features"></a><span data-ttu-id="37069-103">Fonctionnalités Direct3D 11,4</span><span class="sxs-lookup"><span data-stu-id="37069-103">Direct3D 11.4 Features</span></span>

<span data-ttu-id="37069-104">Les fonctionnalités suivantes ont été ajoutées dans Direct3D 11,4.</span><span class="sxs-lookup"><span data-stu-id="37069-104">The following functionality has been added in Direct3D 11.4.</span></span>

<span data-ttu-id="37069-105">Consultez également [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="37069-105">Also see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="direct3d-device-removal"></a><span data-ttu-id="37069-106">Suppression de l’appareil Direct3D</span><span class="sxs-lookup"><span data-stu-id="37069-106">Direct3D device removal</span></span>

<span data-ttu-id="37069-107">Les méthodes [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)et [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) sont prises en charge par une nouvelle interface, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), pour prendre en charge la réception d’une notification d’événement asynchrone lorsqu’un périphérique Direct3D a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="37069-107">The [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent), and [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) methods are supported by a new interface, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), to support receiving an asynchronous event notification when a Direct3D device has been removed.</span></span>

## <a name="multithreaded-protection"></a><span data-ttu-id="37069-108">Protection multithread</span><span class="sxs-lookup"><span data-stu-id="37069-108">Multithreaded protection</span></span>

<span data-ttu-id="37069-109">Pour vous assurer que les commandes graphiques en particulier sont exécutées dans un ordre spécifique, l’interface [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) a des méthodes permettant d’activer et de désactiver la protection multithread, ainsi que les méthodes d’entrée et de sortie du code critique nécessitant cette protection.</span><span class="sxs-lookup"><span data-stu-id="37069-109">To ensure that graphics commands in particular are executed in a specific order, the [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) interface has methods to turn multithread protection on and off, and methods to enter and leave critical code requiring this protection.</span></span>

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a><span data-ttu-id="37069-110">Clôtures pour la synchronisation de plusieurs appareils et l’interopérabilité avec Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="37069-110">Fences for multi-device synchronization and interop with Direct3D 12</span></span>

<span data-ttu-id="37069-111">[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) et [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) fournissent les mêmes fonctionnalités de barrière que Direct3D 12 pour Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="37069-111">The [**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) and [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) provide the same fence functionality as Direct3D 12 for Direct3D 11.</span></span> <span data-ttu-id="37069-112">Les délimiteurs sont utilisés pour synchroniser plusieurs appareils Direct3D11, et pour l’interopérabilité entre Direct3D 11 et Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="37069-112">Fences are used to synchronize multiple Direct3D11 devices, and for interop between Direct3D 11 and Direct3D 12.</span></span> <span data-ttu-id="37069-113">Les délimiteurs sont pris en charge dans Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="37069-113">Fences are supported in the Windows 10 Creators Update.</span></span>

## <a name="extended-nv12-texture-support"></a><span data-ttu-id="37069-114">Prise en charge étendue de la texture NV12</span><span class="sxs-lookup"><span data-stu-id="37069-114">Extended NV12 texture support</span></span>

<span data-ttu-id="37069-115">Les textures NV12 avec des fonctionnalités d’encodage vidéo et de capture prennent désormais en charge le partage.</span><span class="sxs-lookup"><span data-stu-id="37069-115">NV12 textures with capture and video encode capabilities now support sharing.</span></span> <span data-ttu-id="37069-116">Les indicateurs de texture D3D11 plus anciens pour l’encodage vidéo et la capture sont dépréciés pour NV12, car ils seront définis en permanence pour les nouveaux pilotes.</span><span class="sxs-lookup"><span data-stu-id="37069-116">Older D3D11 texture flags for video encode and capture are deprecated for NV12, as it will be set all the time for new drivers.</span></span> <span data-ttu-id="37069-117">Ces textures peuvent être partagées non seulement avec D3D11, mais également avec D3D12.</span><span class="sxs-lookup"><span data-stu-id="37069-117">Such textures can be shared not only with D3D11, but also with D3D12.</span></span> <span data-ttu-id="37069-118">Dans D3D12, aucun nouvel indicateur ne représente ces fonctionnalités de texture.</span><span class="sxs-lookup"><span data-stu-id="37069-118">In D3D12, no new flags represent these texture capabilities.</span></span>

<span data-ttu-id="37069-119">Reportez-vous au paramètre booléen dans [**d3d11 \_ Feature \_ Data \_ d3d11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span><span class="sxs-lookup"><span data-stu-id="37069-119">Refer to the boolean setting in [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span></span>

## <a name="shader-caching"></a><span data-ttu-id="37069-120">Mise en cache du nuanceur</span><span class="sxs-lookup"><span data-stu-id="37069-120">Shader Caching</span></span>

<span data-ttu-id="37069-121">Les pilotes peuvent prendre en charge la mise en cache des nuanceurs gérés par le système d’exploitation des applications Direct3D11 dans Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="37069-121">Drivers may support OS-managed shader caching of Direct3D11 applications in the Windows 10 Creators update.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37069-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="37069-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37069-123">Nouveautés de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="37069-123">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 