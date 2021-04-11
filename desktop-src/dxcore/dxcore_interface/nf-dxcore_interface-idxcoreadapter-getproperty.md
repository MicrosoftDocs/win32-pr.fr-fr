---
title: IDXCoreAdapter::GetProperty
description: Récupère la valeur de la propriété de l’adaptateur spécifiée.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c8a7f7b36fdb0128b4047335051823da07a074c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316260"
---
# <a name="idxcoreadaptergetproperty-method"></a><span data-ttu-id="e78d8-103">IDXCoreAdapter :: GetProperty, méthode</span><span class="sxs-lookup"><span data-stu-id="e78d8-103">IDXCoreAdapter::GetProperty method</span></span>

<span data-ttu-id="e78d8-104">Récupère la valeur de la propriété de l’adaptateur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e78d8-104">Retrieves the value of the specified adapter property.</span></span> <span data-ttu-id="e78d8-105">Avant d’appeler **GetProperty** pour un type de propriété, appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e78d8-105">Before calling **GetProperty** for a property type, call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span> <span data-ttu-id="e78d8-106">De même, avant d’appeler **GetProperty**, appelez [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) pour déterminer la taille nécessaire de la mémoire tampon dans laquelle la valeur de propriété doit être reçue.</span><span class="sxs-lookup"><span data-stu-id="e78d8-106">Also before calling **GetProperty**, call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the necessary size of the buffer in which to receive the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78d8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e78d8-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a><span data-ttu-id="e78d8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e78d8-108">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="e78d8-109">propriété</span><span class="sxs-lookup"><span data-stu-id="e78d8-109">property</span></span>

<span data-ttu-id="e78d8-110">Type : **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="e78d8-110">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="e78d8-111">Type de la propriété dont vous souhaitez récupérer la valeur.</span><span class="sxs-lookup"><span data-stu-id="e78d8-111">The type of the property whose value you wish to retrieve.</span></span> <span data-ttu-id="e78d8-112">Consultez le tableau dans [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) pour plus d’informations sur chaque propriété de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="e78d8-112">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

### <a name="buffersize"></a><span data-ttu-id="e78d8-113">Tampon</span><span class="sxs-lookup"><span data-stu-id="e78d8-113">bufferSize</span></span>

<span data-ttu-id="e78d8-114">Type : **size_t**</span><span class="sxs-lookup"><span data-stu-id="e78d8-114">Type: **size_t**</span></span>

<span data-ttu-id="e78d8-115">Taille, en octets, de la mémoire tampon de sortie que vous allouez et fournissez dans *PropertyData*.</span><span class="sxs-lookup"><span data-stu-id="e78d8-115">The size, in bytes, of the output buffer that you allocate and provide in *propertyData*.</span></span>

### <a name="propertydata-out"></a><span data-ttu-id="e78d8-116">propertyData [out]</span><span class="sxs-lookup"><span data-stu-id="e78d8-116">propertyData [out]</span></span>

<span data-ttu-id="e78d8-117">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="e78d8-117">Type: **void\***</span></span>

<span data-ttu-id="e78d8-118">Pointeur vers une mémoire tampon de sortie que vous allouez dans votre application, et que la fonction remplit.</span><span class="sxs-lookup"><span data-stu-id="e78d8-118">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="e78d8-119">Appelez [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) pour déterminer la taille de la mémoire tampon *PropertyData* pour une propriété d’adaptateur donnée.</span><span class="sxs-lookup"><span data-stu-id="e78d8-119">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="e78d8-120">Retours</span><span class="sxs-lookup"><span data-stu-id="e78d8-120">Returns</span></span>

<span data-ttu-id="e78d8-121">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="e78d8-121">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="e78d8-122">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="e78d8-122">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="e78d8-123">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e78d8-123">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="e78d8-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e78d8-124">Return value</span></span>|<span data-ttu-id="e78d8-125">Description</span><span class="sxs-lookup"><span data-stu-id="e78d8-125">Description</span></span>|
|-|-|
|<span data-ttu-id="e78d8-126">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="e78d8-126">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="e78d8-127">Le type de propriété spécifié dans la *propriété* n’est pas reconnu par ce système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e78d8-127">The property type specified in *property* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="e78d8-128">Appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e78d8-128">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="e78d8-129">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="e78d8-129">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="e78d8-130">Le type de propriété spécifié dans la *propriété* n’est pas pris en charge par l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="e78d8-130">The property type specified in *property* is not supported by the adapter.</span></span> <span data-ttu-id="e78d8-131">Appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e78d8-131">Call [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) to confirm that the property type is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="e78d8-132">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e78d8-132">E_INVALIDARG</span></span>|<span data-ttu-id="e78d8-133">Une taille de mémoire tampon insuffisante est fournie dans *PropertyData*.</span><span class="sxs-lookup"><span data-stu-id="e78d8-133">An insufficient buffer size is provided in *propertyData*.</span></span> <span data-ttu-id="e78d8-134">Appelez [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) pour déterminer la taille de la mémoire tampon *PropertyData* pour une propriété d’adaptateur donnée.</span><span class="sxs-lookup"><span data-stu-id="e78d8-134">Call [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) to determine the size that the *propertyData* buffer should be for a given adapter property.</span></span>|
|<span data-ttu-id="e78d8-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="e78d8-135">E_POINTER</span></span>|<span data-ttu-id="e78d8-136">`nullptr` a été fourni pour *PropertyData*.</span><span class="sxs-lookup"><span data-stu-id="e78d8-136">`nullptr` was provided for *propertyData*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e78d8-137">Notes</span><span class="sxs-lookup"><span data-stu-id="e78d8-137">Remarks</span></span>

<span data-ttu-id="e78d8-138">Vous pouvez appeler **GetProperty** sur un adaptateur qui n’est plus valide &mdash; . la fonction n’échouera pas à la suite de cela.</span><span class="sxs-lookup"><span data-stu-id="e78d8-138">You can call **GetProperty** on an adapter that's no longer valid&mdash;the function won't fail as a result of that.</span></span> <span data-ttu-id="e78d8-139">Cette fonction met à zéro la mémoire tampon *PropertyData* avant de la remplir.</span><span class="sxs-lookup"><span data-stu-id="e78d8-139">This function zeros out the *propertyData* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="e78d8-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e78d8-140">See also</span></span>

<span data-ttu-id="e78d8-141">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="e78d8-141">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>