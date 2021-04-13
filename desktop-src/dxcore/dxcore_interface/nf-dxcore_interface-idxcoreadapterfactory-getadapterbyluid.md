---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Récupère l’objet d’adaptateur DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) pour un LUID spécifié, s’il est disponible.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382381"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a><span data-ttu-id="7e6f9-103">IDXCoreAdapterFactory :: GetAdapterByLuid, méthode</span><span class="sxs-lookup"><span data-stu-id="7e6f9-103">IDXCoreAdapterFactory::GetAdapterByLuid method</span></span>

<span data-ttu-id="7e6f9-104">Récupère l’objet d’adaptateur DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) pour un LUID spécifié, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-104">Retrieves the DXCore adapter object ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) for a specified LUID, if available.</span></span> <span data-ttu-id="7e6f9-105">Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="7e6f9-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e6f9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e6f9-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="7e6f9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e6f9-107">Parameters</span></span>

### <a name="adapterluid"></a><span data-ttu-id="7e6f9-108">adapterLUID</span><span class="sxs-lookup"><span data-stu-id="7e6f9-108">adapterLUID</span></span>

<span data-ttu-id="7e6f9-109">Type : **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span><span class="sxs-lookup"><span data-stu-id="7e6f9-109">Type: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**</span></span>

<span data-ttu-id="7e6f9-110">Valeur locale unique qui identifie l’instance de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-110">The locally unique value that identifies the adapter instance.</span></span>

### <a name="riid-in"></a><span data-ttu-id="7e6f9-111">riid [in]</span><span class="sxs-lookup"><span data-stu-id="7e6f9-111">riid [in]</span></span>

<span data-ttu-id="7e6f9-112">Type : **REFIID**</span><span class="sxs-lookup"><span data-stu-id="7e6f9-112">Type: **REFIID**</span></span>

<span data-ttu-id="7e6f9-113">Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="7e6f9-114">Il doit s’agir de l’identificateur d’interface (IID) de [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span><span class="sxs-lookup"><span data-stu-id="7e6f9-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="7e6f9-115">ppvAdapter [out]</span><span class="sxs-lookup"><span data-stu-id="7e6f9-115">ppvAdapter [out]</span></span>

<span data-ttu-id="7e6f9-116">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="7e6f9-116">Type: **void\*\***</span></span>

<span data-ttu-id="7e6f9-117">Adresse d’un pointeur vers une interface avec l’IID spécifié dans le paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="7e6f9-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="7e6f9-118">Une fois le retour réussi, *\* ppvAdapter* (l’adresse déréférencée) contient un pointeur vers l’adaptateur dxcore créé.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="7e6f9-119">Retours</span><span class="sxs-lookup"><span data-stu-id="7e6f9-119">Returns</span></span>

<span data-ttu-id="7e6f9-120">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="7e6f9-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="7e6f9-121">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="7e6f9-122">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="7e6f9-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e6f9-123">Return value</span></span>|<span data-ttu-id="7e6f9-124">Description</span><span class="sxs-lookup"><span data-stu-id="7e6f9-124">Description</span></span>|
|-|-|
|<span data-ttu-id="7e6f9-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="7e6f9-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="7e6f9-126">Le LUID d’adaptateur transmis dans *adapterLUID* est reconnu, mais l’état de l’adaptateur n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-126">The adapter LUID passed in *adapterLUID* is recognized, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="7e6f9-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7e6f9-127">E_INVALIDARG</span></span>|<span data-ttu-id="7e6f9-128">Aucun LUID d’adaptateur de ce type, car la valeur transmise dans *adapterLUID* est disponible via dxcore.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-128">No such adapter LUID as the value passed in *adapterLUID* is available through DXCore.</span></span>|
|<span data-ttu-id="7e6f9-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="7e6f9-129">E_NOINTERFACE</span></span>|<span data-ttu-id="7e6f9-130">Une valeur non valide a été fournie pour *riid*.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="7e6f9-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="7e6f9-131">E_POINTER</span></span>|<span data-ttu-id="7e6f9-132">`nullptr` a été fourni pour *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7e6f9-133">Notes</span><span class="sxs-lookup"><span data-stu-id="7e6f9-133">Remarks</span></span>

<span data-ttu-id="7e6f9-134">Plusieurs appels passant le même [LUID](/windows/win32/api/winnt/ns-winnt-luid) retournent des pointeurs d’interface identiques.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-134">Multiple calls passing the same [LUID](/windows/win32/api/winnt/ns-winnt-luid) return identical interface pointers.</span></span> <span data-ttu-id="7e6f9-135">Par conséquent, il est possible de comparer des pointeurs d’interface pour déterminer si plusieurs pointeurs font référence au même objet d’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="7e6f9-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e6f9-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e6f9-136">See also</span></span>

<span data-ttu-id="7e6f9-137">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="7e6f9-137">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>