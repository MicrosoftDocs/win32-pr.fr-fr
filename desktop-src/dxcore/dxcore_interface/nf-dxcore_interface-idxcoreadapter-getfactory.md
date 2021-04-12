---
title: IDXCoreAdapter::GetFactory
description: Récupère un pointeur d’interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) vers l’objet de fabrique d’adaptateur dxcore. | IDXCoreAdapter::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 1ac3e7fccd39b9b03ecb7016494a610519d26afa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211520"
---
# <a name="idxcoreadaptergetfactory-method"></a><span data-ttu-id="1f064-104">IDXCoreAdapter :: GetFactory, méthode</span><span class="sxs-lookup"><span data-stu-id="1f064-104">IDXCoreAdapter::GetFactory method</span></span>

<span data-ttu-id="1f064-105">Récupère un pointeur d’interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) vers l’objet de fabrique d’adaptateur dxcore.</span><span class="sxs-lookup"><span data-stu-id="1f064-105">Retrieves an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface pointer to the DXCore adapter factory object.</span></span> <span data-ttu-id="1f064-106">Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="1f064-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f064-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f064-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory
) = 0;

template <class T>
HRESULT GetFactory(_COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a><span data-ttu-id="1f064-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f064-108">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="1f064-109">riid</span><span class="sxs-lookup"><span data-stu-id="1f064-109">riid</span></span>

<span data-ttu-id="1f064-110">Type : **REFIID**</span><span class="sxs-lookup"><span data-stu-id="1f064-110">Type: **REFIID**</span></span>

<span data-ttu-id="1f064-111">Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="1f064-111">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="1f064-112">Il doit s’agir de l’identificateur d’interface (IID) de [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="1f064-112">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="1f064-113">ppvFactory [out]</span><span class="sxs-lookup"><span data-stu-id="1f064-113">ppvFactory [out]</span></span>

<span data-ttu-id="1f064-114">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="1f064-114">Type: **void\*\***</span></span>

<span data-ttu-id="1f064-115">Adresse d’un pointeur vers une interface avec l’IID spécifié dans le paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="1f064-115">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="1f064-116">Une fois le retour réussi, *\* ppvFactory* (l’adresse déréférencée) contient un pointeur vers l’objet de fabrique d’adaptateur dxcore existant.</span><span class="sxs-lookup"><span data-stu-id="1f064-116">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the existing DXCore adapter factory object.</span></span> <span data-ttu-id="1f064-117">Avant de retourner, la fonction incrémente le décompte de références sur l’interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) de l’objet de fabrique.</span><span class="sxs-lookup"><span data-stu-id="1f064-117">Before returning, the function increments the reference count on the factory object's [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span>

## <a name="returns"></a><span data-ttu-id="1f064-118">Retours</span><span class="sxs-lookup"><span data-stu-id="1f064-118">Returns</span></span>

<span data-ttu-id="1f064-119">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="1f064-119">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="1f064-120">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="1f064-120">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="1f064-121">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="1f064-121">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="1f064-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f064-122">Return value</span></span>|<span data-ttu-id="1f064-123">Description</span><span class="sxs-lookup"><span data-stu-id="1f064-123">Description</span></span>|
|-|-|
|<span data-ttu-id="1f064-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="1f064-124">E_NOINTERFACE</span></span>|<span data-ttu-id="1f064-125">Une valeur non valide a été fournie pour *riid*.</span><span class="sxs-lookup"><span data-stu-id="1f064-125">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="1f064-126">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="1f064-126">E_POINTER</span></span>|<span data-ttu-id="1f064-127">`nullptr` a été fourni pour *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="1f064-127">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1f064-128">Notes</span><span class="sxs-lookup"><span data-stu-id="1f064-128">Remarks</span></span>

<span data-ttu-id="1f064-129">Pour la durée pendant laquelle une référence existe sur une interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) , une interface [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) ou une interface [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) , les appels supplémentaires à [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList :: GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md)ou [IDXCoreAdapter :: GetFactory]() retournent des pointeurs vers le même objet, ce qui permet d’accroître le nombre de références de l’interface **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="1f064-129">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory]() will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f064-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f064-130">See also</span></span>

<span data-ttu-id="1f064-131">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="1f064-131">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
