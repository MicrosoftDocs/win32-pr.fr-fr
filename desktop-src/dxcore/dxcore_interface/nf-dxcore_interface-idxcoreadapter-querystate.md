---
title: IDXCoreAdapter::QueryState
description: Récupère l’état actuel de l’élément spécifié sur l’adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511091"
---
# <a name="idxcoreadapterquerystate-method"></a><span data-ttu-id="1a721-103">IDXCoreAdapter :: QueryState, méthode</span><span class="sxs-lookup"><span data-stu-id="1a721-103">IDXCoreAdapter::QueryState method</span></span>

<span data-ttu-id="1a721-104">Récupère l’état actuel de l’élément spécifié sur l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1a721-104">Retrieves the current state of the specified item on the adapter.</span></span> <span data-ttu-id="1a721-105">Avant d’appeler **QueryState** pour un type de propriété, appelez [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) pour confirmer que l’interrogation du genre d’État est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1a721-105">Before calling **QueryState** for a property type, call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a721-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a721-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a><span data-ttu-id="1a721-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a721-107">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="1a721-108">state</span><span class="sxs-lookup"><span data-stu-id="1a721-108">state</span></span>

<span data-ttu-id="1a721-109">Type : **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="1a721-109">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="1a721-110">Type d’élément d’État sur l’adaptateur dont vous souhaitez récupérer l’État.</span><span class="sxs-lookup"><span data-stu-id="1a721-110">The kind of state item on the adapter whose state you wish to retrieve.</span></span> <span data-ttu-id="1a721-111">Consultez le tableau dans [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) pour plus d’informations sur chaque type d’état de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1a721-111">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

### <a name="inputstatedetailssize"></a><span data-ttu-id="1a721-112">inputStateDetailsSize</span><span class="sxs-lookup"><span data-stu-id="1a721-112">inputStateDetailsSize</span></span>

<span data-ttu-id="1a721-113">Type : **size_t**</span><span class="sxs-lookup"><span data-stu-id="1a721-113">Type: **size_t**</span></span>

<span data-ttu-id="1a721-114">Taille, en octets, de la mémoire tampon des détails de l’état d’entrée que vous pouvez également allouer et fournir dans *inputStateDetails*.</span><span class="sxs-lookup"><span data-stu-id="1a721-114">The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.</span></span>

### <a name="inputstatedetails-in"></a><span data-ttu-id="1a721-115">inputStateDetails [in]</span><span class="sxs-lookup"><span data-stu-id="1a721-115">inputStateDetails [in]</span></span>

<span data-ttu-id="1a721-116">Type : **void const \***</span><span class="sxs-lookup"><span data-stu-id="1a721-116">Type: **void const\***</span></span>

<span data-ttu-id="1a721-117">Pointeur facultatif vers une mémoire tampon de détails d’état d’entrée constante que vous allouez dans votre application, contenant toutes les informations relatives à votre demande requises pour le genre d’État que vous spécifiez dans *État*.</span><span class="sxs-lookup"><span data-stu-id="1a721-117">An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*.</span></span> <span data-ttu-id="1a721-118">Consultez le tableau dans [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) pour plus d’informations sur les exigences en matière de mémoire tampon d’entrée pour un type d’État donné.</span><span class="sxs-lookup"><span data-stu-id="1a721-118">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about any input buffer requirement for a given state kind.</span></span>

### <a name="outputbuffersize"></a><span data-ttu-id="1a721-119">outputBufferSize</span><span class="sxs-lookup"><span data-stu-id="1a721-119">outputBufferSize</span></span>

<span data-ttu-id="1a721-120">Type : **size_t**</span><span class="sxs-lookup"><span data-stu-id="1a721-120">Type: **size_t**</span></span>

<span data-ttu-id="1a721-121">Taille, en octets, de la mémoire tampon de sortie que vous allouez et fournissez dans *OUTPUTBUFFER*.</span><span class="sxs-lookup"><span data-stu-id="1a721-121">The size, in bytes, of the output buffer that you allocate and provide in *outputBuffer*.</span></span>

### <a name="outputbuffer-out"></a><span data-ttu-id="1a721-122">outputBuffer [out]</span><span class="sxs-lookup"><span data-stu-id="1a721-122">outputBuffer [out]</span></span>

<span data-ttu-id="1a721-123">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="1a721-123">Type: **void\***</span></span>

<span data-ttu-id="1a721-124">Pointeur vers une mémoire tampon de sortie que vous allouez dans votre application, et que la fonction remplit.</span><span class="sxs-lookup"><span data-stu-id="1a721-124">A pointer to an output buffer that you allocate in your application, and that the function fills in.</span></span> <span data-ttu-id="1a721-125">Consultez le tableau dans [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) pour plus d’informations sur la spécification de la mémoire tampon de sortie pour un type d’État donné.</span><span class="sxs-lookup"><span data-stu-id="1a721-125">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about the output buffer requirement for a given state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="1a721-126">Retours</span><span class="sxs-lookup"><span data-stu-id="1a721-126">Returns</span></span>

<span data-ttu-id="1a721-127">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="1a721-127">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="1a721-128">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="1a721-128">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="1a721-129">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="1a721-129">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="1a721-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a721-130">Return value</span></span>|<span data-ttu-id="1a721-131">Description</span><span class="sxs-lookup"><span data-stu-id="1a721-131">Description</span></span>|
|-|-|
|<span data-ttu-id="1a721-132">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="1a721-132">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="1a721-133">L’état de l’adaptateur n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="1a721-133">The adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="1a721-134">DXGI_ERROR_INVALID_CALL</span><span class="sxs-lookup"><span data-stu-id="1a721-134">DXGI_ERROR_INVALID_CALL</span></span>|<span data-ttu-id="1a721-135">Le genre d’état spécifié dans l' *État* n’est pas reconnu par ce système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1a721-135">The state kind specified in *state* is not recognized by this operating system (OS).</span></span> <span data-ttu-id="1a721-136">Appelez [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) pour confirmer que l’interrogation du genre d’État est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1a721-136">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="1a721-137">DXGI_ERROR_UNSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="1a721-137">DXGI_ERROR_UNSUPPORTED</span></span>|<span data-ttu-id="1a721-138">Le genre d’état spécifié dans l' *État* n’est pas pris en charge par l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="1a721-138">The state kind specified in *state* is not supported by the adapter.</span></span> <span data-ttu-id="1a721-139">Appelez [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) pour confirmer que l’interrogation du genre d’État est disponible pour cet adaptateur et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1a721-139">Call [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>|
|<span data-ttu-id="1a721-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1a721-140">E_INVALIDARG</span></span>|<span data-ttu-id="1a721-141">Une taille de mémoire tampon insuffisante est fournie pour *OUTPUTBUFFER* (ou pour *inputStateDetails* où un tampon de détails d’état d’entrée est nécessaire).</span><span class="sxs-lookup"><span data-stu-id="1a721-141">An insufficient buffer size is provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|
|<span data-ttu-id="1a721-142">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="1a721-142">E_POINTER</span></span>|<span data-ttu-id="1a721-143">`nullptr` a été fourni pour *OUTPUTBUFFER* (ou pour *inputStateDetails* où un tampon de détails d’état d’entrée est nécessaire).</span><span class="sxs-lookup"><span data-stu-id="1a721-143">`nullptr` was provided for *outputBuffer* (or for *inputStateDetails* where an input state details buffer is necessary).</span></span>|

## <a name="remarks"></a><span data-ttu-id="1a721-144">Notes</span><span class="sxs-lookup"><span data-stu-id="1a721-144">Remarks</span></span>

<span data-ttu-id="1a721-145">Pour plus d’informations sur chaque type d’état de l’adaptateur et sur les entrées et les sorties utilisées, consultez [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="1a721-145">See [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind, and what inputs and outputs are used.</span></span> <span data-ttu-id="1a721-146">Cette fonction met à zéro la mémoire tampon *OUTPUTBUFFER* avant de la remplir.</span><span class="sxs-lookup"><span data-stu-id="1a721-146">This function zeros out the *outputBuffer* buffer prior to filling it in.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a721-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a721-147">See also</span></span>

<span data-ttu-id="1a721-148">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="1a721-148">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>