---
description: D3DXLoadMeshHierarchyFromX fonction-charge la première hiérarchie d’images à partir d’un fichier. x.
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: D3DXLoadMeshHierarchyFromX, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f6f08e10155509df800cca3cb3788d6b27e520
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114357"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a><span data-ttu-id="db243-103">D3DXLoadMeshHierarchyFromX fonction)</span><span class="sxs-lookup"><span data-stu-id="db243-103">D3DXLoadMeshHierarchyFromX function</span></span>

<span data-ttu-id="db243-104">Charge la première hiérarchie d’images à partir d’un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="db243-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="db243-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db243-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="db243-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db243-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db243-107">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db243-107">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db243-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db243-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db243-109">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="db243-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="db243-110">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="db243-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="db243-111">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="db243-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="db243-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="db243-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="db243-113">*MeshOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db243-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db243-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db243-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db243-115">Combinaison d’un ou plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) qui spécifient les options de création du maillage.</span><span class="sxs-lookup"><span data-stu-id="db243-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="db243-116">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db243-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db243-117">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="db243-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="db243-118">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="db243-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="db243-119">*pAlloc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db243-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db243-120">Type : **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="db243-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="db243-121">Pointeur vers une interface [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="db243-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="db243-122">*pUserDataLoader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db243-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db243-123">Type : **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="db243-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="db243-124">Interface fournie par l’application qui permet le chargement des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db243-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="db243-125">Consultez [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span><span class="sxs-lookup"><span data-stu-id="db243-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="db243-126">*ppFrameHierarchy* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="db243-126">*ppFrameHierarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db243-127">Type : **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="db243-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="db243-128">Retourne un pointeur vers la hiérarchie de frames chargée.</span><span class="sxs-lookup"><span data-stu-id="db243-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="db243-129">Consultez [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="db243-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="db243-130">*ppAnimController* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="db243-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db243-131">Type : **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="db243-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="db243-132">Retourne un pointeur vers le contrôleur d’animation correspondant à l’animation dans le fichier. x.</span><span class="sxs-lookup"><span data-stu-id="db243-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="db243-133">Il est créé avec des suivis et des événements par défaut.</span><span class="sxs-lookup"><span data-stu-id="db243-133">This is created with default tracks and events.</span></span> <span data-ttu-id="db243-134">Consultez [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="db243-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db243-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="db243-135">Return value</span></span>

<span data-ttu-id="db243-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db243-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db243-137">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db243-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="db243-138">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="db243-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="db243-139">Notes </span><span class="sxs-lookup"><span data-stu-id="db243-139">Remarks</span></span>

<span data-ttu-id="db243-140">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="db243-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="db243-141">Si Unicode est défini, l’appel de fonction est résolu en D3DXLoadMeshHierarchyFromXW.</span><span class="sxs-lookup"><span data-stu-id="db243-141">If Unicode is defined, the function call resolves to D3DXLoadMeshHierarchyFromXW.</span></span> <span data-ttu-id="db243-142">Dans le cas contraire, l’appel de fonction est résolu en D3DXLoadMeshHierarchyFromXA.</span><span class="sxs-lookup"><span data-stu-id="db243-142">Otherwise, the function call resolves to D3DXLoadMeshHierarchyFromXA.</span></span>

<span data-ttu-id="db243-143">Tous les maillages du fichier seront réduits en un seul maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="db243-143">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="db243-144">Si le fichier contient une hiérarchie de frames, toutes les transformations sont appliquées à la maille.</span><span class="sxs-lookup"><span data-stu-id="db243-144">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="db243-145">**D3DXLoadMeshHierarchyFromX** charge les données d’animation et la hiérarchie d’images à partir d’un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="db243-145">**D3DXLoadMeshHierarchyFromX** loads the animation data and frame hierarchy from a .x file.</span></span> <span data-ttu-id="db243-146">Il analyse le fichier. x et génère une hiérarchie d’images et un contrôleur d’animation en fonction de l’objet dérivé de [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)qui lui est passé par le biais de pAlloc.</span><span class="sxs-lookup"><span data-stu-id="db243-146">It scans the .x file and builds a frame hierarchy and animation controller according to the [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)-derived object passed to it through pAlloc.</span></span> <span data-ttu-id="db243-147">Le chargement des données nécessite plusieurs étapes, comme suit :</span><span class="sxs-lookup"><span data-stu-id="db243-147">Loading the data requires several steps as follows:</span></span>

1.  <span data-ttu-id="db243-148">Dérivez [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), en implémentant chaque méthode.</span><span class="sxs-lookup"><span data-stu-id="db243-148">Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementing each method.</span></span> <span data-ttu-id="db243-149">Cela contrôle la manière dont les images et les maillages sont alloués et libérés.</span><span class="sxs-lookup"><span data-stu-id="db243-149">This controls how frames and meshes are allocated and freed.</span></span>
2.  <span data-ttu-id="db243-150">Dérivez [**ID3DXLoadUserData**](id3dxloaduserdata.md), en implémentant chaque méthode.</span><span class="sxs-lookup"><span data-stu-id="db243-150">Derive [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementing each method.</span></span> <span data-ttu-id="db243-151">Si votre fichier. x n’a pas de données incorporées définies par l’utilisateur ou si vous n’en avez pas besoin, vous pouvez ignorer cette partie.</span><span class="sxs-lookup"><span data-stu-id="db243-151">If your .x file has no embedded user-defined data, or if you do not need it, you can skip this part.</span></span>
3.  <span data-ttu-id="db243-152">Créez un objet de votre classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) , et éventuellement de votre classe LoadUserData.</span><span class="sxs-lookup"><span data-stu-id="db243-152">Create an object of your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class, and optionally of your LoadUserData class.</span></span> <span data-ttu-id="db243-153">Vous n’avez pas besoin d’appeler les méthodes de ces objets vous-même.</span><span class="sxs-lookup"><span data-stu-id="db243-153">You do not need to call any methods of these objects yourself.</span></span>
4.  <span data-ttu-id="db243-154">Appelez **D3DXLoadMeshHierarchyFromX**, en passant votre objet [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) et votre objet [**ID3DXLoadUserData**](id3dxloaduserdata.md) (ou **null**) pour créer la hiérarchie d’images et le contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="db243-154">Call **D3DXLoadMeshHierarchyFromX**, passing in your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) object and your [**ID3DXLoadUserData**](id3dxloaduserdata.md) object (or **NULL**) to create the frame hierarchy and animation controller.</span></span> <span data-ttu-id="db243-155">Tous les jeux d’animations et les frames sont automatiquement inscrits sur le contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="db243-155">All the animation sets and frames are automatically registered to the animation controller.</span></span>

<span data-ttu-id="db243-156">Pendant le chargement, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) et [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) sont rappelés sur chaque frame pour contrôler le chargement et l’allocation du frame.</span><span class="sxs-lookup"><span data-stu-id="db243-156">During the load, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) and [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) are called back on each frame to control loading and allocation of the frame.</span></span> <span data-ttu-id="db243-157">L’application définit ces méthodes pour contrôler le mode de stockage des frames.</span><span class="sxs-lookup"><span data-stu-id="db243-157">The application defines these methods to control how frames are stored.</span></span> <span data-ttu-id="db243-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) et [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) sont rappelés sur chaque objet de maillage pour contrôler le chargement et l’allocation des objets de maillage.</span><span class="sxs-lookup"><span data-stu-id="db243-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) and [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) are called back on each mesh object to control loading and allocation of mesh objects.</span></span> <span data-ttu-id="db243-159">[**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) est rappelée pour chaque objet de niveau supérieur qui n’est pas chargé par les autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="db243-159">[**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) is called back for each top level object that doesn't get loaded by the other methods.</span></span>

<span data-ttu-id="db243-160">Pour libérer ces données, appelez ID3DXAnimationController :: Release pour libérer les jeux d’animations et [**D3DXFRAMEDestroy**](d3dxframedestroy.md), en passant le nœud racine de la hiérarchie de frames et un objet de votre classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) dérivée.</span><span class="sxs-lookup"><span data-stu-id="db243-160">To free this data, call ID3DXAnimationController::Release to free the animation sets, and [**D3DXFRAMEDestroy**](d3dxframedestroy.md), passing in the root node of the frame hierarchy and an object of your derived [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class.</span></span> <span data-ttu-id="db243-161">[**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) et [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) sont appelés pour chaque objet Frame et Mesh dans la hiérarchie d’images.</span><span class="sxs-lookup"><span data-stu-id="db243-161">[**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) and [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) will each be called for every frame and mesh object in the frame hierarchy.</span></span> <span data-ttu-id="db243-162">Votre implémentation de **DestroyFrame** doit libérer tout ce qui est alloué par [**CreateFrame**](id3dxallocatehierarchy--createframe.md), et de la même façon pour les méthodes de conteneur de maillage.</span><span class="sxs-lookup"><span data-stu-id="db243-162">Your implementation of **DestroyFrame** should release everything allocated by [**CreateFrame**](id3dxallocatehierarchy--createframe.md), and likewise for the mesh container methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="db243-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db243-163">Requirements</span></span>



| <span data-ttu-id="db243-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db243-164">Requirement</span></span> | <span data-ttu-id="db243-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="db243-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db243-166">En-tête</span><span class="sxs-lookup"><span data-stu-id="db243-166">Header</span></span><br/>  | <dl> <span data-ttu-id="db243-167"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="db243-167"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="db243-168">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="db243-168">Library</span></span><br/> | <dl> <span data-ttu-id="db243-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db243-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db243-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db243-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db243-171">Fonctions d’animation</span><span class="sxs-lookup"><span data-stu-id="db243-171">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
