---
title: Méthode ID3DX11DataProcessor CreateDeviceObject (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Crée un objet appareil.'
ms.assetid: 797d216b-2f54-4d24-aa97-04be0c71f909
keywords:
- Méthode CreateDeviceObject Direct3D 11
- Méthode CreateDeviceObject Direct3D 11, interface ID3DX11DataProcessor
- Interface ID3DX11DataProcessor Direct3D 11, méthode CreateDeviceObject
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.CreateDeviceObject
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ff178cec1830d1b0213af23a2a70654416d35e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323390"
---
# <a name="id3dx11dataprocessorcreatedeviceobject-method"></a><span data-ttu-id="7d3ec-107">ID3DX11DataProcessor :: CreateDeviceObject, méthode</span><span class="sxs-lookup"><span data-stu-id="7d3ec-107">ID3DX11DataProcessor::CreateDeviceObject method</span></span>

> [!Note]  
> <span data-ttu-id="7d3ec-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="7d3ec-109">Crée un objet appareil.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-109">Creates a device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d3ec-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d3ec-110">Syntax</span></span>


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a><span data-ttu-id="7d3ec-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d3ec-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d3ec-112">*ppDataObject* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-112">*ppDataObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-113">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="7d3ec-113">Type: **void\*\***</span></span>

<span data-ttu-id="7d3ec-114">Adresse d’un pointeur vers l’objet appareil créé.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-114">Address of a pointer to the created device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d3ec-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d3ec-115">Return value</span></span>

<span data-ttu-id="7d3ec-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7d3ec-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7d3ec-117">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7d3ec-117">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d3ec-118">Notes</span><span class="sxs-lookup"><span data-stu-id="7d3ec-118">Remarks</span></span>

<span data-ttu-id="7d3ec-119">Cette méthode est utilisée par une [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="7d3ec-119">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d3ec-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7d3ec-120">Requirements</span></span>



| <span data-ttu-id="7d3ec-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d3ec-121">Requirement</span></span> | <span data-ttu-id="7d3ec-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d3ec-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d3ec-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d3ec-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7d3ec-124"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d3ec-124"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="7d3ec-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7d3ec-125">Library</span></span><br/> | <dl> <span data-ttu-id="7d3ec-126"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d3ec-126"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7d3ec-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d3ec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d3ec-128">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="7d3ec-128">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="7d3ec-129">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="7d3ec-129">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





