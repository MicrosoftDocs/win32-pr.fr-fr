---
description: Définissez les données d’attribut du maillage.
ms.assetid: bcf7b1b3-b923-400a-8d12-5094f3844d8f
title: 'ID3DX10Mesh :: SetAttributeData, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19d69f8747196d7b25c85cb04fb173adef193098
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211858"
---
# <a name="id3dx10meshsetattributedata-method"></a><span data-ttu-id="96dce-103">ID3DX10Mesh :: SetAttributeData, méthode</span><span class="sxs-lookup"><span data-stu-id="96dce-103">ID3DX10Mesh::SetAttributeData method</span></span>

<span data-ttu-id="96dce-104">Définissez les données d’attribut du maillage.</span><span class="sxs-lookup"><span data-stu-id="96dce-104">Set the mesh's attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="96dce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96dce-105">Syntax</span></span>


```C++
HRESULT SetAttributeData(
  [in] const UINT *pData
);
```



## <a name="parameters"></a><span data-ttu-id="96dce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96dce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96dce-107">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96dce-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96dce-108">Type : **const [**uint**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="96dce-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="96dce-109">Données d’attribut à définir.</span><span class="sxs-lookup"><span data-stu-id="96dce-109">The attribute data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96dce-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96dce-110">Return value</span></span>

<span data-ttu-id="96dce-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96dce-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96dce-112">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="96dce-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="96dce-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96dce-113">Requirements</span></span>



| <span data-ttu-id="96dce-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96dce-114">Requirement</span></span> | <span data-ttu-id="96dce-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="96dce-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96dce-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="96dce-116">Header</span></span><br/>  | <dl> <span data-ttu-id="96dce-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="96dce-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="96dce-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="96dce-118">Library</span></span><br/> | <dl> <span data-ttu-id="96dce-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96dce-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96dce-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96dce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96dce-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="96dce-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="96dce-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="96dce-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
