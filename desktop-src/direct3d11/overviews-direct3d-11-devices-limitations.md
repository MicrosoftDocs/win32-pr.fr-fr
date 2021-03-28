---
title: Limitations de la création d’appareils de déformation et de référence
description: Certaines limitations existent pour la création de périphériques de déformation et de référence dans Direct3D 10,1 et Direct3D 11,0. Cette rubrique présente ces limitations.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315197"
---
# <a name="limitations-creating-warp-and-reference-devices"></a><span data-ttu-id="60811-104">Limitations de la création d’appareils de déformation et de référence</span><span class="sxs-lookup"><span data-stu-id="60811-104">Limitations Creating WARP and Reference Devices</span></span>

<span data-ttu-id="60811-105">Certaines limitations existent pour la création de périphériques de déformation et de référence dans Direct3D 10,1 et Direct3D 11,0.</span><span class="sxs-lookup"><span data-stu-id="60811-105">Some limitations exist for creating WARP and Reference devices in Direct3D 10.1 and Direct3D 11.0.</span></span> <span data-ttu-id="60811-106">Cette rubrique présente ces limitations.</span><span class="sxs-lookup"><span data-stu-id="60811-106">This topic discusses those limitations.</span></span>

<span data-ttu-id="60811-107">Les types de pilote de référence de type de pilote D3D10 \_ \_ \_ Warp et D3D10 \_ \_ \_ ne sont pas pris en charge sur les \_ niveaux de fonctionnalité D3D10 Feature de \_ \_ 9 \_ 1 à D3D10 \_ Feature \_ Level \_ 9 \_ 3 dans Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="60811-107">The D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE driver types are not supported on the D3D10\_FEATURE\_LEVEL\_9\_1 through D3D10\_FEATURE\_LEVEL\_9\_3 feature levels in Direct3D 10.1.</span></span> <span data-ttu-id="60811-108">En outre, le \_ \_ type de pilote de type Warp du pilote D3D \_ n’est pas pris en charge sur le \_ niveau de fonctionnalité D3D \_ \_ 11 \_ 0 dans Direct3D 11,0.</span><span class="sxs-lookup"><span data-stu-id="60811-108">Additionally, the D3D\_DRIVER\_TYPE\_WARP driver type is not supported on D3D\_FEATURE\_LEVEL\_11\_0 in Direct3D 11.0.</span></span> <span data-ttu-id="60811-109">Autrement dit, lorsque vous appelez [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) pour créer un périphérique Direct3D 10,1 ou lorsque vous appelez [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) pour créer un appareil Direct3D 11,0, si vous spécifiez une combinaison de l’un de ces types de pilote avec l’un de ces niveaux de fonctionnalité dans l’appel, l’appel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="60811-109">That is, when you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device or when you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.0 device, if you specify a combination of one of these driver types with one of these feature levels in the call, the call is invalid.</span></span> <span data-ttu-id="60811-110">Seules les combinaisons suivantes de niveaux de fonctionnalité, runtimes et types de pilotes sont valides pour les périphériques de déviation et de référence :</span><span class="sxs-lookup"><span data-stu-id="60811-110">Only the following combinations of feature levels, runtimes, and driver types are valid for WARP and Reference devices:</span></span>

-   <span data-ttu-id="60811-111">\_ \_ Type de pilote D3D \_ Warp sur tous les niveaux de fonctionnalités dans Direct3D 11,1, inclus dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="60811-111">D3D\_DRIVER\_TYPE\_WARP on all feature levels in Direct3D 11.1, which Windows 8 includes</span></span>

    <span data-ttu-id="60811-112">\_ \_ \_ Référence du type de pilote D3D sur tous les niveaux de fonctionnalités dans Direct3D 11,1</span><span class="sxs-lookup"><span data-stu-id="60811-112">D3D\_DRIVER\_TYPE\_REFERENCE on all feature levels in Direct3D 11.1</span></span>

    <span data-ttu-id="60811-113">Quand vous appelez [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) pour créer un appareil Direct3D 11,1, l’appel est valide si vous spécifiez une combinaison de l’un de ces types de pilote avec l’un de ces niveaux de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="60811-113">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="60811-114">\_ \_ Type de pilote D3D \_ Warp sur le \_ niveau de fonctionnalité D3D \_ \_ 9 \_ 1 à \_ l’aide de fonctionnalités \_ \_ de niveau de fonctionnalité 10 \_ 1 dans Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="60811-114">D3D\_DRIVER\_TYPE\_WARP on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="60811-115">Informations \_ \_ \_ de référence sur le type de pilote D3D sur les niveaux de fonctionnalité de \_ \_ \_ 9 \_ 1 à D3D \_ de niveau de fonctionnalité \_ \_ 11 \_ 0 dans Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="60811-115">D3D\_DRIVER\_TYPE\_REFERENCE on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_11\_0 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="60811-116">Quand vous appelez [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) pour créer un appareil Direct3D 11, l’appel est valide si vous spécifiez une combinaison de l’un de ces types de pilote avec l’un de ces niveaux de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="60811-116">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="60811-117">D3D10 \_ de \_ type \_ de pilote Warp et D3D10 \_ \_ \_ référence de type de pilote sur D3D10 niveau de fonctionnalité \_ \_ \_ 10 \_ 0 à D3D10 \_ \_ \_ \_ niveaux de fonctionnalité 10 1 dans Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="60811-117">D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE on D3D10\_FEATURE\_LEVEL\_10\_0 through D3D10\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 10.1</span></span>

    <span data-ttu-id="60811-118">Quand vous appelez [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) pour créer un appareil Direct3D 10,1, l’appel est valide si vous spécifiez une combinaison de l’un de ces types de pilote avec l’un de ces niveaux de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="60811-118">When you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60811-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="60811-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60811-120">Appareils</span><span class="sxs-lookup"><span data-stu-id="60811-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="60811-121">Présentation de Direct3D 11 sur le matériel de niveau inférieur</span><span class="sxs-lookup"><span data-stu-id="60811-121">Introduction to Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[<span data-ttu-id="60811-122">Comment : créer un appareil WARP</span><span class="sxs-lookup"><span data-stu-id="60811-122">How To: Create a WARP Device</span></span>](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[<span data-ttu-id="60811-123">Comment : créer un appareil de référence</span><span class="sxs-lookup"><span data-stu-id="60811-123">How To: Create a Reference Device</span></span>](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[<span data-ttu-id="60811-124">**\_Type de pilote D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="60811-124">**D3D10\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[<span data-ttu-id="60811-125">**D3D10 \_ fonctionnalité de \_ niveau1**</span><span class="sxs-lookup"><span data-stu-id="60811-125">**D3D10\_FEATURE\_LEVEL1**</span></span>](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[<span data-ttu-id="60811-126">**\_Type de pilote D3D \_**</span><span class="sxs-lookup"><span data-stu-id="60811-126">**D3D\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[<span data-ttu-id="60811-127">**\_Niveau de fonctionnalité D3D \_**</span><span class="sxs-lookup"><span data-stu-id="60811-127">**D3D\_FEATURE\_LEVEL**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 