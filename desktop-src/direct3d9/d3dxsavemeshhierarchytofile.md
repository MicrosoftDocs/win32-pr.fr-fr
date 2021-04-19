---
description: Crée un fichier. x et y enregistre la hiérarchie de maillage et les animations correspondantes.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: D3DXSaveMeshHierarchyToFile, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538511"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a><span data-ttu-id="0928d-103">D3DXSaveMeshHierarchyToFile fonction)</span><span class="sxs-lookup"><span data-stu-id="0928d-103">D3DXSaveMeshHierarchyToFile function</span></span>

<span data-ttu-id="0928d-104">Crée un fichier. x et y enregistre la hiérarchie de maillage et les animations correspondantes.</span><span class="sxs-lookup"><span data-stu-id="0928d-104">Creates a .x file and saves the mesh hierarchy and corresponding animations in it.</span></span>

## <a name="syntax"></a><span data-ttu-id="0928d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0928d-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a><span data-ttu-id="0928d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0928d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0928d-107">*pFilename* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0928d-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0928d-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0928d-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0928d-109">Pointeur vers une chaîne qui spécifie le nom du fichier. x identifiant le maillage enregistré.</span><span class="sxs-lookup"><span data-stu-id="0928d-109">Pointer to a string that specifies the name of the .x file identifying the saved mesh.</span></span> <span data-ttu-id="0928d-110">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="0928d-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0928d-111">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="0928d-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="0928d-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0928d-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0928d-113">*XFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0928d-113">*XFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0928d-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0928d-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0928d-115">Format du fichier. x (texte ou binaire, compressé ou non).</span><span class="sxs-lookup"><span data-stu-id="0928d-115">Format of the .x file (text or binary, compressed or not).</span></span> <span data-ttu-id="0928d-116">Consultez D3DXF \_ FILEFORMAT.</span><span class="sxs-lookup"><span data-stu-id="0928d-116">See D3DXF\_FILEFORMAT.</span></span> <span data-ttu-id="0928d-117">D3DXF \_ FileFormat \_ Compressed peut être combiné (à l’aide d’un or logique) avec les \_ indicateurs de texte D3DXF FileFormat \_ ou D3DXF \_ FileFormat \_ pour réduire la taille du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="0928d-117">D3DXF\_FILEFORMAT\_COMPRESSED can be combined (using a logical OR) with either the D3DXF\_FILEFORMAT\_BINARY or D3DXF\_FILEFORMAT\_TEXT flags to reduce the output file size.</span></span>

</dd> <dt>

<span data-ttu-id="0928d-118">*pFrameRoot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0928d-118">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0928d-119">Type : **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="0928d-119">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="0928d-120">Nœud racine de la hiérarchie à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="0928d-120">Root node of the hierarchy to be saved.</span></span> <span data-ttu-id="0928d-121">Consultez [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="0928d-121">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="0928d-122">*pAnimController* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0928d-122">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0928d-123">Type : **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="0928d-123">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="0928d-124">Contrôleur d’animation qui contient les jeux d’animations à stocker.</span><span class="sxs-lookup"><span data-stu-id="0928d-124">Animation controller that has animation sets to be stored.</span></span> <span data-ttu-id="0928d-125">Consultez [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="0928d-125">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="0928d-126">*pUserDataSaver* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0928d-126">*pUserDataSaver* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0928d-127">Type : **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="0928d-127">Type: **[**LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span></span>

<span data-ttu-id="0928d-128">Interface fournie par l’application qui permet l’enregistrement des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0928d-128">Application-provided interface that allows saving of user data.</span></span> <span data-ttu-id="0928d-129">Consultez [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span><span class="sxs-lookup"><span data-stu-id="0928d-129">See [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0928d-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0928d-130">Return value</span></span>

<span data-ttu-id="0928d-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0928d-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0928d-132">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0928d-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0928d-133">Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0928d-133">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0928d-134">Notes</span><span class="sxs-lookup"><span data-stu-id="0928d-134">Remarks</span></span>

<span data-ttu-id="0928d-135">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="0928d-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0928d-136">Si Unicode est défini, l’appel de fonction est résolu en D3DXSaveMeshHierarchyToFileW.</span><span class="sxs-lookup"><span data-stu-id="0928d-136">If Unicode is defined, the function call resolves to D3DXSaveMeshHierarchyToFileW.</span></span> <span data-ttu-id="0928d-137">Dans le cas contraire, l’appel de fonction est résolu en D3DXSaveMeshHierarchyToFileA.</span><span class="sxs-lookup"><span data-stu-id="0928d-137">Otherwise, the function call resolves to D3DXSaveMeshHierarchyToFileA.</span></span>

<span data-ttu-id="0928d-138">Cette fonction n’enregistre pas les jeux d’animations compressés.</span><span class="sxs-lookup"><span data-stu-id="0928d-138">This function does not save compressed animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="0928d-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0928d-139">Requirements</span></span>



| <span data-ttu-id="0928d-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0928d-140">Requirement</span></span> | <span data-ttu-id="0928d-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="0928d-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0928d-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="0928d-142">Header</span></span><br/>  | <dl> <span data-ttu-id="0928d-143"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0928d-143"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0928d-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0928d-144">Library</span></span><br/> | <dl> <span data-ttu-id="0928d-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0928d-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0928d-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0928d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0928d-147">Fonctions d’animation</span><span class="sxs-lookup"><span data-stu-id="0928d-147">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[<span data-ttu-id="0928d-148">Référence de fichier X</span><span class="sxs-lookup"><span data-stu-id="0928d-148">X File Reference</span></span>](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
