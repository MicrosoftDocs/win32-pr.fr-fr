---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Génère une liste d’objets adaptateur représentant l’état actuel de l’adaptateur du système et répondant aux critères spécifiés.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463459"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a><span data-ttu-id="f0cd7-103">IDXCoreAdapterFactory :: CreateAdapterList, méthode</span><span class="sxs-lookup"><span data-stu-id="f0cd7-103">IDXCoreAdapterFactory::CreateAdapterList method</span></span>

<span data-ttu-id="f0cd7-104">Génère une liste d’objets adaptateur représentant l’état actuel de l’adaptateur du système et répondant aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-104">Generates a list of adapter objects representing the current adapter state of the system, and meeting the criteria specified.</span></span> <span data-ttu-id="f0cd7-105">Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="f0cd7-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0cd7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0cd7-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a><span data-ttu-id="f0cd7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0cd7-107">Parameters</span></span>

### <a name="numattributes"></a><span data-ttu-id="f0cd7-108">numAttributes</span><span class="sxs-lookup"><span data-stu-id="f0cd7-108">numAttributes</span></span>

<span data-ttu-id="f0cd7-109">Type : **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="f0cd7-109">Type: **uint32_t**</span></span>

<span data-ttu-id="f0cd7-110">Nombre d’éléments dans le tableau vers lequel pointe l’argument *FilterAttributes* .</span><span class="sxs-lookup"><span data-stu-id="f0cd7-110">The number of elements in the array pointed to by the *filterAttributes* argument.</span></span>

### <a name="filterattributes-in"></a><span data-ttu-id="f0cd7-111">filterAttributes [in]</span><span class="sxs-lookup"><span data-stu-id="f0cd7-111">filterAttributes [in]</span></span>

<span data-ttu-id="f0cd7-112">Type : **const GUID \***</span><span class="sxs-lookup"><span data-stu-id="f0cd7-112">Type: **const GUID\***</span></span>

<span data-ttu-id="f0cd7-113">Pointeur vers un tableau de GUID d’attribut d’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-113">A pointer to an array of adapter attribute GUIDs.</span></span> <span data-ttu-id="f0cd7-114">Pour obtenir la liste des GUID d’attribut, consultez [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f0cd7-114">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span> <span data-ttu-id="f0cd7-115">Au moins un GUID doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-115">At least one GUID must be provided.</span></span> <span data-ttu-id="f0cd7-116">Dans le cas où plusieurs GUID sont fournis dans le tableau, seuls les adaptateurs qui satisfont à *tous* les attributs demandés sont inclus dans la liste retournée.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-116">In the case that more than one GUID is provided in the array, only adapters that meet *all* of the requested attributes will be included in the returned list.</span></span>

### <a name="riid"></a><span data-ttu-id="f0cd7-117">riid</span><span class="sxs-lookup"><span data-stu-id="f0cd7-117">riid</span></span>

<span data-ttu-id="f0cd7-118">Type : **REFIID**</span><span class="sxs-lookup"><span data-stu-id="f0cd7-118">Type: **REFIID**</span></span>

<span data-ttu-id="f0cd7-119">Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans *ppvAdapterList*.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-119">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapterList*.</span></span> <span data-ttu-id="f0cd7-120">Il doit s’agir de l’identificateur d’interface (IID) de [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).</span><span class="sxs-lookup"><span data-stu-id="f0cd7-120">This is expected to be the interface identifier (IID) of [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).</span></span>

### <a name="ppvadapterlist-out"></a><span data-ttu-id="f0cd7-121">ppvAdapterList [out]</span><span class="sxs-lookup"><span data-stu-id="f0cd7-121">ppvAdapterList [out]</span></span>

<span data-ttu-id="f0cd7-122">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="f0cd7-122">Type: **void\*\***</span></span>

<span data-ttu-id="f0cd7-123">Adresse d’un pointeur vers une interface avec l’IID spécifié dans le paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="f0cd7-123">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="f0cd7-124">Une fois le retour réussi, *\* ppvAdapterList* (l’adresse déréférencée) contient un pointeur vers la liste d’adaptateurs créée.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-124">Upon successful return, *\*ppvAdapterList* (the dereferenced address) contains a pointer to the adapter list created.</span></span>

## <a name="returns"></a><span data-ttu-id="f0cd7-125">Retours</span><span class="sxs-lookup"><span data-stu-id="f0cd7-125">Returns</span></span>

<span data-ttu-id="f0cd7-126">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="f0cd7-126">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="f0cd7-127">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-127">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="f0cd7-128">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-128">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="f0cd7-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0cd7-129">Return value</span></span>|<span data-ttu-id="f0cd7-130">Description</span><span class="sxs-lookup"><span data-stu-id="f0cd7-130">Description</span></span>|
|-|-|
|<span data-ttu-id="f0cd7-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f0cd7-131">E_INVALIDARG</span></span>|<span data-ttu-id="f0cd7-132">`nullptr` a été fourni pour *FilterAttributes*, ou 0 a été fourni pour *numAttributes*.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-132">`nullptr` was provided for *filterAttributes*, or 0 was provided for *numAttributes*.</span></span>|
|<span data-ttu-id="f0cd7-133">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="f0cd7-133">E_NOINTERFACE</span></span>|<span data-ttu-id="f0cd7-134">Une valeur non valide a été fournie pour *riid*.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-134">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="f0cd7-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="f0cd7-135">E_POINTER</span></span>|<span data-ttu-id="f0cd7-136">`nullptr` a été fourni pour *ppvAdapterList*.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-136">`nullptr` was provided for *ppvAdapterList*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f0cd7-137">Notes</span><span class="sxs-lookup"><span data-stu-id="f0cd7-137">Remarks</span></span>

<span data-ttu-id="f0cd7-138">Même si aucun adaptateur n’est trouvé, à condition que les arguments soient valides, **CreateAdapterList** crée un objet [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) valide et retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-138">Even if no adapters are found, as long as the arguments are valid, **CreateAdapterList** creates a valid [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object, and returns **S_OK**.</span></span> <span data-ttu-id="f0cd7-139">Une fois générés, les adaptateurs de cette liste spécifique ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-139">Once generated, the adapters in this specific list won't change.</span></span> <span data-ttu-id="f0cd7-140">Toutefois, la liste est considérée comme obsolète si l’un des adaptateurs devient non valide, ou si un nouvel adaptateur répond aux critères de filtre fournis.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-140">But the list will be considered stale if one of the adapters later becomes invalid, or if a new adapter arrives that meets the provided filter criteria.</span></span> <span data-ttu-id="f0cd7-141">La liste retournée par **CreateAdapterList** n’est pas ordonnée d’une manière particulière, mais l’ordre d’une liste est cohérent entre plusieurs appels, et même entre les redémarrages du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-141">The list returned by **CreateAdapterList** is not ordered in any particular way, but the ordering of a list is consistent across multiple calls, and even across operating system restarts.</span></span> <span data-ttu-id="f0cd7-142">Le classement peut changer lors des modifications de configuration du système, y compris l’ajout ou la suppression d’un adaptateur, ou la mise à jour d’un pilote sur un adaptateur existant.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-142">The ordering may change upon system configuration changes, including the addition or removal of an adapter, or a driver update on an existing adapter.</span></span> <span data-ttu-id="f0cd7-143">Vous pouvez vous inscrire à ces modifications avec [IDXCoreAdapterFactory :: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) en utilisant le type de notification **DXCoreNotificationType. AdapterListStale**.</span><span class="sxs-lookup"><span data-stu-id="f0cd7-143">You can register for these changes with [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) using the notification type **DXCoreNotificationType.AdapterListStale**.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0cd7-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0cd7-144">See also</span></span>

<span data-ttu-id="f0cd7-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [référence dxcore](../dxcore-reference.md), [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f0cd7-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>