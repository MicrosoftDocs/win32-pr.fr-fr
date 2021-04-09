---
description: Obtient une description de la table constante.
ms.assetid: 3a7396c6-3a3e-44c2-96b7-60339015b376
title: 'ID3DXConstantTable :: GetDesc, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71eeb951ec73fbeb9942f52e30ab9ad59e374ee7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870118"
---
# <a name="id3dxconstanttablegetdesc-method"></a><span data-ttu-id="8c82c-103">ID3DXConstantTable :: GetDesc, méthode</span><span class="sxs-lookup"><span data-stu-id="8c82c-103">ID3DXConstantTable::GetDesc method</span></span>

<span data-ttu-id="8c82c-104">Obtient une description de la table constante.</span><span class="sxs-lookup"><span data-stu-id="8c82c-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c82c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c82c-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="8c82c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c82c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c82c-107">*pDesc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c82c-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c82c-108">Type : **[ **D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c82c-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="8c82c-109">Description de la table constante.</span><span class="sxs-lookup"><span data-stu-id="8c82c-109">Description of the constant table.</span></span> <span data-ttu-id="8c82c-110">Consultez [**D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="8c82c-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c82c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c82c-111">Return value</span></span>

<span data-ttu-id="8c82c-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8c82c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8c82c-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8c82c-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8c82c-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="8c82c-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c82c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c82c-115">Requirements</span></span>



| <span data-ttu-id="8c82c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c82c-116">Requirement</span></span> | <span data-ttu-id="8c82c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c82c-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c82c-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c82c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8c82c-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c82c-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8c82c-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c82c-120">Library</span></span><br/> | <dl> <span data-ttu-id="8c82c-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c82c-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8c82c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c82c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c82c-123">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="8c82c-123">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="8c82c-124">**ID3DXConstantTable::GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="8c82c-124">**ID3DXConstantTable::GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)
</dt> </dl>

 

 




