---
description: 'Supprime les données de maillage de l’appareil qui a été validé sur l’appareil (avec ID3DX10Mesh :: CommitToDevice).'
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: ID3DX10Mesh ::D méthode iscard (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537256"
---
# <a name="id3dx10meshdiscard-method"></a><span data-ttu-id="37adf-103">ID3DX10Mesh ::D méthode iscard</span><span class="sxs-lookup"><span data-stu-id="37adf-103">ID3DX10Mesh::Discard method</span></span>

<span data-ttu-id="37adf-104">Supprime les données de maillage de l’appareil qui a été validé sur l’appareil (avec [**ID3DX10Mesh :: CommitToDevice**](id3dx10mesh-committodevice.md)).</span><span class="sxs-lookup"><span data-stu-id="37adf-104">Removes mesh data from the device that has been committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="37adf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37adf-105">Syntax</span></span>


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a><span data-ttu-id="37adf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37adf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37adf-107">*dwDiscard* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37adf-107">*dwDiscard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37adf-108">Type : **[ **d3dx10 \_ Mesh \_ ignore \_ Flags**](d3dx10-mesh-discard-flags.md)**</span><span class="sxs-lookup"><span data-stu-id="37adf-108">Type: **[**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md)**</span></span>

<span data-ttu-id="37adf-109">Spécifie les éléments de données de maillage à ignorer de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="37adf-109">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="37adf-110">Consultez [**\_ indicateurs d3dx10 \_ Mesh \_ ignore**](d3dx10-mesh-discard-flags.md).</span><span class="sxs-lookup"><span data-stu-id="37adf-110">See [**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37adf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37adf-111">Return value</span></span>

<span data-ttu-id="37adf-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="37adf-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="37adf-113">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="37adf-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37adf-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37adf-114">Requirements</span></span>



| <span data-ttu-id="37adf-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37adf-115">Requirement</span></span> | <span data-ttu-id="37adf-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="37adf-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37adf-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="37adf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="37adf-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="37adf-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="37adf-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="37adf-119">Library</span></span><br/> | <dl> <span data-ttu-id="37adf-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37adf-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37adf-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37adf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37adf-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="37adf-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="37adf-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="37adf-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




