---
description: Consultez la liste des indicateurs de capacité du pilote. Comprend les définitions, les valeurs et les descriptions avec des liens vers des API.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f209e840450b834c3a69593d1297f2cba9ee43c0
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343374"
---
# <a name="d3dcaps2"></a><span data-ttu-id="9bdcb-104">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="9bdcb-104">D3DCAPS2</span></span>

<span data-ttu-id="9bdcb-105">Indicateurs de capacité du pilote.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9bdcb-106">#définition</span><span class="sxs-lookup"><span data-stu-id="9bdcb-106">#define</span></span></td>
<td><span data-ttu-id="9bdcb-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bdcb-107">Value</span></span></td>
<td><span data-ttu-id="9bdcb-108">Description</span><span class="sxs-lookup"><span data-stu-id="9bdcb-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bdcb-109">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="9bdcb-109">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="9bdcb-110">0x40000000L</span><span class="sxs-lookup"><span data-stu-id="9bdcb-110">0x40000000L</span></span></td>
<td><span data-ttu-id="9bdcb-111">Le pilote est en capacité de générer automatiquement des des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-111">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="9bdcb-112">Pour plus d’informations, consultez <a href="automatic-generation-of-mipmaps.md">génération automatique de des mipmaps (Direct3D 9)</a>.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-112">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9bdcb-113">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="9bdcb-113">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="9bdcb-114">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="9bdcb-114">0x00100000L</span></span></td>
<td><span data-ttu-id="9bdcb-115">Un étalonnage est installé sur le système et peut ajuster automatiquement la rampe gamma afin que le résultat soit identique sur tous les systèmes ayant un étalonnage.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-115">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="9bdcb-116">Pour appeler le étalonnage lors de la définition de nouveaux niveaux gamma, utilisez l’indicateur D3DSGR_CALIBRATE lors de l’appel de <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-116">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="9bdcb-117">L’étalonnage des rampes gamma entraîne une surcharge de traitement et ne doit pas être utilisé fréquemment.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-117">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bdcb-118">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="9bdcb-118">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="9bdcb-119">0x80000000L</span><span class="sxs-lookup"><span data-stu-id="9bdcb-119">0x80000000L</span></span></td>
<td><span data-ttu-id="9bdcb-120">L’appareil peut créer des ressources partageables.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-120">The device can create sharable resources.</span></span> <span data-ttu-id="9bdcb-121">Les méthodes qui créent des ressources peuvent définir des valeurs non NULL pour leurs paramètres <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9bdcb-121">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9bdcb-122">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="9bdcb-122">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="9bdcb-123">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-123">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9bdcb-124">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="9bdcb-124">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="9bdcb-125">0x10000000L</span><span class="sxs-lookup"><span data-stu-id="9bdcb-125">0x10000000L</span></span></td>
<td><span data-ttu-id="9bdcb-126">Le pilote est en charge de la gestion des ressources.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-126">The driver is capable of managing resources.</span></span> <span data-ttu-id="9bdcb-127">Sur ces pilotes, les ressources de D3DPOOL_MANAGED seront gérées par le pilote.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-127">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="9bdcb-128">Pour que Direct3D remplace le pilote afin que Direct3D gère les ressources, utilisez l’indicateur D3DCREATE_DISABLE_DRIVER_MANAGEMENT lors de l’appel de <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-128">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bdcb-129">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="9bdcb-129">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="9bdcb-130">0x20000000L</span><span class="sxs-lookup"><span data-stu-id="9bdcb-130">0x20000000L</span></span></td>
<td><span data-ttu-id="9bdcb-131">Le pilote prend en charge les textures dynamiques.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-131">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9bdcb-132">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="9bdcb-132">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="9bdcb-133">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="9bdcb-133">0x00020000L</span></span></td>
<td><span data-ttu-id="9bdcb-134">Le pilote prend en charge l’ajustement dynamique de la rampe gamma en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-134">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9bdcb-135">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="9bdcb-135">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="9bdcb-136">0x02000000L</span><span class="sxs-lookup"><span data-stu-id="9bdcb-136">0x02000000L</span></span></td>
<td><span data-ttu-id="9bdcb-137">Réservé non utilisé.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9bdcb-138">Ces constantes sont utilisées par le membre D3CAPS2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="9bdcb-138">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="9bdcb-139">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="9bdcb-139">Constant Information</span></span>



|  <span data-ttu-id="9bdcb-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9bdcb-140">Requirement</span></span>                        | <span data-ttu-id="9bdcb-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bdcb-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="9bdcb-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="9bdcb-142">Header</span></span>                   | <span data-ttu-id="9bdcb-143">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="9bdcb-143">d3d9caps.h</span></span> |
| <span data-ttu-id="9bdcb-144">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="9bdcb-144">Minimum operating system</span></span> | <span data-ttu-id="9bdcb-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9bdcb-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9bdcb-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bdcb-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bdcb-147">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="9bdcb-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
