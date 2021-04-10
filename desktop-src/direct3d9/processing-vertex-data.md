---
description: L’interface IDirect3DDevice9 prend en charge le traitement des vertex dans les logiciels et le matériel.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Traitement des données de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846590"
---
# <a name="processing-vertex-data-direct3d-9"></a><span data-ttu-id="9cbb8-103">Traitement des données de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9cbb8-103">Processing Vertex Data (Direct3D 9)</span></span>

<span data-ttu-id="9cbb8-104">L’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) prend en charge le traitement des vertex dans les logiciels et le matériel.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-104">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface supports vertex processing in both software and hardware.</span></span> <span data-ttu-id="9cbb8-105">En général, les fonctionnalités de l’appareil pour le traitement des vertex logiciels et matériels ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-105">In general, the device capabilities for software and hardware vertex processing are not identical.</span></span> <span data-ttu-id="9cbb8-106">Les fonctionnalités matérielles sont variables, en fonction de l’adaptateur d’affichage et du pilote, tandis que les fonctionnalités logicielles sont fixes.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-106">Hardware capabilities are variable, depending on the display adapter and driver, while software capabilities are fixed.</span></span>

<span data-ttu-id="9cbb8-107">Les indicateurs suivants contrôlent le comportement de traitement des vertex pour la couche d’abstraction matérielle (HAL) et les périphériques de référence.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-107">The following flags control vertex processing behavior for the hardware abstraction layer (HAL) and reference devices.</span></span>

-   <span data-ttu-id="9cbb8-108">D3DCREATE \_ logiciel \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="9cbb8-108">D3DCREATE\_SOFTWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="9cbb8-109">\_Matériel D3DCREATE \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="9cbb8-109">D3DCREATE\_HARDWARE\_VERTEXPROCESSING</span></span>
-   <span data-ttu-id="9cbb8-110">D3DCREATE \_ mixte \_ VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="9cbb8-110">D3DCREATE\_MIXED\_VERTEXPROCESSING</span></span>

<span data-ttu-id="9cbb8-111">Spécifiez l’un des indicateurs de comportement de traitement des vertex lors de l’appel de [**IDirect3D9 :: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span><span class="sxs-lookup"><span data-stu-id="9cbb8-111">Specify one of the vertex processing behavior flags when calling [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span> <span data-ttu-id="9cbb8-112">L’indicateur en mode mixte permet à l’appareil d’effectuer le traitement des vertex logiciels et matériels.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-112">The mixed-mode flag enables the device to perform both software and hardware vertex processing.</span></span> <span data-ttu-id="9cbb8-113">Un seul indicateur de traitement de vertex peut être défini pour un appareil à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-113">Only one vertex processing flag may be set for a device at any one time.</span></span> <span data-ttu-id="9cbb8-114">Notez que l' \_ indicateur VERTEXPROCESSING Hardware D3DCREATE doit \_ être défini lors de la création d’un appareil pur (D3DCREATE \_ PUREDEVICE).</span><span class="sxs-lookup"><span data-stu-id="9cbb8-114">Note that the D3DCREATE\_HARDWARE\_VERTEXPROCESSING flag is required to be set when creating a pure device (D3DCREATE\_PUREDEVICE).</span></span>

<span data-ttu-id="9cbb8-115">Pour éviter les capacités de traitement double des vertex sur un seul appareil, seules les capacités de traitement du vertex matériel peuvent être interrogées au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-115">To avoid dual vertex processing capabilities on a single device, only the hardware vertex processing capabilities can be queried at run time.</span></span> <span data-ttu-id="9cbb8-116">Les fonctionnalités de traitement des vertex logiciels sont fixes et ne peuvent pas être interrogées au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-116">Software vertex processing capabilities are fixed and cannot be queried at run time.</span></span>

<span data-ttu-id="9cbb8-117">Le membre VertexProcessingCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) détermine les capacités de traitement du vertex matériel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-117">The VertexProcessingCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure determines the hardware vertex processing capabilities of the device.</span></span>

<span data-ttu-id="9cbb8-118">Pour le traitement des vertex logiciels, les fonctionnalités suivantes sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-118">For software vertex processing the following capabilities are supported.</span></span>

-   <span data-ttu-id="9cbb8-119">membre D3DVTXPCAPS \_ DIRECTIONALLIGHTS de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="9cbb8-119">the D3DVTXPCAPS\_DIRECTIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="9cbb8-120">membre D3DVTXPCAPS \_ LOCALVIEWER de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="9cbb8-120">the D3DVTXPCAPS\_LOCALVIEWER member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="9cbb8-121">membre D3DVTXPCAPS \_ MATERIALSOURCE7 de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="9cbb8-121">the D3DVTXPCAPS\_MATERIALSOURCE7 member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="9cbb8-122">membre D3DVTXPCAPS \_ POSITIONALLIGHTS de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="9cbb8-122">the D3DVTXPCAPS\_POSITIONALLIGHTS member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="9cbb8-123">membre D3DVTXPCAPS \_ TEXGEN de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="9cbb8-123">the D3DVTXPCAPS\_TEXGEN member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>
-   <span data-ttu-id="9cbb8-124">\_membre d’interpolation D3DVTXPCAPS de [D3DVTXPCAPS](d3dvtxpcaps.md)</span><span class="sxs-lookup"><span data-stu-id="9cbb8-124">the D3DVTXPCAPS\_TWEENING member of [D3DVTXPCAPS](d3dvtxpcaps.md)</span></span>

<span data-ttu-id="9cbb8-125">En outre, le tableau suivant répertorie les valeurs qui sont définies pour les membres de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour un appareil en mode de traitement de vertex logiciel.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-125">In addition, the following table lists the values that are set for members of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for a device in software vertex processing mode.</span></span>



| <span data-ttu-id="9cbb8-126">Membre</span><span class="sxs-lookup"><span data-stu-id="9cbb8-126">Member</span></span>                 | <span data-ttu-id="9cbb8-127">Fonctionnalités de traitement des vertex logiciels</span><span class="sxs-lookup"><span data-stu-id="9cbb8-127">Software vertex processing capabilities</span></span> |
|------------------------|-----------------------------------------|
| <span data-ttu-id="9cbb8-128">MaxActiveLights</span><span class="sxs-lookup"><span data-stu-id="9cbb8-128">MaxActiveLights</span></span>        | <span data-ttu-id="9cbb8-129">Illimité</span><span class="sxs-lookup"><span data-stu-id="9cbb8-129">Unlimited</span></span>                               |
| <span data-ttu-id="9cbb8-130">MaxUserClipPlanes</span><span class="sxs-lookup"><span data-stu-id="9cbb8-130">MaxUserClipPlanes</span></span>      | <span data-ttu-id="9cbb8-131">6</span><span class="sxs-lookup"><span data-stu-id="9cbb8-131">6</span></span>                                       |
| <span data-ttu-id="9cbb8-132">MaxVertexBlendMatrices</span><span class="sxs-lookup"><span data-stu-id="9cbb8-132">MaxVertexBlendMatrices</span></span> | <span data-ttu-id="9cbb8-133">4</span><span class="sxs-lookup"><span data-stu-id="9cbb8-133">4</span></span>                                       |
| <span data-ttu-id="9cbb8-134">MaxStreams</span><span class="sxs-lookup"><span data-stu-id="9cbb8-134">MaxStreams</span></span>             | <span data-ttu-id="9cbb8-135">16</span><span class="sxs-lookup"><span data-stu-id="9cbb8-135">16</span></span>                                      |
| <span data-ttu-id="9cbb8-136">MaxVertexIndex</span><span class="sxs-lookup"><span data-stu-id="9cbb8-136">MaxVertexIndex</span></span>         | <span data-ttu-id="9cbb8-137">Égale</span><span class="sxs-lookup"><span data-stu-id="9cbb8-137">0xFFFFFFFF</span></span>                              |



 

<span data-ttu-id="9cbb8-138">En général, toute application qui est liée au traitement des vertex doit utiliser un appareil HAL.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-138">In general, any application that is vertex processing bound should use a HAL device.</span></span> <span data-ttu-id="9cbb8-139">Le traitement des vertex logiciels fournit un ensemble garanti de fonctionnalités de traitement des vertex, y compris un nombre illimité d’éclairages et une prise en charge complète des nuanceurs de vertex programmables.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-139">Software vertex processing provides a guaranteed set of vertex processing capabilities, including an unbounded number of lights and full support for programmable vertex shaders.</span></span> <span data-ttu-id="9cbb8-140">Vous pouvez basculer entre le traitement des vertex logiciels et matériels à tout moment lors de l’utilisation de l’appareil HAL (qui est le seul type d’appareil prenant en charge le traitement du vertex matériel et logiciel).</span><span class="sxs-lookup"><span data-stu-id="9cbb8-140">You can toggle between software and hardware vertex processing at any time when using the HAL device (which is the only device type that supports both hardware and software vertex processing).</span></span> <span data-ttu-id="9cbb8-141">La seule exigence est que les mémoires tampons de vertex utilisées pour le traitement du vertex logiciel doivent être allouées dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="9cbb8-141">The only requirement is that vertex buffers used for software vertex processing must be allocated in system memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cbb8-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9cbb8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cbb8-143">Périphériques Direct3D</span><span class="sxs-lookup"><span data-stu-id="9cbb8-143">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
