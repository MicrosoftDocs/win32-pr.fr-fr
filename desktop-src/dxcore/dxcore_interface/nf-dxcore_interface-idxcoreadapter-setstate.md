---
title: IDXCoreAdapter::SetState
description: Définit l’état de l’élément spécifié sur l’adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8cbeacdb8c6020441b5dd74a9f9233a6c112b4f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510487"
---
# <a name="idxcoreadaptersetstate-method"></a><span data-ttu-id="693f4-103">IDXCoreAdapter :: SetState, méthode</span><span class="sxs-lookup"><span data-stu-id="693f4-103">IDXCoreAdapter::SetState method</span></span>

<span data-ttu-id="693f4-104">Définit l’état de l’élément spécifié sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="693f4-104">Sets the state of the specified item on the adapter.</span></span> <span data-ttu-id="693f4-105">Avant d’appeler **SetState** pour un type de propriété, appelez [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) pour confirmer que la définition du type d’État est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="693f4-105">Before calling **SetState** for a property type, call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="693f4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="693f4-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a><span data-ttu-id="693f4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="693f4-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="693f4-108">state</span><span class="sxs-lookup"><span data-stu-id="693f4-108">state</span></span>

<span data-ttu-id="693f4-109">Type : **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="693f4-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="693f4-110">Type d’élément d’État sur l’adaptateur dont vous souhaitez définir l’État.</span><span class="sxs-lookup"><span data-stu-id="693f4-110">The kind of state item on the adapter whose state you wish to set.</span></span> <span data-ttu-id="693f4-111">Consultez le tableau dans [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) pour plus d’informations sur chaque type d’état de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="693f4-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="693f4-112">inputStateDetailsSize</span><span class="sxs-lookup"><span data-stu-id="693f4-112">inputStateDetailsSize</span></span>

<span data-ttu-id="693f4-113">Type : **size_t**</span><span class="sxs-lookup"><span data-stu-id="693f4-113">Type: **size_t**</span></span>

<span data-ttu-id="693f4-114">Taille, en octets, de la mémoire tampon des détails de l’état d’entrée que vous pouvez également allouer et fournir dans *inputStateDetails*.</span><span class="sxs-lookup"><span data-stu-id="693f4-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="693f4-115">inputStateDetails [in]</span><span class="sxs-lookup"><span data-stu-id="693f4-115">inputStateDetails [in]</span></span>

<span data-ttu-id="693f4-116">Type : **void const \***</span><span class="sxs-lookup"><span data-stu-id="693f4-116">Type: **void const\***</span></span>

<span data-ttu-id="693f4-117">Pointeur facultatif vers une mémoire tampon de détails d’état d’entrée constante que vous allouez dans votre application, contenant toutes les informations relatives à votre demande requises pour le genre d’État que vous spécifiez dans *État*.</span><span class="sxs-lookup"><span data-stu-id="693f4-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="693f4-118">Consultez le tableau dans [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) pour plus d’informations sur les exigences en matière de mémoire tampon d’entrée pour un type d’État donné.</span><span class="sxs-lookup"><span data-stu-id="693f4-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="inputdatasize"></a><span data-ttu-id="693f4-119">inputDataSize</span><span class="sxs-lookup"><span data-stu-id="693f4-119">inputDataSize</span></span>

<span data-ttu-id="693f4-120">Type : **size_t**</span><span class="sxs-lookup"><span data-stu-id="693f4-120">Type: **size_t**</span></span>

<span data-ttu-id="693f4-121">Taille, en octets, de la mémoire tampon d’entrée que vous allouez et fournissez dans *inputData*.</span><span class="sxs-lookup"><span data-stu-id="693f4-121">The size, in bytes, of the input buffer that you allocate and provide in *inputData*.</span></span>

### <a name="inputdata-in"></a><span data-ttu-id="693f4-122">inputData [in]</span><span class="sxs-lookup"><span data-stu-id="693f4-122">inputData [in]</span></span>

<span data-ttu-id="693f4-123">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="693f4-123">Type: **void\***</span></span>

<span data-ttu-id="693f4-124">Pointeur vers une mémoire tampon d’entrée que vous allouez dans votre application, contenant les informations d’État à définir pour l’élément d’État dont vous spécifiez le type dans *État*.</span><span class="sxs-lookup"><span data-stu-id="693f4-124">A pointer to an input buffer that you allocate in your application, containing the state information to set for the state item whose kind you specify in *state*.</span></span> <span data-ttu-id="693f4-125">Consultez le tableau dans [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) pour plus d’informations sur la spécification de la mémoire tampon d’entrée pour un type d’État donné.</span><span class="sxs-lookup"><span data-stu-id="693f4-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the input buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="693f4-126">Retours</span><span class="sxs-lookup"><span data-stu-id="693f4-126">Returns</span></span>

<span data-ttu-id="693f4-127">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="693f4-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="693f4-128">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="693f4-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="693f4-129">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="693f4-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="693f4-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="693f4-130">Return value</span></span>|<span data-ttu-id="693f4-131">Description</span><span class="sxs-lookup"><span data-stu-id="693f4-131">Description</span></span>|
|-|-|
|<span data-ttu-id="693f4-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="693f4-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="693f4-133">L’état de l’adaptateur n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="693f4-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="693f4-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="693f4-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="693f4-135">Le genre d’état spécifié dans l' *État* n’est pas reconnu par ce système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="693f4-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="693f4-136">Appelez [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) pour confirmer que la définition du type d’État est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="693f4-136">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="693f4-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="693f4-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="693f4-138">Le genre d’état spécifié dans l' *État* n’est pas pris en charge par l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="693f4-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="693f4-139">Appelez [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) pour confirmer que la définition du type d’État est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="693f4-139">Call [IsSetStateSupported](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) to confirm that setting the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="693f4-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="693f4-140">E_INVALIDARG</span></span>|<span data-ttu-id="693f4-141">Une taille de mémoire tampon insuffisante est fournie pour *inputData* (ou pour *inputStateDetails* où un tampon de détails d’état d’entrée est nécessaire).</span><span class="sxs-lookup"><span data-stu-id="693f4-141">An insufficient buffer size is provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="693f4-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="693f4-142">E_POINTER</span></span>|<span data-ttu-id="693f4-143">`nullptr` a été fourni pour *inputData* (ou pour *inputStateDetails* où un tampon de détails d’état d’entrée est nécessaire).</span><span class="sxs-lookup"><span data-stu-id="693f4-143">`nullptr` was provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="see-also"></a><span data-ttu-id="693f4-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="693f4-144">See also</span></span>

<span data-ttu-id="693f4-145">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="693f4-145">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>