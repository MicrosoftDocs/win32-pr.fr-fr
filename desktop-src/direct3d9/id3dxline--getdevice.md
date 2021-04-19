---
description: Récupère le périphérique Direct3D associé à l’objet Line.
ms.assetid: 42459668-aa18-478d-82d9-b8b25dc4a898
title: 'ID3DXLine :: GetDevice, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a97edf37d14edce4982d62d76f9429091ad491ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522767"
---
# <a name="id3dxlinegetdevice-method"></a><span data-ttu-id="fb8f6-103">ID3DXLine :: GetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="fb8f6-103">ID3DXLine::GetDevice method</span></span>

<span data-ttu-id="fb8f6-104">Récupère le périphérique Direct3D associé à l’objet Line.</span><span class="sxs-lookup"><span data-stu-id="fb8f6-104">Retrieves the Direct3D device associated with the line object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb8f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb8f6-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="fb8f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb8f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb8f6-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="fb8f6-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fb8f6-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="fb8f6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="fb8f6-109">Adresse d’un pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’objet appareil Direct3D associé à l’objet Line.</span><span class="sxs-lookup"><span data-stu-id="fb8f6-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the line object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb8f6-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb8f6-110">Return value</span></span>

<span data-ttu-id="fb8f6-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb8f6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb8f6-112">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb8f6-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb8f6-113">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="fb8f6-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb8f6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb8f6-114">Requirements</span></span>



| <span data-ttu-id="fb8f6-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb8f6-115">Requirement</span></span> | <span data-ttu-id="fb8f6-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb8f6-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb8f6-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb8f6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fb8f6-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb8f6-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="fb8f6-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fb8f6-119">Library</span></span><br/> | <dl> <span data-ttu-id="fb8f6-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb8f6-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb8f6-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb8f6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb8f6-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="fb8f6-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
