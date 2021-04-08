---
description: Verrouille un tampon d’index et obtient un pointeur vers la mémoire tampon d’index.
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: 'ID3DXBaseMesh :: LockIndexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 388915d0d11ff910c19a2c70b305597a79cd04bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043080"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a><span data-ttu-id="152eb-103">ID3DXBaseMesh :: LockIndexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="152eb-103">ID3DXBaseMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="152eb-104">Verrouille un tampon d’index et obtient un pointeur vers la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="152eb-104">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="152eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="152eb-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="152eb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="152eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="152eb-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="152eb-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="152eb-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="152eb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="152eb-109">Combinaison de zéro ou plusieurs indicateurs de verrouillage qui décrivent le type de verrou à effectuer.</span><span class="sxs-lookup"><span data-stu-id="152eb-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="152eb-110">Pour cette méthode, les indicateurs valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="152eb-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="152eb-111">D3DLOCK \_ Ignorer</span><span class="sxs-lookup"><span data-stu-id="152eb-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="152eb-112">D3DLOCK \_ aucune \_ \_ mise à jour incorrecte</span><span class="sxs-lookup"><span data-stu-id="152eb-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="152eb-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="152eb-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="152eb-114">D3DLOCK en \_ lecture seule</span><span class="sxs-lookup"><span data-stu-id="152eb-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="152eb-115">Pour obtenir une description des indicateurs, consultez [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="152eb-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="152eb-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="152eb-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="152eb-117">Type : **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="152eb-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="152eb-118">\*Pointeur void vers une mémoire tampon contenant les données d’index.</span><span class="sxs-lookup"><span data-stu-id="152eb-118">VOID\* pointer to a buffer containing the index data.</span></span> <span data-ttu-id="152eb-119">Le nombre d’index dans cette mémoire tampon est égal à [**ID3DXBaseMesh :: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.</span><span class="sxs-lookup"><span data-stu-id="152eb-119">The count of indices in this buffer will be equal to [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="152eb-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="152eb-120">Return value</span></span>

<span data-ttu-id="152eb-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="152eb-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="152eb-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="152eb-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="152eb-123">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="152eb-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="152eb-124">Notes</span><span class="sxs-lookup"><span data-stu-id="152eb-124">Remarks</span></span>

<span data-ttu-id="152eb-125">Lorsque vous utilisez des mémoires tampons d’index, vous êtes autorisé à effectuer plusieurs appels de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="152eb-125">When working with index buffers, you are allowed to make multiple lock calls.</span></span> <span data-ttu-id="152eb-126">Toutefois, vous devez vous assurer que le nombre d’appels de verrous correspond au nombre d’appels de déverrouillage.</span><span class="sxs-lookup"><span data-stu-id="152eb-126">However, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="152eb-127">Les appels DrawPrimitive échouent avec un nombre de verrous en attente sur un tampon d’index actuellement défini.</span><span class="sxs-lookup"><span data-stu-id="152eb-127">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set index buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="152eb-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="152eb-128">Requirements</span></span>



| <span data-ttu-id="152eb-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="152eb-129">Requirement</span></span> | <span data-ttu-id="152eb-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="152eb-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="152eb-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="152eb-131">Header</span></span><br/>  | <dl> <span data-ttu-id="152eb-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="152eb-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="152eb-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="152eb-133">Library</span></span><br/> | <dl> <span data-ttu-id="152eb-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="152eb-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="152eb-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="152eb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152eb-136">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="152eb-136">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
