---
description: Définit les niveaux d’échantillonnage multiple de la scène complète que l’appareil peut appliquer.
ms.assetid: 1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8
title: Énumération D3DMULTISAMPLE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMULTISAMPLE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: da8f9c1c8bb3aa74c0ab22a5cc701e7d835898de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323002"
---
# <a name="d3dmultisample_type-enumeration"></a><span data-ttu-id="633fa-103">\_Énumération de type D3DMULTISAMPLE</span><span class="sxs-lookup"><span data-stu-id="633fa-103">D3DMULTISAMPLE\_TYPE enumeration</span></span>

<span data-ttu-id="633fa-104">Définit les niveaux d’échantillonnage multiple de la scène complète que l’appareil peut appliquer.</span><span class="sxs-lookup"><span data-stu-id="633fa-104">Defines the levels of full-scene multisampling that the device can apply.</span></span>

## <a name="syntax"></a><span data-ttu-id="633fa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="633fa-105">Syntax</span></span>


```C++
typedef enum D3DMULTISAMPLE_TYPE { 
  D3DMULTISAMPLE_NONE          = 0,
  D3DMULTISAMPLE_NONMASKABLE   = 1,
  D3DMULTISAMPLE_2_SAMPLES     = 2,
  D3DMULTISAMPLE_3_SAMPLES     = 3,
  D3DMULTISAMPLE_4_SAMPLES     = 4,
  D3DMULTISAMPLE_5_SAMPLES     = 5,
  D3DMULTISAMPLE_6_SAMPLES     = 6,
  D3DMULTISAMPLE_7_SAMPLES     = 7,
  D3DMULTISAMPLE_8_SAMPLES     = 8,
  D3DMULTISAMPLE_9_SAMPLES     = 9,
  D3DMULTISAMPLE_10_SAMPLES    = 10,
  D3DMULTISAMPLE_11_SAMPLES    = 11,
  D3DMULTISAMPLE_12_SAMPLES    = 12,
  D3DMULTISAMPLE_13_SAMPLES    = 13,
  D3DMULTISAMPLE_14_SAMPLES    = 14,
  D3DMULTISAMPLE_15_SAMPLES    = 15,
  D3DMULTISAMPLE_16_SAMPLES    = 16,
  D3DMULTISAMPLE_FORCE_DWORD   = 0xffffffff
} D3DMULTISAMPLE_TYPE, *LPD3DMULTISAMPLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="633fa-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="633fa-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="633fa-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="633fa-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-108">Aucun niveau d’échantillonnage multiple de la scène complète n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-108">No level of full-scene multisampling is available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE non \_ masquable**</span><span class="sxs-lookup"><span data-stu-id="633fa-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE\_NONMASKABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="633fa-110">Active la valeur de la qualité d’échantillonnage multiples.</span><span class="sxs-lookup"><span data-stu-id="633fa-110">Enables the multisample quality value.</span></span> <span data-ttu-id="633fa-111">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="633fa-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**\_Exemples D3DMULTISAMPLE 2 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**D3DMULTISAMPLE\_2\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-113">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-113">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**\_Exemples D3DMULTISAMPLE 3 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**D3DMULTISAMPLE\_3\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-115">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-115">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**\_Exemples D3DMULTISAMPLE 4 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**D3DMULTISAMPLE\_4\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-117">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-117">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**\_Exemples D3DMULTISAMPLE 5 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**D3DMULTISAMPLE\_5\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-119">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-119">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**\_Exemples D3DMULTISAMPLE 6 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**D3DMULTISAMPLE\_6\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-121">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-121">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**\_Exemples D3DMULTISAMPLE 7 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**D3DMULTISAMPLE\_7\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-123">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-123">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**\_Exemples D3DMULTISAMPLE 8 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**D3DMULTISAMPLE\_8\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-125">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-125">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**\_Exemples D3DMULTISAMPLE 9 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**D3DMULTISAMPLE\_9\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-127">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-127">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**\_Exemples D3DMULTISAMPLE 10 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**D3DMULTISAMPLE\_10\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-129">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-129">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**\_Exemples D3DMULTISAMPLE 11 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**D3DMULTISAMPLE\_11\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-131">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-131">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**\_Exemples D3DMULTISAMPLE 12 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**D3DMULTISAMPLE\_12\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-133">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-133">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**\_Exemples D3DMULTISAMPLE 13 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**D3DMULTISAMPLE\_13\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-135">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-135">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**\_Exemples D3DMULTISAMPLE 14 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**D3DMULTISAMPLE\_14\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-137">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-137">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**\_Exemples D3DMULTISAMPLE 15 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE\_15\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-139">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-139">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**\_Exemples D3DMULTISAMPLE 16 \_**</span><span class="sxs-lookup"><span data-stu-id="633fa-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**D3DMULTISAMPLE\_16\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-141">Niveau d’échantillonnage multiple de scène intégrale disponible.</span><span class="sxs-lookup"><span data-stu-id="633fa-141">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="633fa-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="633fa-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="633fa-143">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="633fa-143">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="633fa-144">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="633fa-144">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="633fa-145">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="633fa-145">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="633fa-146">Notes</span><span class="sxs-lookup"><span data-stu-id="633fa-146">Remarks</span></span>

<span data-ttu-id="633fa-147">En plus de l’activation de l’échantillonnage multiple de scène complète à [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) Time, des États de rendu transforment différents aspects en fonction des niveaux affinés.</span><span class="sxs-lookup"><span data-stu-id="633fa-147">In addition to enabling full-scene multisampling at [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) time, there will be render states that turn various aspects on and off at fine-grained levels.</span></span>

<span data-ttu-id="633fa-148">L’échantillonnage multiple est valide uniquement sur une chaîne de permutation en cours de création ou de réinitialisation à l’aide de l' \_ effet D3DSWAPEFFECT ignorer l’échange.</span><span class="sxs-lookup"><span data-stu-id="633fa-148">Multisampling is valid only on a swap chain that is being created or reset with the D3DSWAPEFFECT\_DISCARD swap effect.</span></span>

<span data-ttu-id="633fa-149">La valeur d’anticrénelage sur plusieurs échantillons peut être définie avec les paramètres (ou sous-paramètres) dans les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="633fa-149">The multisample antialiasing value can be set with the parameters (or sub-parameters) in the following methods.</span></span>



| <span data-ttu-id="633fa-150">Méthode</span><span class="sxs-lookup"><span data-stu-id="633fa-150">Method</span></span>                                                                                             | <span data-ttu-id="633fa-151">Paramètres</span><span class="sxs-lookup"><span data-stu-id="633fa-151">Parameters</span></span>                         | <span data-ttu-id="633fa-152">Sous-paramètres</span><span class="sxs-lookup"><span data-stu-id="633fa-152">Sub-parameters</span></span>                     |
|----------------------------------------------------------------------------------------------------|------------------------------------|------------------------------------|
| [<span data-ttu-id="633fa-153">**IDirect3D9::CheckDeviceMultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="633fa-153">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)           | <span data-ttu-id="633fa-154">MultiSampleType et pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="633fa-154">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="633fa-155">**IDirect3D9::CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="633fa-155">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)                                       | <span data-ttu-id="633fa-156">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="633fa-156">pPresentationParameters</span></span>            | <span data-ttu-id="633fa-157">MultiSampleType et pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="633fa-157">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="633fa-158">**IDirect3DDevice9::CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="633fa-158">**IDirect3DDevice9::CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) | <span data-ttu-id="633fa-159">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="633fa-159">pPresentationParameters</span></span>            | <span data-ttu-id="633fa-160">MultiSampleType et pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="633fa-160">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="633fa-161">**IDirect3DDevice9::CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="633fa-161">**IDirect3DDevice9::CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) | <span data-ttu-id="633fa-162">MultiSampleType et pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="633fa-162">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="633fa-163">**IDirect3DDevice9::CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="633fa-163">**IDirect3DDevice9::CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)               | <span data-ttu-id="633fa-164">MultiSampleType et pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="633fa-164">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="633fa-165">**IDirect3DDevice9 :: Reset**</span><span class="sxs-lookup"><span data-stu-id="633fa-165">**IDirect3DDevice9::Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)                                         | <span data-ttu-id="633fa-166">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="633fa-166">pPresentationParameters</span></span>            | <span data-ttu-id="633fa-167">MultiSampleType et pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="633fa-167">MultiSampleType and pQualityLevels</span></span> |



 

<span data-ttu-id="633fa-168">Il n’est pas recommandé de passer d’un type à plusieurs échantillons à un autre pour augmenter la qualité de l’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="633fa-168">It is not good practice to switch from one multisample type to another to raise the quality of the antialiasing.</span></span>

<span data-ttu-id="633fa-169">D3DMULTISAMPLE \_ None active les effets d’échange autres que l’abandon, le verrouillage, etc.</span><span class="sxs-lookup"><span data-stu-id="633fa-169">D3DMULTISAMPLE\_NONE enables swap effects other than discarding, locking, and so on.</span></span>

<span data-ttu-id="633fa-170">Si le périphérique d’affichage prend en charge l’échantillonnage multiple masquable (plusieurs exemples pour un format de cible de rendu à plusieurs échantillons et la prise en charge de l’anticrénelage) ou simplement un échantillonnage non masquable (uniquement la prise en charge de l’anticrénelage), le pilote de l’appareil fournit le nombre de niveaux de qualité pour le \_ type d’échantillon multiple non masquable D3DMULTISAMPLE.</span><span class="sxs-lookup"><span data-stu-id="633fa-170">Whether the display device supports maskable multisampling (more than one sample for a multiple-sample render-target format plus antialias support) or just non-maskable multisampling (only antialias support), the driver for the device provides the number of quality levels for the D3DMULTISAMPLE\_NONMASKABLE multiple-sample type.</span></span> <span data-ttu-id="633fa-171">Les applications qui utilisent simplement plusieurs échantillonnages à des fins d’anticrénelage ont uniquement besoin d’interroger le nombre de niveaux de qualité à plusieurs exemples non masquables que le pilote prend en charge.</span><span class="sxs-lookup"><span data-stu-id="633fa-171">Applications that just use multisampling for antialiasing purposes only need to query for the number of non-maskable multiple-sample quality levels that the driver supports.</span></span>

<span data-ttu-id="633fa-172">Les niveaux de qualité pris en charge par l’appareil peuvent être obtenus à l’aide du paramètre pQualityLevels de [**IDirect3D9 :: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span><span class="sxs-lookup"><span data-stu-id="633fa-172">The quality levels supported by the device can be obtained with the pQualityLevels parameter of [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="633fa-173">Les niveaux de qualité utilisés par l’application sont définis avec le paramètre MultiSampleQuality de [**IDirect3DDevice9 :: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) et [**IDirect3DDevice9 :: CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span><span class="sxs-lookup"><span data-stu-id="633fa-173">Quality levels used by the application are set with the MultiSampleQuality parameter of [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) and [**IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span></span>

<span data-ttu-id="633fa-174">Pour plus \_ d’informations sur l’échantillonnage masquable, consultez D3DRS MULTISAMPLEMASK.</span><span class="sxs-lookup"><span data-stu-id="633fa-174">See D3DRS\_MULTISAMPLEMASK for discussion of maskable multisampling.</span></span>

## <a name="requirements"></a><span data-ttu-id="633fa-175">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="633fa-175">Requirements</span></span>



| <span data-ttu-id="633fa-176">Condition requise</span><span class="sxs-lookup"><span data-stu-id="633fa-176">Requirement</span></span> | <span data-ttu-id="633fa-177">Valeur</span><span class="sxs-lookup"><span data-stu-id="633fa-177">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="633fa-178">En-tête</span><span class="sxs-lookup"><span data-stu-id="633fa-178">Header</span></span><br/> | <dl> <span data-ttu-id="633fa-179"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="633fa-179"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="633fa-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="633fa-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633fa-181">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="633fa-181">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="633fa-182">**\_Paramètres D3DPRESENT**</span><span class="sxs-lookup"><span data-stu-id="633fa-182">**D3DPRESENT\_PARAMETERS**</span></span>](d3dpresent-parameters.md)
</dt> <dt>

[<span data-ttu-id="633fa-183">**D3DSURFACE \_ desc**</span><span class="sxs-lookup"><span data-stu-id="633fa-183">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> </dl>

 

 
