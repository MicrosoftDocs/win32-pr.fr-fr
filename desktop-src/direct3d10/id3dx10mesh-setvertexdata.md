---
description: Définissez les données de vertex dans l’une des mémoires tampons de vertex du maillage.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'ID3DX10Mesh :: SetVertexData, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 68d54c6868e44517d42e0b53159f7a23ef45a05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542182"
---
# <a name="id3dx10meshsetvertexdata-method"></a><span data-ttu-id="d4fb7-103">ID3DX10Mesh :: SetVertexData, méthode</span><span class="sxs-lookup"><span data-stu-id="d4fb7-103">ID3DX10Mesh::SetVertexData method</span></span>

<span data-ttu-id="d4fb7-104">Définissez les données de vertex dans l’une des mémoires tampons de vertex du maillage.</span><span class="sxs-lookup"><span data-stu-id="d4fb7-104">Set vertex data into one of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4fb7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4fb7-105">Syntax</span></span>


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a><span data-ttu-id="d4fb7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4fb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4fb7-107">*iBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4fb7-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4fb7-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4fb7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4fb7-109">Mémoire tampon de vertex à remplir avec pData.</span><span class="sxs-lookup"><span data-stu-id="d4fb7-109">The vertex buffer to be filled with pData.</span></span>

</dd> <dt>

<span data-ttu-id="d4fb7-110">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4fb7-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4fb7-111">Type : **const void \***</span><span class="sxs-lookup"><span data-stu-id="d4fb7-111">Type: **const void\***</span></span>

<span data-ttu-id="d4fb7-112">Données de vertex à définir.</span><span class="sxs-lookup"><span data-stu-id="d4fb7-112">The vertex data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4fb7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4fb7-113">Return value</span></span>

<span data-ttu-id="d4fb7-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4fb7-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4fb7-115">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d4fb7-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4fb7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4fb7-116">Requirements</span></span>



| <span data-ttu-id="d4fb7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4fb7-117">Requirement</span></span> | <span data-ttu-id="d4fb7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4fb7-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4fb7-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4fb7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d4fb7-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4fb7-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4fb7-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4fb7-121">Library</span></span><br/> | <dl> <span data-ttu-id="d4fb7-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4fb7-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4fb7-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4fb7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4fb7-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="d4fb7-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="d4fb7-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d4fb7-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
