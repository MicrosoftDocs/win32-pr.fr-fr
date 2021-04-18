---
description: Supprime toutes les ressources de l’appareil en affectant à leurs pointeurs la valeur NULL. Cela doit être appelé lors de l’arrêt de votre application. Cela permet de s’assurer que, lorsque l’un d’eux libère toutes ses ressources, aucune d’entre elles n’est liée à l’appareil.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: D3DX10UnsetAllDeviceObjects, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d3a113be935f77dbd62b2f3fac4c16c7cac9881
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522594"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a><span data-ttu-id="7f8c7-105">D3DX10UnsetAllDeviceObjects fonction)</span><span class="sxs-lookup"><span data-stu-id="7f8c7-105">D3DX10UnsetAllDeviceObjects function</span></span>

<span data-ttu-id="7f8c7-106">Supprime toutes les ressources de l’appareil en affectant à leurs pointeurs la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-106">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="7f8c7-107">Cela doit être appelé lors de l’arrêt de votre application.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-107">This should be called during shutdown of your application.</span></span> <span data-ttu-id="7f8c7-108">Cela permet de s’assurer que, lorsque l’un d’eux libère toutes ses ressources, aucune d’entre elles n’est liée à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-108">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f8c7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f8c7-109">Syntax</span></span>


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="7f8c7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f8c7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f8c7-111">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f8c7-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f8c7-112">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="7f8c7-112">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="7f8c7-113">Pointeur vers l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7f8c7-113">Pointer to the device.</span></span> <span data-ttu-id="7f8c7-114">Voir [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span><span class="sxs-lookup"><span data-stu-id="7f8c7-114">See [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f8c7-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f8c7-115">Return value</span></span>

<span data-ttu-id="7f8c7-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f8c7-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f8c7-117">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7f8c7-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f8c7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f8c7-118">Requirements</span></span>



| <span data-ttu-id="7f8c7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f8c7-119">Requirement</span></span> | <span data-ttu-id="7f8c7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f8c7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f8c7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f8c7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7f8c7-122"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f8c7-122"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="7f8c7-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7f8c7-123">Library</span></span><br/> | <dl> <span data-ttu-id="7f8c7-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f8c7-124"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7f8c7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f8c7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f8c7-126">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="7f8c7-126">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




