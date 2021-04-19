---
description: Définissez les données d’index du maillage.
ms.assetid: f3e7e166-94b5-45f6-9d43-8d7e32b7b523
title: 'ID3DX10Mesh :: SetIndexData, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetIndexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f561a4109fbab2163b2ec51e95b45a618da5b6d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522973"
---
# <a name="id3dx10meshsetindexdata-method"></a><span data-ttu-id="048a1-103">ID3DX10Mesh :: SetIndexData, méthode</span><span class="sxs-lookup"><span data-stu-id="048a1-103">ID3DX10Mesh::SetIndexData method</span></span>

<span data-ttu-id="048a1-104">Définissez les données d’index du maillage.</span><span class="sxs-lookup"><span data-stu-id="048a1-104">Set the mesh's index data.</span></span>

## <a name="syntax"></a><span data-ttu-id="048a1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="048a1-105">Syntax</span></span>


```C++
HRESULT SetIndexData(
  [in] const void *pData,
  [in]       UINT cIndices
);
```



## <a name="parameters"></a><span data-ttu-id="048a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="048a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="048a1-107">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="048a1-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="048a1-108">Type : **const void \***</span><span class="sxs-lookup"><span data-stu-id="048a1-108">Type: **const void\***</span></span>

<span data-ttu-id="048a1-109">Données d’index.</span><span class="sxs-lookup"><span data-stu-id="048a1-109">The index data.</span></span>

</dd> <dt>

<span data-ttu-id="048a1-110">*cIndices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="048a1-110">*cIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="048a1-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="048a1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="048a1-112">Nombre d’index dans pData.</span><span class="sxs-lookup"><span data-stu-id="048a1-112">The number of indices in pData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="048a1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="048a1-113">Return value</span></span>

<span data-ttu-id="048a1-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="048a1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="048a1-115">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="048a1-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="048a1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="048a1-116">Requirements</span></span>



| <span data-ttu-id="048a1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="048a1-117">Requirement</span></span> | <span data-ttu-id="048a1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="048a1-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="048a1-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="048a1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="048a1-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="048a1-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="048a1-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="048a1-121">Library</span></span><br/> | <dl> <span data-ttu-id="048a1-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="048a1-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="048a1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="048a1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="048a1-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="048a1-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="048a1-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="048a1-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
