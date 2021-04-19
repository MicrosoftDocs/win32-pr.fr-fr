---
description: 'Accédez à la mémoire tampon d’index du maillage une fois qu’elle a été validée sur l’appareil avec ID3DX10Mesh :: CommitToDevice. Cela diffère de ID3DX10Mesh :: GetIndexBuffer, qui retourne la mémoire tampon d’index avant qu’elle ait été validée sur l’appareil.'
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'ID3DX10Mesh :: GetDeviceIndexBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537270"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a><span data-ttu-id="5f8ad-104">ID3DX10Mesh :: GetDeviceIndexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="5f8ad-104">ID3DX10Mesh::GetDeviceIndexBuffer method</span></span>

<span data-ttu-id="5f8ad-105">Accédez à la mémoire tampon d’index du maillage une fois qu’elle a été validée sur l’appareil avec [**ID3DX10Mesh :: CommitToDevice**](id3dx10mesh-committodevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f8ad-105">Access the mesh's index buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="5f8ad-106">Cela diffère de [**ID3DX10Mesh :: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), qui retourne la mémoire tampon d’index avant qu’elle ait été validée sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-106">This is different from [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), which returns the index buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8ad-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f8ad-107">Syntax</span></span>


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="5f8ad-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f8ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f8ad-109">*ppIndexBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5f8ad-109">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f8ad-110">Type : **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="5f8ad-110">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="5f8ad-111">Mémoire tampon d’index une fois qu’elle a été validée sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-111">The index buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f8ad-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f8ad-112">Return value</span></span>

<span data-ttu-id="5f8ad-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5f8ad-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5f8ad-114">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5f8ad-114">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5f8ad-115">Notes</span><span class="sxs-lookup"><span data-stu-id="5f8ad-115">Remarks</span></span>

<span data-ttu-id="5f8ad-116">Si la mémoire tampon d’index du maillage n’a pas déjà été validée sur l’appareil, cette API valide automatiquement le tampon d’index avant de retourner un pointeur vers la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5f8ad-116">If the mesh's index buffer has not already been committed to the device, this API will automatically commit the index buffer before it returns a pointer to the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f8ad-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f8ad-117">Requirements</span></span>



| <span data-ttu-id="5f8ad-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f8ad-118">Requirement</span></span> | <span data-ttu-id="5f8ad-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f8ad-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8ad-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f8ad-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5f8ad-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f8ad-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f8ad-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f8ad-122">Library</span></span><br/> | <dl> <span data-ttu-id="5f8ad-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f8ad-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f8ad-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f8ad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8ad-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="5f8ad-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="5f8ad-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="5f8ad-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




