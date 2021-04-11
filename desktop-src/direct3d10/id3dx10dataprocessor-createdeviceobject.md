---
description: Créez un objet d’appareil.
ms.assetid: 5b9b00de-c744-43c7-b383-1d3358c80741
title: 'ID3DX10DataProcessor :: CreateDeviceObject, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.CreateDeviceObject
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1ed362f992ca2b9d3ce6e561e08e5fe7fd0bdbe3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211785"
---
# <a name="id3dx10dataprocessorcreatedeviceobject-method"></a><span data-ttu-id="41923-103">ID3DX10DataProcessor :: CreateDeviceObject, méthode</span><span class="sxs-lookup"><span data-stu-id="41923-103">ID3DX10DataProcessor::CreateDeviceObject method</span></span>

<span data-ttu-id="41923-104">Créez un objet d’appareil.</span><span class="sxs-lookup"><span data-stu-id="41923-104">Create a device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="41923-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41923-105">Syntax</span></span>


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a><span data-ttu-id="41923-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41923-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41923-107">*ppDataObject* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="41923-107">*ppDataObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41923-108">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="41923-108">Type: **void\*\***</span></span>

<span data-ttu-id="41923-109">Adresse d’un pointeur vers l’objet appareil créé.</span><span class="sxs-lookup"><span data-stu-id="41923-109">Address of a pointer to the created device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41923-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41923-110">Return value</span></span>

<span data-ttu-id="41923-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41923-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41923-112">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="41923-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41923-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41923-113">Requirements</span></span>



| <span data-ttu-id="41923-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41923-114">Requirement</span></span> | <span data-ttu-id="41923-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="41923-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41923-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="41923-116">Header</span></span><br/>  | <dl> <span data-ttu-id="41923-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="41923-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="41923-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41923-118">Library</span></span><br/> | <dl> <span data-ttu-id="41923-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41923-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41923-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41923-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41923-121">ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="41923-121">ID3DX10DataProcessor</span></span>](id3dx10dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="41923-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="41923-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




