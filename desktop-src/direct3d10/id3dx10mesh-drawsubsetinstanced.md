---
description: Dessinez plusieurs instances du même sous-ensemble d’une maille.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: ID3DX10Mesh ::D méthode rawSubsetInstanced (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2e28d7a7d2c1d743090832d68793ec3743662308
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335633"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a><span data-ttu-id="81a07-103">ID3DX10Mesh ::D méthode rawSubsetInstanced</span><span class="sxs-lookup"><span data-stu-id="81a07-103">ID3DX10Mesh::DrawSubsetInstanced method</span></span>

<span data-ttu-id="81a07-104">Dessinez plusieurs instances du même sous-ensemble d’une maille.</span><span class="sxs-lookup"><span data-stu-id="81a07-104">Draw several instances of the same subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81a07-105">Syntax</span></span>


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="81a07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81a07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a07-107">*AttribId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81a07-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a07-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81a07-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81a07-109">Spécifie le sous-ensemble du maillage à dessiner.</span><span class="sxs-lookup"><span data-stu-id="81a07-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="81a07-110">Cette valeur est utilisée pour différencier les visages d’un maillage comme appartenant à un ou plusieurs groupes d’attributs.</span><span class="sxs-lookup"><span data-stu-id="81a07-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span> <span data-ttu-id="81a07-111">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="81a07-111">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="81a07-112">*InstanceCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81a07-112">*InstanceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a07-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81a07-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81a07-114">Nombre d’instances à restituer.</span><span class="sxs-lookup"><span data-stu-id="81a07-114">Number of instances to render.</span></span>

</dd> <dt>

<span data-ttu-id="81a07-115">*StartInstanceLocation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81a07-115">*StartInstanceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a07-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81a07-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81a07-117">L’instance à partir de laquelle commencer l’extraction dans chaque mémoire tampon marquée comme des données d’instance.</span><span class="sxs-lookup"><span data-stu-id="81a07-117">Which instance to start fetching from in each buffer marked as instance data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a07-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="81a07-118">Return value</span></span>

<span data-ttu-id="81a07-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81a07-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81a07-120">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="81a07-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="81a07-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="81a07-121">Remarks</span></span>

<span data-ttu-id="81a07-122">Une maille contient une table d’attributs.</span><span class="sxs-lookup"><span data-stu-id="81a07-122">A mesh contains an attribute table.</span></span> <span data-ttu-id="81a07-123">La table d’attributs peut diviser un maillage en sous-ensembles, où chaque sous-ensemble est identifié par un ID d’attribut.</span><span class="sxs-lookup"><span data-stu-id="81a07-123">The attribute table can divide a mesh into subsets, where each subset is identified with an attribute ID.</span></span> <span data-ttu-id="81a07-124">Par exemple, un maillage avec 200 faces, divisé en trois sous-ensembles, peut avoir une table d’attributs qui ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="81a07-124">For example, a mesh with 200 faces, divided into three subsets, might have an attribute table that looks like this:</span></span>



| <span data-ttu-id="81a07-125">Subset</span><span class="sxs-lookup"><span data-stu-id="81a07-125">Subset</span></span>     | <span data-ttu-id="81a07-126">Visages</span><span class="sxs-lookup"><span data-stu-id="81a07-126">Faces</span></span>           |
|------------|-----------------|
| <span data-ttu-id="81a07-127">AttribID 0</span><span class="sxs-lookup"><span data-stu-id="81a07-127">AttribID 0</span></span> | <span data-ttu-id="81a07-128">Visages 0 ~ 50</span><span class="sxs-lookup"><span data-stu-id="81a07-128">Faces 0 ~ 50</span></span>    |
| <span data-ttu-id="81a07-129">AttribID 1</span><span class="sxs-lookup"><span data-stu-id="81a07-129">AttribID 1</span></span> | <span data-ttu-id="81a07-130">Visages 51 ~ 125</span><span class="sxs-lookup"><span data-stu-id="81a07-130">Faces 51 ~ 125</span></span>  |
| <span data-ttu-id="81a07-131">AttribID 2</span><span class="sxs-lookup"><span data-stu-id="81a07-131">AttribID 2</span></span> | <span data-ttu-id="81a07-132">Visages 126 ~ 200</span><span class="sxs-lookup"><span data-stu-id="81a07-132">Faces 126 ~ 200</span></span> |



 

<span data-ttu-id="81a07-133">L’instanciation peut étendre les performances en réutilisant la même géométrie pour dessiner plusieurs objets dans une scène.</span><span class="sxs-lookup"><span data-stu-id="81a07-133">Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene.</span></span> <span data-ttu-id="81a07-134">Un exemple d’instanciation pourrait consister à dessiner le même objet avec des positions et des couleurs différentes.</span><span class="sxs-lookup"><span data-stu-id="81a07-134">One example of instancing could be to draw the same object with different positions and colors.</span></span> <span data-ttu-id="81a07-135">L’indexation requiert plusieurs mémoires tampons de vertex : au moins une pour les données par vertex et une deuxième mémoire tampon pour les données par instance.</span><span class="sxs-lookup"><span data-stu-id="81a07-135">Indexing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data.</span></span>

<span data-ttu-id="81a07-136">Les instances de dessin avec DrawSubsetInstanced sont très similaires au processus utilisé avec [**ID3D10Device ::D rawindexedinstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) décrit dans [exemple d’instanciation](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="81a07-136">Drawing instances with DrawSubsetInstanced is very similar to the process used with [**ID3D10Device::DrawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) that is outlined in [Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span></span> <span data-ttu-id="81a07-137">La principale différence lors de l’utilisation de DrawSubsetInstanced est que les mémoires tampons de vertex et d’index doivent être extraites de l’objet d' [**interface ID3DX10Mesh**](id3dx10mesh.md) avant que les données d’instanciation puissent être combinées.</span><span class="sxs-lookup"><span data-stu-id="81a07-137">The key difference when using DrawSubsetInstanced is that vertex and index buffers must be extracted from the [**ID3DX10Mesh Interface**](id3dx10mesh.md) object before the instancing data can be combined.</span></span>

<span data-ttu-id="81a07-138">Le code suivant illustre l’extraction des tampons de vertex et d’index à partir de l’objet de maillage.</span><span class="sxs-lookup"><span data-stu-id="81a07-138">The following code illustrates extracting the vertex and index buffers from the mesh object.</span></span>


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a><span data-ttu-id="81a07-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81a07-139">Requirements</span></span>



| <span data-ttu-id="81a07-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81a07-140">Requirement</span></span> | <span data-ttu-id="81a07-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="81a07-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81a07-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="81a07-142">Header</span></span><br/>  | <dl> <span data-ttu-id="81a07-143"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="81a07-143"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="81a07-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81a07-144">Library</span></span><br/> | <dl> <span data-ttu-id="81a07-145"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81a07-145"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81a07-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81a07-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a07-147">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="81a07-147">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="81a07-148">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="81a07-148">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
