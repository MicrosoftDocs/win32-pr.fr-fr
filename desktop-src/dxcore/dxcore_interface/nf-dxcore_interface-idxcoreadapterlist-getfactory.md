---
title: IDXCoreAdapterList::GetFactory
description: Récupère un pointeur d’interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) vers l’objet de fabrique d’adaptateur dxcore. | IDXCoreAdapterList::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 08dc93f5c7e086e33d15f666a2c5b94fd7dd7e58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538043"
---
# <a name="idxcoreadapterlistgetfactory-method"></a><span data-ttu-id="7cf40-104">IDXCoreAdapterList :: GetFactory, méthode</span><span class="sxs-lookup"><span data-stu-id="7cf40-104">IDXCoreAdapterList::GetFactory method</span></span>

<span data-ttu-id="7cf40-105">Récupère un pointeur d’interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) vers l’objet de fabrique d’adaptateur dxcore.</span><span class="sxs-lookup"><span data-stu-id="7cf40-105">Retrieves an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface pointer to the DXCore adapter factory object.</span></span> <span data-ttu-id="7cf40-106">Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="7cf40-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf40-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cf40-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory) = 0;

template <class T>
HRESULT GetFactory(
  _COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a><span data-ttu-id="7cf40-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cf40-108">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="7cf40-109">riid</span><span class="sxs-lookup"><span data-stu-id="7cf40-109">riid</span></span>

<span data-ttu-id="7cf40-110">Type : **REFIID**</span><span class="sxs-lookup"><span data-stu-id="7cf40-110">Type: **REFIID**</span></span>

<span data-ttu-id="7cf40-111">Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="7cf40-111">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="7cf40-112">Il doit s’agir de l’identificateur d’interface (IID) de [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="7cf40-112">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="7cf40-113">ppvFactory [out]</span><span class="sxs-lookup"><span data-stu-id="7cf40-113">ppvFactory [out]</span></span>

<span data-ttu-id="7cf40-114">Type : **void \* \***</span><span class="sxs-lookup"><span data-stu-id="7cf40-114">Type: **void\*\***</span></span>

<span data-ttu-id="7cf40-115">Adresse d’un pointeur vers une interface avec l’IID spécifié dans le paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="7cf40-115">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="7cf40-116">Une fois le retour réussi, *\* ppvFactory* (l’adresse déréférencée) contient un pointeur vers l’objet de fabrique d’adaptateur dxcore existant.</span><span class="sxs-lookup"><span data-stu-id="7cf40-116">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the existing DXCore adapter factory object.</span></span> <span data-ttu-id="7cf40-117">Avant de retourner, la fonction incrémente le décompte de références sur l’interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) de l’objet de fabrique.</span><span class="sxs-lookup"><span data-stu-id="7cf40-117">Before returning, the function increments the reference count on the factory object's [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span>

## <a name="returns"></a><span data-ttu-id="7cf40-118">Retours</span><span class="sxs-lookup"><span data-stu-id="7cf40-118">Returns</span></span>

<span data-ttu-id="7cf40-119">Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="7cf40-119">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="7cf40-120">Si la fonction est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="7cf40-120">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="7cf40-121">Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="7cf40-121">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="7cf40-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cf40-122">Return value</span></span>|<span data-ttu-id="7cf40-123">Description</span><span class="sxs-lookup"><span data-stu-id="7cf40-123">Description</span></span>|
|-|-|
|<span data-ttu-id="7cf40-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="7cf40-124">E_NOINTERFACE</span></span>|<span data-ttu-id="7cf40-125">Une valeur non valide a été fournie pour *riid*.</span><span class="sxs-lookup"><span data-stu-id="7cf40-125">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="7cf40-126">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="7cf40-126">E_POINTER</span></span>|<span data-ttu-id="7cf40-127">`nullptr` a été fourni pour *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="7cf40-127">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7cf40-128">Notes</span><span class="sxs-lookup"><span data-stu-id="7cf40-128">Remarks</span></span>

<span data-ttu-id="7cf40-129">Pour la durée pendant laquelle une référence existe sur une interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) , une interface [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) ou une interface [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) , les appels supplémentaires à [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList :: GetFactory]()ou [IDXCoreAdapter :: GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) retournent des pointeurs vers le même objet, ce qui permet d’accroître le nombre de références de l’interface **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="7cf40-129">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::GetFactory](), or [IDXCoreAdapter::GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="7cf40-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cf40-130">See also</span></span>

<span data-ttu-id="7cf40-131">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="7cf40-131">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
