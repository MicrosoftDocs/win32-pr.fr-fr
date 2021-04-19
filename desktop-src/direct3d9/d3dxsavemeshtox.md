---
description: Enregistre un maillage dans un fichier. x.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: D3DXSaveMeshToX, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 504e7ad69b83c67dad52ebbf0f6d1eef8639a9fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545278"
---
# <a name="d3dxsavemeshtox-function"></a><span data-ttu-id="752de-103">D3DXSaveMeshToX fonction)</span><span class="sxs-lookup"><span data-stu-id="752de-103">D3DXSaveMeshToX function</span></span>

<span data-ttu-id="752de-104">Enregistre un maillage dans un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="752de-104">Saves a mesh to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="752de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="752de-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a><span data-ttu-id="752de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="752de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="752de-107">*pFilename* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752de-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752de-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="752de-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="752de-109">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="752de-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="752de-110">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="752de-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="752de-111">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="752de-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="752de-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="752de-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="752de-113">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752de-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752de-114">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="752de-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="752de-115">Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) , qui représente le maillage à enregistrer dans un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="752de-115">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to save to a .x file.</span></span>

</dd> <dt>

<span data-ttu-id="752de-116">*pAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752de-116">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752de-117">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="752de-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="752de-118">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille.</span><span class="sxs-lookup"><span data-stu-id="752de-118">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="752de-119">Ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="752de-119">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="752de-120">*pMaterials* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752de-120">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752de-121">Type : **const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="752de-121">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="752de-122">Pointeur vers un tableau de structures [**D3DXMATERIAL**](d3dxmaterial.md) , contenant les informations de matériau à enregistrer dans le fichier. x.</span><span class="sxs-lookup"><span data-stu-id="752de-122">Pointer to an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing material information to be saved in the .x file.</span></span>

</dd> <dt>

<span data-ttu-id="752de-123">*pEffectInstances* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752de-123">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752de-124">Type : **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="752de-124">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="752de-125">Pointeur vers un tableau d’instances d’effet, un par groupe d’attributs dans la maille.</span><span class="sxs-lookup"><span data-stu-id="752de-125">Pointer to an array of effect instances, one per attribute group in the mesh.</span></span> <span data-ttu-id="752de-126">Ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="752de-126">This parameter may be **NULL**.</span></span> <span data-ttu-id="752de-127">Une instance Effect est une instance particulière d’informations d’état utilisée pour initialiser un effet.</span><span class="sxs-lookup"><span data-stu-id="752de-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="752de-128">Pour plus d’informations, consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="752de-128">For more information, see [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="752de-129">*NumMaterials* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752de-129">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752de-130">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="752de-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="752de-131">Nombre de structures [**D3DXMATERIAL**](d3dxmaterial.md) dans le tableau *pMaterials* .</span><span class="sxs-lookup"><span data-stu-id="752de-131">Number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *pMaterials* array.</span></span>

</dd> <dt>

<span data-ttu-id="752de-132">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752de-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752de-133">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="752de-133">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="752de-134">Combinaison de format de fichier et d’options d’enregistrement lors de l’enregistrement d’un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="752de-134">A combination of file format and save options when saving an .x file.</span></span> <span data-ttu-id="752de-135">Consultez les [constantes de fichier D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md).</span><span class="sxs-lookup"><span data-stu-id="752de-135">See [D3DX X File Constants](dx9-graphics-reference-d3dx-x-file-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="752de-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="752de-136">Return value</span></span>

<span data-ttu-id="752de-137">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="752de-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="752de-138">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="752de-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="752de-139">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="752de-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="752de-140">Notes</span><span class="sxs-lookup"><span data-stu-id="752de-140">Remarks</span></span>

<span data-ttu-id="752de-141">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="752de-141">The compiler setting also determines the function version.</span></span> <span data-ttu-id="752de-142">Si Unicode est défini, l’appel de fonction est résolu en D3DXSaveMeshToXW.</span><span class="sxs-lookup"><span data-stu-id="752de-142">If Unicode is defined, the function call resolves to D3DXSaveMeshToXW.</span></span> <span data-ttu-id="752de-143">Dans le cas contraire, l’appel de fonction est résolu en D3DXSaveMeshToXA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="752de-143">Otherwise, the function call resolves to D3DXSaveMeshToXA because ANSI strings are being used.</span></span>

<span data-ttu-id="752de-144">Le format de fichier par défaut est binaire ; Toutefois, si un fichier est spécifié à la fois comme un fichier binaire et un fichier texte, il sera enregistré en tant que fichier texte.</span><span class="sxs-lookup"><span data-stu-id="752de-144">The default file format is binary; however, if a file is specified as both a binary and a text file, it will be saved as a text file.</span></span> <span data-ttu-id="752de-145">Quel que soit le format de fichier, vous pouvez également utiliser le format compressé pour réduire la taille du fichier.</span><span class="sxs-lookup"><span data-stu-id="752de-145">Regardless of the file format, you may also use the compressed format to reduce the file size.</span></span>

<span data-ttu-id="752de-146">Voici un exemple de code standard illustrant l’utilisation de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="752de-146">The following is a typical code example of how to use this function.</span></span>


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



## <a name="requirements"></a><span data-ttu-id="752de-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="752de-147">Requirements</span></span>



| <span data-ttu-id="752de-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="752de-148">Requirement</span></span> | <span data-ttu-id="752de-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="752de-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="752de-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="752de-150">Header</span></span><br/>  | <dl> <span data-ttu-id="752de-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="752de-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="752de-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="752de-152">Library</span></span><br/> | <dl> <span data-ttu-id="752de-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="752de-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="752de-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="752de-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="752de-155">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="752de-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="752de-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="752de-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="752de-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="752de-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
