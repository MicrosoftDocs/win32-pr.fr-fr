---
description: 'Accédez à la mémoire tampon de vertex du maillage une fois qu’elle a été validée sur l’appareil avec ID3DX10Mesh :: CommitToDevice. Cela diffère de ID3DX10Mesh :: GetVertexBuffer, qui retourne la mémoire tampon de vertex avant qu’elle n’ait été validée sur l’appareil.'
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'ID3DX10Mesh :: GetDeviceVertexBuffer, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9943050d174acb4e8f8e676f56a95cfdcde88f5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545298"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a><span data-ttu-id="dd03b-104">ID3DX10Mesh :: GetDeviceVertexBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="dd03b-104">ID3DX10Mesh::GetDeviceVertexBuffer method</span></span>

<span data-ttu-id="dd03b-105">Accédez à la mémoire tampon de vertex du maillage une fois qu’elle a été validée sur l’appareil avec [**ID3DX10Mesh :: CommitToDevice**](id3dx10mesh-committodevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd03b-105">Access the mesh's vertex buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="dd03b-106">Cela diffère de [**ID3DX10Mesh :: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), qui retourne la mémoire tampon de vertex avant qu’elle n’ait été validée sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd03b-106">This is different from [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), which returns the vertex buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd03b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd03b-107">Syntax</span></span>


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="dd03b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd03b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd03b-109">*iBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd03b-109">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd03b-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd03b-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dd03b-111">Index identifiant la mémoire tampon de vertex à laquelle accéder.</span><span class="sxs-lookup"><span data-stu-id="dd03b-111">An index identifying which vertex buffer to access.</span></span>

</dd> <dt>

<span data-ttu-id="dd03b-112">*ppVertexBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dd03b-112">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd03b-113">Type : **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="dd03b-113">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="dd03b-114">Mémoire tampon de vertex une fois qu’elle a été validée sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="dd03b-114">The vertex buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd03b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd03b-115">Return value</span></span>

<span data-ttu-id="dd03b-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd03b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd03b-117">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="dd03b-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd03b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd03b-118">Requirements</span></span>



| <span data-ttu-id="dd03b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd03b-119">Requirement</span></span> | <span data-ttu-id="dd03b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd03b-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd03b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd03b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dd03b-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd03b-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd03b-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd03b-123">Library</span></span><br/> | <dl> <span data-ttu-id="dd03b-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd03b-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd03b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd03b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd03b-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="dd03b-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="dd03b-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="dd03b-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
