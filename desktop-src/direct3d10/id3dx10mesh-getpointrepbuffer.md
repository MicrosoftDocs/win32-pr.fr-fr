---
description: Obtient la mémoire tampon du REP du point de la maille.
ms.assetid: 4be7bee5-15ea-496f-83c2-a3a9bafd97c6
title: 'ID3DX10Mesh :: GetPointRepBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetPointRepBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 131094792f35b21fd230b66bda6a43fb104b65ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116234"
---
# <a name="id3dx10meshgetpointrepbuffer-method"></a><span data-ttu-id="e770a-103">ID3DX10Mesh :: GetPointRepBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="e770a-103">ID3DX10Mesh::GetPointRepBuffer method</span></span>

<span data-ttu-id="e770a-104">Obtient la mémoire tampon du REP du point de la maille.</span><span class="sxs-lookup"><span data-stu-id="e770a-104">Get the mesh's point rep buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e770a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e770a-105">Syntax</span></span>


```C++
HRESULT GetPointRepBuffer(
  [out] ID3DX10MeshBuffer **ppPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="e770a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e770a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e770a-107">*ppPointReps* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e770a-107">*ppPointReps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e770a-108">Type : **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e770a-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="e770a-109">Pointeur vers une mémoire tampon de maillage contenant les données de point du maillage.</span><span class="sxs-lookup"><span data-stu-id="e770a-109">Pointer to a mesh buffer containing the mesh's point rep data.</span></span> <span data-ttu-id="e770a-110">Consultez [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e770a-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e770a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e770a-111">Return value</span></span>

<span data-ttu-id="e770a-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e770a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e770a-113">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e770a-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e770a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e770a-114">Requirements</span></span>



| <span data-ttu-id="e770a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e770a-115">Requirement</span></span> | <span data-ttu-id="e770a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e770a-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e770a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e770a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e770a-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e770a-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e770a-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e770a-119">Library</span></span><br/> | <dl> <span data-ttu-id="e770a-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e770a-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e770a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e770a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e770a-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="e770a-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="e770a-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e770a-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




