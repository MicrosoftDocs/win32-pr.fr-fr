---
title: IDXCoreAdapterList::GetAdapter
description: Récupère un adaptateur spécifique par index à partir d’un objet de liste d’adaptateurs DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031667"
---
# <a name="idxcoreadapterlistgetadapter-method"></a><span data-ttu-id="67e1b-103">IDXCoreAdapterList :: GetAdapter, méthode</span><span class="sxs-lookup"><span data-stu-id="67e1b-103">IDXCoreAdapterList::GetAdapter method</span></span>

<span data-ttu-id="67e1b-104">Récupère un adaptateur spécifique par index à partir d’un objet de liste d’adaptateurs DXCore.</span><span class="sxs-lookup"><span data-stu-id="67e1b-104">Retrieves a specific adapter by index from a DXCore adapter list object.</span></span> <span data-ttu-id="67e1b-105">Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="67e1b-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="67e1b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67e1b-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a><span data-ttu-id="67e1b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67e1b-107">Parameters</span></span>

### <a name="index"></a><span data-ttu-id="67e1b-108">index</span><span class="sxs-lookup"><span data-stu-id="67e1b-108">index</span></span>

<span data-ttu-id="67e1b-109">Type : **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="67e1b-109">Type: **uint32_t**</span></span>

<span data-ttu-id="67e1b-110">Index de base zéro identifiant une instance d’adaptateur dans la liste d’adaptateurs DXCore.</span><span class="sxs-lookup"><span data-stu-id="67e1b-110">A zero-based index, identifying an adapter instance within the DXCore adapter list.</span></span>

### <a name="riid"></a><span data-ttu-id="67e1b-111">riid</span><span class="sxs-lookup"><span data-stu-id="67e1b-111">riid</span></span>

<span data-ttu-id="67e1b-112">Type : **REFIID**</span><span class="sxs-lookup"><span data-stu-id="67e1b-112">Type: **REFIID**</span></span>

<span data-ttu-id="67e1b-113">Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="67e1b-113">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*.</span></span> <span data-ttu-id="67e1b-114">Il doit s’agir de l’identificateur d’interface (IID) de [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span><span class="sxs-lookup"><span data-stu-id="67e1b-114">This is expected to be the interface identifier (IID) of [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).</span></span>

### <a name="ppvadapter-out"></a><span data-ttu-id="67e1b-115">ppvAdapter [out]</span><span class="sxs-lookup"><span data-stu-id="67e1b-115">ppvAdapter [out]</span></span>

<span data-ttu-id="67e1b-116">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="67e1b-116">Type: **void\*\***</span></span>

<span data-ttu-id="67e1b-117">Adresse d’un pointeur vers une interface avec l’IID spécifié dans le paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="67e1b-117">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="67e1b-118">Une fois le retour réussi, *\* ppvAdapter* (l’adresse déréférencée) contient un pointeur vers l’adaptateur dxcore créé.</span><span class="sxs-lookup"><span data-stu-id="67e1b-118">Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the DXCore adapter created.</span></span>

## <a name="returns"></a><span data-ttu-id="67e1b-119">Retours</span><span class="sxs-lookup"><span data-stu-id="67e1b-119">Returns</span></span>

<span data-ttu-id="67e1b-120">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="67e1b-120">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="67e1b-121">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="67e1b-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="67e1b-122">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="67e1b-122">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="67e1b-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67e1b-123">Return value</span></span>|<span data-ttu-id="67e1b-124">Description</span><span class="sxs-lookup"><span data-stu-id="67e1b-124">Description</span></span>|
|-|-|
|<span data-ttu-id="67e1b-125">DXGI_ERROR_DEVICE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="67e1b-125">DXGI_ERROR_DEVICE_REMOVED</span></span>|<span data-ttu-id="67e1b-126">L' *index* est valide, mais l’état de l’adaptateur n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="67e1b-126">The *index* is valid, but the adapter is no longer in a valid state.</span></span>|
|<span data-ttu-id="67e1b-127">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="67e1b-127">E_INVALIDARG</span></span>|<span data-ttu-id="67e1b-128">L' *index* fourni n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="67e1b-128">The provided *index* is not valid.</span></span>|
|<span data-ttu-id="67e1b-129">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="67e1b-129">E_NOINTERFACE</span></span>|<span data-ttu-id="67e1b-130">Une valeur non valide a été fournie pour *riid*.</span><span class="sxs-lookup"><span data-stu-id="67e1b-130">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="67e1b-131">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="67e1b-131">E_POINTER</span></span>|<span data-ttu-id="67e1b-132">`nullptr` a été fourni pour *ppvAdapter*.</span><span class="sxs-lookup"><span data-stu-id="67e1b-132">`nullptr` was provided for *ppvAdapter*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="67e1b-133">Notes</span><span class="sxs-lookup"><span data-stu-id="67e1b-133">Remarks</span></span>

<span data-ttu-id="67e1b-134">Plusieurs appels qui passent un index qui représente le même adaptateur retournent des pointeurs d’interface identiques, y compris entre différentes listes d’adaptateurs.</span><span class="sxs-lookup"><span data-stu-id="67e1b-134">Multiple calls passing an index that represents the same adapter return identical interface pointers, even across different adapter lists.</span></span> <span data-ttu-id="67e1b-135">Par conséquent, il est possible de comparer des pointeurs d’interface pour déterminer si plusieurs pointeurs font référence au même objet d’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="67e1b-135">As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.</span></span>

## <a name="see-also"></a><span data-ttu-id="67e1b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67e1b-136">See also</span></span>

<span data-ttu-id="67e1b-137">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="67e1b-137">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>