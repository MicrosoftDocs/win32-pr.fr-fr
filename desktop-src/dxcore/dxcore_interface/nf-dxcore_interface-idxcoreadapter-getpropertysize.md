---
title: IDXCoreAdapter::GetPropertySize
description: Pour une propriété de l’adaptateur spécifiée, récupère la taille de la mémoire tampon, en octets, requise pour un appel à [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509039"
---
# <a name="idxcoreadaptergetpropertysize-method"></a><span data-ttu-id="368d7-103">IDXCoreAdapter :: GetPropertySize, méthode</span><span class="sxs-lookup"><span data-stu-id="368d7-103">IDXCoreAdapter::GetPropertySize method</span></span>

<span data-ttu-id="368d7-104">Pour une propriété de l’adaptateur spécifiée, récupère la taille de la mémoire tampon, en octets, requise pour un appel à [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="368d7-104">For a specified adapter property, retrieves the size of buffer, in bytes, that is required for a call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span> <span data-ttu-id="368d7-105">Avant d’appeler **GetPropertySize** pour un type de propriété, appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="368d7-105">Before calling **GetPropertySize** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="368d7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="368d7-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a><span data-ttu-id="368d7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="368d7-107">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="368d7-108">propriété</span><span class="sxs-lookup"><span data-stu-id="368d7-108">property</span></span>

<span data-ttu-id="368d7-109">Type : **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="368d7-109">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="368d7-110">Type de la propriété dont vous souhaitez récupérer la taille, en octets.</span><span class="sxs-lookup"><span data-stu-id="368d7-110">The type of the property whose size, in bytes, you wish to retrieve.</span></span>

### <a name="buffersize-out"></a><span data-ttu-id="368d7-111">bufferSize [out]</span><span class="sxs-lookup"><span data-stu-id="368d7-111">bufferSize [out]</span></span>

<span data-ttu-id="368d7-112">Type : **size_t \***</span><span class="sxs-lookup"><span data-stu-id="368d7-112">Type: **size_t\***</span></span>

<span data-ttu-id="368d7-113">Pointeur vers une valeur **size_t** .</span><span class="sxs-lookup"><span data-stu-id="368d7-113">A pointer to a **size_t** value.</span></span> <span data-ttu-id="368d7-114">La fonction déréférence le pointeur et affecte à la valeur la taille, en octets, de la mémoire tampon de sortie que vous devez allouer et passer comme argument *PropertyData* dans votre appel à [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="368d7-114">The function dereferences the pointer and sets the value to the size, in bytes, of the output buffer that you should allocate and pass as the *propertyData* argument in your call to [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

## <a name="returns"></a><span data-ttu-id="368d7-115">Retours</span><span class="sxs-lookup"><span data-stu-id="368d7-115">Returns</span></span>

<span data-ttu-id="368d7-116">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="368d7-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="368d7-117">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="368d7-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="368d7-118">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="368d7-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="368d7-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="368d7-119">Return value</span></span>|<span data-ttu-id="368d7-120">Description</span><span class="sxs-lookup"><span data-stu-id="368d7-120">Description</span></span>|
|-|-|
|<span data-ttu-id="368d7-121">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="368d7-121">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="368d7-122">Le type de propriété spécifié dans la *propriété* n’est pas reconnu par ce système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="368d7-122">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="368d7-123">Appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="368d7-123">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="368d7-124">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="368d7-124">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="368d7-125">Le type de propriété spécifié dans la *propriété* n’est pas pris en charge par l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="368d7-125">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="368d7-126">Appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="368d7-126">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="368d7-127">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="368d7-127">E_POINTER</span></span>|<span data-ttu-id="368d7-128">`nullptr` a été fourni pour *bufferSize*.</span><span class="sxs-lookup"><span data-stu-id="368d7-128">`nullptr` was provided for *bufferSize*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="368d7-129">Notes</span><span class="sxs-lookup"><span data-stu-id="368d7-129">Remarks</span></span>

<span data-ttu-id="368d7-130">Vous pouvez appeler **GetPropertySize** sur un adaptateur qui n’est plus valide &mdash; . la fonction ne peut pas échouer.</span><span class="sxs-lookup"><span data-stu-id="368d7-130">You can call **GetPropertySize** on an adapter that's no longer valid&mdash;the function won't fail.</span></span>

## <a name="see-also"></a><span data-ttu-id="368d7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="368d7-131">See also</span></span>

<span data-ttu-id="368d7-132">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="368d7-132">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>