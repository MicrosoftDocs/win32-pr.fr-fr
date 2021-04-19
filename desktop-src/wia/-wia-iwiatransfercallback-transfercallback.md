---
description: Fournit la progression et d’autres notifications pendant un transfert.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'IWiaTransferCallback :: TransferCallback, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527612"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a><span data-ttu-id="c4903-103">IWiaTransferCallback :: TransferCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="c4903-103">IWiaTransferCallback::TransferCallback method</span></span>

<span data-ttu-id="c4903-104">Fournit la progression et d’autres notifications pendant un transfert.</span><span class="sxs-lookup"><span data-stu-id="c4903-104">Provides progress and other notifications during a transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4903-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4903-105">Syntax</span></span>


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a><span data-ttu-id="c4903-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4903-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4903-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4903-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4903-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="c4903-108">Type: **LONG**</span></span>

<span data-ttu-id="c4903-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="c4903-109">Currently unused.</span></span> <span data-ttu-id="c4903-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="c4903-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c4903-111">*pWiaTransferParams* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4903-111">*pWiaTransferParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4903-112">Tapez : \**[**WiaTransferParams**](-wia-wiatransferparams.md) \** _</span><span class="sxs-lookup"><span data-stu-id="c4903-112">Type: \**[**WiaTransferParams**](-wia-wiatransferparams.md)\** _</span></span>

<span data-ttu-id="c4903-113">Spécifie un pointeur vers une structure [_ *WiaTransferParams* \*](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="c4903-113">Specifies a pointer to a [_ *WiaTransferParams*\*](-wia-wiatransferparams.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4903-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4903-114">Return value</span></span>

<span data-ttu-id="c4903-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4903-115">Type: **HRESULT**</span></span>

<span data-ttu-id="c4903-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c4903-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4903-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4903-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4903-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c4903-118">Remarks</span></span>

<span data-ttu-id="c4903-119">Lorsque cette méthode est implémentée par un filtre de traitement d’image, le minipilote WIA (Windows Image Acquisition) 2,0 l’appelle lors de l’acquisition d’images pour renvoyer des messages de progression à l’application.</span><span class="sxs-lookup"><span data-stu-id="c4903-119">When this method is implemented by an image processing filter, the Windows Image Acquisition (WIA) 2.0 minidriver calls it during image acquisition to send progress messages back to the application.</span></span>

<span data-ttu-id="c4903-120">**IWiaTransferCallback :: TransferCallback** d’un filtre doit déléguer à la méthode **IWiaTransferCallback :: TransferCallback** du rappel d’application.</span><span class="sxs-lookup"><span data-stu-id="c4903-120">A filter's **IWiaTransferCallback::TransferCallback** must delegate to the application callback's **IWiaTransferCallback::TransferCallback** method.</span></span> <span data-ttu-id="c4903-121">En règle générale, le flux de filtre filtre les données qui lui sont passées et écrit les données filtrées directement dans le flux de données fourni par l’application.</span><span class="sxs-lookup"><span data-stu-id="c4903-121">Usually, the filter stream filters the data passed to it and writes the filtered data directly to the application provided stream.</span></span> <span data-ttu-id="c4903-122">Lorsque le filtre de traitement d’images stocke les données entre les appels à sa méthode [IStream :: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , il doit également modifier les valeurs *lPercentComplete* et *ulBytesWrittenToCurrentStream* dans la structure [**WiaTransferParams**](-wia-wiatransferparams.md) .</span><span class="sxs-lookup"><span data-stu-id="c4903-122">When image processing filter stores data between calls to its [IStream::Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) method, it must also modify the *lPercentComplete* and *ulBytesWrittenToCurrentStream* values in the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4903-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4903-123">Requirements</span></span>



| <span data-ttu-id="c4903-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4903-124">Requirement</span></span> | <span data-ttu-id="c4903-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4903-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4903-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4903-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c4903-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4903-127">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c4903-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4903-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c4903-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4903-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c4903-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4903-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4903-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4903-131"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="c4903-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="c4903-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4903-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4903-133"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="c4903-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c4903-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4903-135"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4903-135"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
