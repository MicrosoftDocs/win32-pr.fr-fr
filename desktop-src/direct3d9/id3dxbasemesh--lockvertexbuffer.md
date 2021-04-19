---
description: Verrouille une mémoire tampon de vertex et obtient un pointeur vers la mémoire tampon de vertex.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'ID3DXBaseMesh :: LockVertexBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e93e59715d9f262d7693f2bef652f8be63337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523195"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a><span data-ttu-id="d1c56-103">ID3DXBaseMesh :: LockVertexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="d1c56-103">ID3DXBaseMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="d1c56-104">Verrouille une mémoire tampon de vertex et obtient un pointeur vers la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="d1c56-104">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c56-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1c56-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="d1c56-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1c56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1c56-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="d1c56-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c56-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1c56-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1c56-109">Combinaison de zéro ou plusieurs indicateurs de verrouillage qui décrivent le type de verrou à effectuer.</span><span class="sxs-lookup"><span data-stu-id="d1c56-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="d1c56-110">Pour cette méthode, les indicateurs valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d1c56-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="d1c56-111">D3DLOCK \_ Ignorer</span><span class="sxs-lookup"><span data-stu-id="d1c56-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="d1c56-112">D3DLOCK \_ aucune \_ \_ mise à jour incorrecte</span><span class="sxs-lookup"><span data-stu-id="d1c56-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="d1c56-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="d1c56-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="d1c56-114">D3DLOCK en \_ lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1c56-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="d1c56-115">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="d1c56-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="d1c56-116">Pour obtenir une description des indicateurs, consultez [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="d1c56-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1c56-117">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d1c56-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d1c56-118">Type : **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1c56-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d1c56-119">\*Pointeur void vers une mémoire tampon contenant les données de vertex.</span><span class="sxs-lookup"><span data-stu-id="d1c56-119">VOID\* pointer to a buffer containing the vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1c56-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1c56-120">Return value</span></span>

<span data-ttu-id="d1c56-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d1c56-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d1c56-122">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d1c56-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d1c56-123">Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d1c56-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1c56-124">Notes</span><span class="sxs-lookup"><span data-stu-id="d1c56-124">Remarks</span></span>

<span data-ttu-id="d1c56-125">Lorsque vous utilisez des mémoires tampons de vertex, vous êtes autorisé à effectuer plusieurs appels de verrouillage. Toutefois, vous devez vous assurer que le nombre d’appels de verrous correspond au nombre d’appels de déverrouillage.</span><span class="sxs-lookup"><span data-stu-id="d1c56-125">When working with vertex buffers, you are allowed to make multiple lock calls; however, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="d1c56-126">Les appels DrawPrimitive échouent avec un nombre de verrous en attente sur une mémoire tampon de vertex actuellement définie.</span><span class="sxs-lookup"><span data-stu-id="d1c56-126">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set vertex buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1c56-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1c56-127">Requirements</span></span>



| <span data-ttu-id="d1c56-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1c56-128">Requirement</span></span> | <span data-ttu-id="d1c56-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1c56-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c56-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1c56-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d1c56-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1c56-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d1c56-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1c56-132">Library</span></span><br/> | <dl> <span data-ttu-id="d1c56-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1c56-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d1c56-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1c56-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c56-135">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="d1c56-135">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
