---
title: DXCoreCreateAdapterFactory
description: Crée une fabrique d’adaptateur DXCore, que vous pouvez utiliser pour générer d’autres objets DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3f5164578da87af8f4d92c3bedcecb6f3dbaa95e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941244"
---
# <a name="dxcorecreateadapterfactory-function"></a><span data-ttu-id="9fbac-103">DXCoreCreateAdapterFactory fonction)</span><span class="sxs-lookup"><span data-stu-id="9fbac-103">DXCoreCreateAdapterFactory function</span></span>

## <a name="description"></a><span data-ttu-id="9fbac-104">Description</span><span class="sxs-lookup"><span data-stu-id="9fbac-104">Description</span></span>

<span data-ttu-id="9fbac-105">Crée une fabrique d’adaptateur DXCore, que vous pouvez utiliser pour générer d’autres objets DXCore.</span><span class="sxs-lookup"><span data-stu-id="9fbac-105">Creates a DXCore adapter factory, which you can use to generate further DXCore objects.</span></span> <span data-ttu-id="9fbac-106">Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="9fbac-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="9fbac-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fbac-107">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="9fbac-108">riid</span><span class="sxs-lookup"><span data-stu-id="9fbac-108">riid</span></span>

<span data-ttu-id="9fbac-109">Type : **REFIID**</span><span class="sxs-lookup"><span data-stu-id="9fbac-109">Type: **REFIID**</span></span>

<span data-ttu-id="9fbac-110">Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="9fbac-110">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="9fbac-111">Il doit s’agir de l’identificateur d’interface (IID) de [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="9fbac-111">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="9fbac-112">ppvFactory [out]</span><span class="sxs-lookup"><span data-stu-id="9fbac-112">ppvFactory [out]</span></span>

<span data-ttu-id="9fbac-113">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="9fbac-113">Type: **void\*\***</span></span>

<span data-ttu-id="9fbac-114">Adresse d’un pointeur vers une interface avec l’IID spécifié dans le paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="9fbac-114">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="9fbac-115">Une fois le retour réussi, *\* ppvFactory* (l’adresse déréférencée) contient un pointeur vers la fabrique dxcore créée.</span><span class="sxs-lookup"><span data-stu-id="9fbac-115">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the DXCore factory created.</span></span>

## <a name="returns"></a><span data-ttu-id="9fbac-116">Retours</span><span class="sxs-lookup"><span data-stu-id="9fbac-116">Returns</span></span>

<span data-ttu-id="9fbac-117">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="9fbac-117">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="9fbac-118">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="9fbac-118">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="9fbac-119">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="9fbac-119">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="9fbac-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9fbac-120">Return value</span></span>|<span data-ttu-id="9fbac-121">Description</span><span class="sxs-lookup"><span data-stu-id="9fbac-121">Description</span></span>|
|-|-|
|<span data-ttu-id="9fbac-122">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="9fbac-122">E_NOINTERFACE</span></span>|<span data-ttu-id="9fbac-123">Une valeur non valide a été fournie pour *riid*.</span><span class="sxs-lookup"><span data-stu-id="9fbac-123">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="9fbac-124">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="9fbac-124">E_POINTER</span></span>|<span data-ttu-id="9fbac-125">`nullptr` a été fourni pour *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="9fbac-125">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9fbac-126">Notes</span><span class="sxs-lookup"><span data-stu-id="9fbac-126">Remarks</span></span>

<span data-ttu-id="9fbac-127">Pour la durée pendant laquelle une référence existe sur une interface [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) , une interface [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) ou une interface [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) , les appels supplémentaires à **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList :: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)ou [IDXCoreAdapter :: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) retournent des pointeurs vers le même objet, ce qui permet d’accroître le nombre de références de l’interface **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="9fbac-127">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="9fbac-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fbac-128">See also</span></span>

<span data-ttu-id="9fbac-129">[Référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="9fbac-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>