---
description: Définit la classe de mémoire qui contient les mémoires tampons d’une ressource.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: Énumération D3DPOOL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535821"
---
# <a name="d3dpool-enumeration"></a><span data-ttu-id="dbacb-103">Énumération D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="dbacb-103">D3DPOOL enumeration</span></span>

<span data-ttu-id="dbacb-104">Définit la classe de mémoire qui contient les mémoires tampons d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="dbacb-104">Defines the memory class that holds the buffers for a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbacb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbacb-105">Syntax</span></span>


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a><span data-ttu-id="dbacb-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="dbacb-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dbacb-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="dbacb-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="dbacb-108">Les ressources sont placées dans le pool de mémoire le plus approprié pour l’ensemble des utilisations demandées pour la ressource donnée.</span><span class="sxs-lookup"><span data-stu-id="dbacb-108">Resources are placed in the memory pool most appropriate for the set of usages requested for the given resource.</span></span> <span data-ttu-id="dbacb-109">Il s’agit généralement de la mémoire vidéo, y compris la mémoire vidéo locale et la mémoire AGP.</span><span class="sxs-lookup"><span data-stu-id="dbacb-109">This is usually video memory, including both local video memory and AGP memory.</span></span> <span data-ttu-id="dbacb-110">Le \_ pool par défaut D3DPOOL est distinct de D3DPOOL \_ géré et D3DPOOL \_ SYSTEMMEM, et il spécifie que la ressource est placée dans la mémoire par défaut pour l’accès à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dbacb-110">The D3DPOOL\_DEFAULT pool is separate from D3DPOOL\_MANAGED and D3DPOOL\_SYSTEMMEM, and it specifies that the resource is placed in the preferred memory for device access.</span></span> <span data-ttu-id="dbacb-111">Notez que D3DPOOL \_ default n’indique jamais que D3DPOOL \_ géré ou D3DPOOL \_ SYSTEMMEM doit être choisi comme type de pool de mémoire pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="dbacb-111">Note that D3DPOOL\_DEFAULT never indicates that either D3DPOOL\_MANAGED or D3DPOOL\_SYSTEMMEM should be chosen as the memory pool type for this resource.</span></span> <span data-ttu-id="dbacb-112">Les textures placées dans le \_ pool par défaut D3DPOOL ne peuvent pas être verrouillées, sauf s’il s’agit de textures dynamiques ou de formats privés, FourCC et de pilote.</span><span class="sxs-lookup"><span data-stu-id="dbacb-112">Textures placed in the D3DPOOL\_DEFAULT pool cannot be locked unless they are dynamic textures or they are private, FOURCC, driver formats.</span></span> <span data-ttu-id="dbacb-113">Pour accéder aux textures qui ne sont pas verrouillées, vous devez utiliser des fonctions telles que [**IDirect3DDevice9 :: UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9 :: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9 :: GetFrontBufferData**](/windows/desktop/api)et [**IDirect3DDevice9 :: GetRenderTargetData**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="dbacb-113">To access unlockable textures, you must use functions such as [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9::GetFrontBufferData**](/windows/desktop/api), and [**IDirect3DDevice9::GetRenderTargetData**](/windows/desktop/api).</span></span> <span data-ttu-id="dbacb-114">D3DPOOL \_ Managed est probablement un meilleur choix que D3DPOOL \_ Default pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="dbacb-114">D3DPOOL\_MANAGED is probably a better choice than D3DPOOL\_DEFAULT for most applications.</span></span> <span data-ttu-id="dbacb-115">Notez que certaines textures créées dans un format de pixel propriétaire du pilote, inconnues du runtime Direct3D, peuvent être verrouillées.</span><span class="sxs-lookup"><span data-stu-id="dbacb-115">Note that some textures created in driver-proprietary pixel formats, unknown to the Direct3D runtime, can be locked.</span></span> <span data-ttu-id="dbacb-116">Notez également que, à la différence des textures, les mémoires tampons d’arrière-plan, les cibles de rendu, les mémoires tampons de vertex et les mémoires tampons d’index peuvent être verrouillées.</span><span class="sxs-lookup"><span data-stu-id="dbacb-116">Also note that - unlike textures - swap chain back buffers, render targets, vertex buffers, and index buffers can be locked.</span></span> <span data-ttu-id="dbacb-117">Quand un appareil est perdu, les ressources créées à l’aide de D3DPOOL \_ par défaut doivent être libérées avant d’appeler [**IDirect3DDevice9 :: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="dbacb-117">When a device is lost, resources created using D3DPOOL\_DEFAULT must be released before calling [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="dbacb-118">Pour plus d’informations, consultez [appareils perdus (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="dbacb-118">For more information, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="dbacb-119">Lors de la création de ressources avec D3DPOOL \_ par défaut, si la mémoire de carte vidéo est déjà validée, les ressources managées sont supprimées pour libérer suffisamment de mémoire pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="dbacb-119">When creating resources with D3DPOOL\_DEFAULT, if video card memory is already committed, managed resources will be evicted to free enough memory to satisfy the request.</span></span>

</dd> <dt>

<span data-ttu-id="dbacb-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**Géré par D3DPOOL \_**</span><span class="sxs-lookup"><span data-stu-id="dbacb-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="dbacb-121">Les ressources sont automatiquement copiées dans la mémoire accessible par l’appareil en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="dbacb-121">Resources are copied automatically to device-accessible memory as needed.</span></span> <span data-ttu-id="dbacb-122">Les ressources managées sont sauvegardées par la mémoire système et n’ont pas besoin d’être recréées lorsqu’un appareil est perdu.</span><span class="sxs-lookup"><span data-stu-id="dbacb-122">Managed resources are backed by system memory and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="dbacb-123">Pour plus d’informations, consultez [gestion des ressources (Direct3D 9)](managing-resources.md) .</span><span class="sxs-lookup"><span data-stu-id="dbacb-123">See [Managing Resources (Direct3D 9)](managing-resources.md) for more information.</span></span> <span data-ttu-id="dbacb-124">Les ressources managées peuvent être verrouillées.</span><span class="sxs-lookup"><span data-stu-id="dbacb-124">Managed resources can be locked.</span></span> <span data-ttu-id="dbacb-125">Seule la copie de la mémoire système est directement modifiée.</span><span class="sxs-lookup"><span data-stu-id="dbacb-125">Only the system-memory copy is directly modified.</span></span> <span data-ttu-id="dbacb-126">En fonction des besoins, Direct3D copie vos modifications dans la mémoire accessible par le pilote.</span><span class="sxs-lookup"><span data-stu-id="dbacb-126">Direct3D copies your changes to driver-accessible memory as needed.</span></span>



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbacb-127">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="dbacb-127">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="dbacb-128">D3DPOOL \_ Managed est valide avec [**IDirect3DDevice9**](/windows/desktop/api); Toutefois, il n’est pas valide avec [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span><span class="sxs-lookup"><span data-stu-id="dbacb-128">D3DPOOL\_MANAGED is valid with [**IDirect3DDevice9**](/windows/desktop/api); however, it is not valid with [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dbacb-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="dbacb-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="dbacb-130">Les ressources sont placées dans la mémoire qui n’est généralement pas accessible par le périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dbacb-130">Resources are placed in memory that is not typically accessible by the Direct3D device.</span></span> <span data-ttu-id="dbacb-131">Cette allocation de mémoire consomme la mémoire RAM du système, mais ne réduit pas la mémoire RAM paginable.</span><span class="sxs-lookup"><span data-stu-id="dbacb-131">This memory allocation consumes system RAM but does not reduce pageable RAM.</span></span> <span data-ttu-id="dbacb-132">Ces ressources n’ont pas besoin d’être recréées lorsqu’un appareil est perdu.</span><span class="sxs-lookup"><span data-stu-id="dbacb-132">These resources do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="dbacb-133">Les ressources de ce pool peuvent être verrouillées et peuvent être utilisées comme source pour une opération [**IDirect3DDevice9 :: UpdateSurface**](/windows/desktop/api) ou [**IDirect3DDevice9 :: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) sur une ressource mémoire créée avec D3DPOOL \_ par défaut.</span><span class="sxs-lookup"><span data-stu-id="dbacb-133">Resources in this pool can be locked and can be used as the source for a [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api) or [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) operation to a memory resource created with D3DPOOL\_DEFAULT.</span></span>

</dd> <dt>

<span data-ttu-id="dbacb-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**\_ÉRAFLURE D3DPOOL**</span><span class="sxs-lookup"><span data-stu-id="dbacb-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL\_SCRATCH**</span></span>
</dt> <dd>

<span data-ttu-id="dbacb-135">Les ressources sont placées dans la mémoire vive du système et n’ont pas besoin d’être recréées lorsqu’un appareil est perdu.</span><span class="sxs-lookup"><span data-stu-id="dbacb-135">Resources are placed in system RAM and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="dbacb-136">Ces ressources ne sont pas liées par la taille de l’appareil ou les restrictions de format.</span><span class="sxs-lookup"><span data-stu-id="dbacb-136">These resources are not bound by device size or format restrictions.</span></span> <span data-ttu-id="dbacb-137">Pour cette raison, ces ressources ne sont pas accessibles par l’appareil Direct3D ni définies en tant que textures ou cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="dbacb-137">Because of this, these resources cannot be accessed by the Direct3D device nor set as textures or render targets.</span></span> <span data-ttu-id="dbacb-138">Toutefois, ces ressources peuvent toujours être créées, verrouillées et copiées.</span><span class="sxs-lookup"><span data-stu-id="dbacb-138">However, these resources can always be created, locked, and copied.</span></span>

</dd> <dt>

<span data-ttu-id="dbacb-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="dbacb-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="dbacb-140">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="dbacb-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="dbacb-141">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dbacb-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="dbacb-142">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="dbacb-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbacb-143">Notes</span><span class="sxs-lookup"><span data-stu-id="dbacb-143">Remarks</span></span>

<span data-ttu-id="dbacb-144">Tous les types de pools sont valides avec toutes les ressources, notamment : les mémoires tampons de vertex, les mémoires tampons d’index, les textures et les surfaces.</span><span class="sxs-lookup"><span data-stu-id="dbacb-144">All pool types are valid with all resources including: vertex buffers, index buffers, textures, and surfaces.</span></span>

<span data-ttu-id="dbacb-145">Les tableaux suivants indiquent des restrictions sur les types de pools pour les cibles de rendu, les stencils de profondeur et les utilisations dynamiques et de mipmap.</span><span class="sxs-lookup"><span data-stu-id="dbacb-145">The following tables indicate restrictions on pool types for render targets, depth stencils, and dynamic and mipmap usages.</span></span> <span data-ttu-id="dbacb-146">Un x indique une combinaison compatible ; l’absence d’un x indique une incompatibilité.</span><span class="sxs-lookup"><span data-stu-id="dbacb-146">An x indicates a compatible combination; lack of an x indicates incompatibility.</span></span>



| <span data-ttu-id="dbacb-147">pool</span><span class="sxs-lookup"><span data-stu-id="dbacb-147">Pool</span></span>               | <span data-ttu-id="dbacb-148">D3DUSAGE \_ RENDERTARGET</span><span class="sxs-lookup"><span data-stu-id="dbacb-148">D3DUSAGE\_RENDERTARGET</span></span> | <span data-ttu-id="dbacb-149">D3DUSAGE \_ DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="dbacb-149">D3DUSAGE\_DEPTHSTENCIL</span></span> |
|--------------------|------------------------|------------------------|
| <span data-ttu-id="dbacb-150">D3DPOOL \_ par défaut</span><span class="sxs-lookup"><span data-stu-id="dbacb-150">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="dbacb-151">x</span><span class="sxs-lookup"><span data-stu-id="dbacb-151">x</span></span>                      | <span data-ttu-id="dbacb-152">x</span><span class="sxs-lookup"><span data-stu-id="dbacb-152">x</span></span>                      |
| <span data-ttu-id="dbacb-153">Géré par D3DPOOL \_</span><span class="sxs-lookup"><span data-stu-id="dbacb-153">D3DPOOL\_MANAGED</span></span>   |                        |                        |
| <span data-ttu-id="dbacb-154">\_ÉRAFLURE D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="dbacb-154">D3DPOOL\_SCRATCH</span></span>   |                        |                        |
| <span data-ttu-id="dbacb-155">D3DPOOL \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="dbacb-155">D3DPOOL\_SYSTEMMEM</span></span> |                        |                        |



 



| <span data-ttu-id="dbacb-156">pool</span><span class="sxs-lookup"><span data-stu-id="dbacb-156">Pool</span></span>               | <span data-ttu-id="dbacb-157">D3DUSAGE \_ dynamique</span><span class="sxs-lookup"><span data-stu-id="dbacb-157">D3DUSAGE\_DYNAMIC</span></span> | <span data-ttu-id="dbacb-158">D3DUSAGE \_ AUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="dbacb-158">D3DUSAGE\_AUTOGENMIPMAP</span></span> |
|--------------------|-------------------|-------------------------|
| <span data-ttu-id="dbacb-159">D3DPOOL \_ par défaut</span><span class="sxs-lookup"><span data-stu-id="dbacb-159">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="dbacb-160">x</span><span class="sxs-lookup"><span data-stu-id="dbacb-160">x</span></span>                 | <span data-ttu-id="dbacb-161">x</span><span class="sxs-lookup"><span data-stu-id="dbacb-161">x</span></span>                       |
| <span data-ttu-id="dbacb-162">Géré par D3DPOOL \_</span><span class="sxs-lookup"><span data-stu-id="dbacb-162">D3DPOOL\_MANAGED</span></span>   |                   | <span data-ttu-id="dbacb-163">x</span><span class="sxs-lookup"><span data-stu-id="dbacb-163">x</span></span>                       |
| <span data-ttu-id="dbacb-164">\_ÉRAFLURE D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="dbacb-164">D3DPOOL\_SCRATCH</span></span>   |                   |                         |
| <span data-ttu-id="dbacb-165">D3DPOOL \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="dbacb-165">D3DPOOL\_SYSTEMMEM</span></span> | <span data-ttu-id="dbacb-166">x</span><span class="sxs-lookup"><span data-stu-id="dbacb-166">x</span></span>                 |                         |



 

<span data-ttu-id="dbacb-167">Pour plus d’informations sur les types d’utilisation, consultez [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="dbacb-167">For more information about usage types, see [**D3DUSAGE**](d3dusage.md).</span></span>

<span data-ttu-id="dbacb-168">Les pools ne peuvent pas être mélangés pour différents objets contenus dans une ressource (niveaux MIP dans un mipmap) et, lorsqu’un pool est choisi, il ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="dbacb-168">Pools cannot be mixed for different objects contained within one resource (mip levels in a mipmap) and, when a pool is chosen, it cannot be changed.</span></span>

<span data-ttu-id="dbacb-169">Les applications doivent utiliser D3DPOOL \_ géré pour la plupart des ressources statiques, car cela évite à l’application d’avoir à gérer les périphériques perdus.</span><span class="sxs-lookup"><span data-stu-id="dbacb-169">Applications should use D3DPOOL\_MANAGED for most static resources because this saves the application from having to deal with lost devices.</span></span> <span data-ttu-id="dbacb-170">(Les ressources managées sont restaurées par le Runtime.) Cela est particulièrement bénéfique pour les systèmes d’architecture de mémoire unifiée (UMA).</span><span class="sxs-lookup"><span data-stu-id="dbacb-170">(Managed resources are restored by the runtime.) This is especially beneficial for unified memory architecture (UMA) systems.</span></span> <span data-ttu-id="dbacb-171">Les autres ressources dynamiques ne constituent pas une bonne correspondance pour la gestion de D3DPOOL \_ .</span><span class="sxs-lookup"><span data-stu-id="dbacb-171">Other dynamic resources are not a good match for D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="dbacb-172">En fait, les mémoires tampons d’index et les mémoires tampons de vertex ne peuvent pas être créées à l’aide \_ de D3DPOOL géré avec D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="dbacb-172">In fact, index buffers and vertex buffers cannot be created using D3DPOOL\_MANAGED together with D3DUSAGE\_DYNAMIC.</span></span>

<span data-ttu-id="dbacb-173">Pour les textures dynamiques, il est parfois préférable d’utiliser une paire de textures de mémoire vidéo et de mémoire système, d’allouer la mémoire vidéo à l’aide de D3DPOOL \_ par défaut et de la mémoire système à l’aide de D3DPOOL \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="dbacb-173">For dynamic textures, it is sometimes desirable to use a pair of video memory and system memory textures, allocating the video memory using D3DPOOL\_DEFAULT and the system memory using D3DPOOL\_SYSTEMMEM.</span></span> <span data-ttu-id="dbacb-174">Vous pouvez verrouiller et modifier les bits de la texture de la mémoire système à l’aide d’une méthode de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="dbacb-174">You can lock and modify the bits of the system memory texture using a locking method.</span></span> <span data-ttu-id="dbacb-175">Vous pouvez ensuite mettre à jour la texture de la mémoire vidéo à l’aide de [**IDirect3DDevice9 :: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span><span class="sxs-lookup"><span data-stu-id="dbacb-175">Then you can update the video memory texture using [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbacb-176">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbacb-176">Requirements</span></span>



| <span data-ttu-id="dbacb-177">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbacb-177">Requirement</span></span> | <span data-ttu-id="dbacb-178">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbacb-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbacb-179">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbacb-179">Header</span></span><br/> | <dl> <span data-ttu-id="dbacb-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbacb-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbacb-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbacb-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbacb-182">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="dbacb-182">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="dbacb-183">**D3DUSAGE**</span><span class="sxs-lookup"><span data-stu-id="dbacb-183">**D3DUSAGE**</span></span>](d3dusage.md)
</dt> <dt>

[<span data-ttu-id="dbacb-184">**IDirect3DDevice9::CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="dbacb-184">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[<span data-ttu-id="dbacb-185">**IDirect3DDevice9::CreateIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="dbacb-185">**IDirect3DDevice9::CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[<span data-ttu-id="dbacb-186">**IDirect3DDevice9::CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="dbacb-186">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[<span data-ttu-id="dbacb-187">**IDirect3DDevice9::CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="dbacb-187">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[<span data-ttu-id="dbacb-188">**IDirect3DDevice9::CreateVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="dbacb-188">**IDirect3DDevice9::CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[<span data-ttu-id="dbacb-189">**D3DINDEXBUFFER \_ desc**</span><span class="sxs-lookup"><span data-stu-id="dbacb-189">**D3DINDEXBUFFER\_DESC**</span></span>](d3dindexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="dbacb-190">**D3DSURFACE \_ desc**</span><span class="sxs-lookup"><span data-stu-id="dbacb-190">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> <dt>

[<span data-ttu-id="dbacb-191">**D3DVERTEXBUFFER \_ desc**</span><span class="sxs-lookup"><span data-stu-id="dbacb-191">**D3DVERTEXBUFFER\_DESC**</span></span>](d3dvertexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="dbacb-192">**D3DVOLUME \_ desc**</span><span class="sxs-lookup"><span data-stu-id="dbacb-192">**D3DVOLUME\_DESC**</span></span>](d3dvolume-desc.md)
</dt> </dl>

 

 
