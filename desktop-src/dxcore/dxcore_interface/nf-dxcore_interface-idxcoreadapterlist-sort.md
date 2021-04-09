---
title: IDXCoreAdapterList::Sort
description: Trie un objet de liste d’adaptateurs DXCore en fonction d’un tableau d’entrée fourni de critères de tri.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102196"
---
# <a name="idxcoreadapterlistsort-method"></a><span data-ttu-id="3b727-103">IDXCoreAdapterList :: sort, méthode</span><span class="sxs-lookup"><span data-stu-id="3b727-103">IDXCoreAdapterList::Sort method</span></span>

## <a name="description"></a><span data-ttu-id="3b727-104">Description</span><span class="sxs-lookup"><span data-stu-id="3b727-104">Description</span></span>

<span data-ttu-id="3b727-105">Trie un objet de liste d’adaptateurs DXCore en fonction d’un tableau d’entrée de critères de tri fourni, où les éléments de tableau précédents dans le tableau de critères reçoivent une pondération plus élevée.</span><span class="sxs-lookup"><span data-stu-id="3b727-105">Sorts a DXCore adapter list object based on a provided input array of sort criteria, where array items earlier in the array of criteria are given a higher weight.</span></span> <span data-ttu-id="3b727-106">Le **Tri** vous permet de trouver plus facilement votre adaptateur idéal dans une liste d’adaptateurs.</span><span class="sxs-lookup"><span data-stu-id="3b727-106">**Sort** helps you to more easily find your ideal adapter in an adapter list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b727-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b727-107">Syntax</span></span>

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a><span data-ttu-id="3b727-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b727-108">Parameters</span></span>

### <a name="numpreferences"></a><span data-ttu-id="3b727-109">numPreferences</span><span class="sxs-lookup"><span data-stu-id="3b727-109">numPreferences</span></span>

<span data-ttu-id="3b727-110">Type : **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="3b727-110">Type: **uint32_t**</span></span>

<span data-ttu-id="3b727-111">Nombre d’éléments dans le tableau vers lequel pointe le paramètre *Preferences* .</span><span class="sxs-lookup"><span data-stu-id="3b727-111">The number of elements that are in the array pointed to by the *preferences* parameter.</span></span>

### <a name="preferences-in"></a><span data-ttu-id="3b727-112">préférences [in]</span><span class="sxs-lookup"><span data-stu-id="3b727-112">preferences [in]</span></span>

<span data-ttu-id="3b727-113">Type : **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***</span><span class="sxs-lookup"><span data-stu-id="3b727-113">Type: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)\***</span></span>

<span data-ttu-id="3b727-114">Pointeur vers un tableau de constantes de valeurs [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) représentant des critères de tri.</span><span class="sxs-lookup"><span data-stu-id="3b727-114">A pointer to a constant array of [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) values, representing sort criteria.</span></span>

## <a name="returns"></a><span data-ttu-id="3b727-115">Retours</span><span class="sxs-lookup"><span data-stu-id="3b727-115">Returns</span></span>

<span data-ttu-id="3b727-116">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="3b727-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="3b727-117">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="3b727-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="3b727-118">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="3b727-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="3b727-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b727-119">Return value</span></span>|<span data-ttu-id="3b727-120">Description</span><span class="sxs-lookup"><span data-stu-id="3b727-120">Description</span></span>|
|-|-|
|<span data-ttu-id="3b727-121">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3b727-121">E_INVALIDARG</span></span>|<span data-ttu-id="3b727-122">L’argument *numPreferences* est égal à zéro ou l’argument *Preferences* a la valeur `nullptr` .</span><span class="sxs-lookup"><span data-stu-id="3b727-122">The *numPreferences* argument is zero, or the *preferences* argument is `nullptr`.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3b727-123">Notes</span><span class="sxs-lookup"><span data-stu-id="3b727-123">Remarks</span></span>

<span data-ttu-id="3b727-124">Dans les cas où une valeur [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) fournie n’est pas reconnue par le système d’exploitation, elle est ignorée et ne provoque pas l’échec de l’API.</span><span class="sxs-lookup"><span data-stu-id="3b727-124">In cases where a provided [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value isn't recognized by the operating system (OS), it is ignored, and won't cause the API to fail.</span></span> <span data-ttu-id="3b727-125">Dans ce cas, les valeurs **DXCoreAdapterPreference** connues seront toujours prises en compte.</span><span class="sxs-lookup"><span data-stu-id="3b727-125">Known **DXCoreAdapterPreference** values will still be considered in this case.</span></span> <span data-ttu-id="3b727-126">Pour déterminer si un type de tri est compris par l’API, appelez [IDXCoreAdapterList :: IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span><span class="sxs-lookup"><span data-stu-id="3b727-126">To determine whether a sort type is understood by the API, call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

<span data-ttu-id="3b727-127">Les valeurs de **DXCoreAdapterPreference** qui se produisent plus tôt dans le tableau de *Préférences* fourni sont traitées avec une priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="3b727-127">**DXCoreAdapterPreference** values that occur earlier in the provided *preferences* array are treated with higher priority.</span></span> 

<span data-ttu-id="3b727-128">Pour plus d’informations sur la logique appliquée à chaque type, reportez-vous à la documentation sur l’énumération **DXCoreAdapterPreference** .</span><span class="sxs-lookup"><span data-stu-id="3b727-128">Refer to the **DXCoreAdapterPreference** enumeration documentation for details about what logic is applied for each type.</span></span> <span data-ttu-id="3b727-129">La logique interne d’un type peut se développer au fur et à mesure du développement du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3b727-129">The internal logic for a type may develop as the OS develops.</span></span>

<span data-ttu-id="3b727-130">Lorsque **sort** retourne, les éléments de la liste de l’adaptateur dxcore sont triés de la plus préférable à la moins préférable.</span><span class="sxs-lookup"><span data-stu-id="3b727-130">When **Sort** returns, items in the DXCore adapter list will have been sorted from most preferable to least preferable.</span></span> <span data-ttu-id="3b727-131">Ainsi, l’appel de [IDXCoreAdapterList :: GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) avec l’index 0 récupère l’adaptateur qui correspond le mieux aux types de préférences de tri demandés ; l’index 1 est la meilleure correspondance la plus proche, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="3b727-131">So, calling [IDXCoreAdapterList::GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) with index 0 retrieves the adapter that best matches the requested sort preference types; index 1 is the next best match, and so on.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b727-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b727-132">See also</span></span>

<span data-ttu-id="3b727-133">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="3b727-133">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>