---
description: Définit un nouveau rappel d’application pour le filtre de traitement d’image à utiliser pour le transfert des appels.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'IWiaImageFilter :: SetNewCallback, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752829"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a><span data-ttu-id="fbf15-103">IWiaImageFilter :: SetNewCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="fbf15-103">IWiaImageFilter::SetNewCallback method</span></span>

<span data-ttu-id="fbf15-104">Définit un nouveau rappel d’application pour le filtre de traitement d’image à utiliser pour le transfert des appels.</span><span class="sxs-lookup"><span data-stu-id="fbf15-104">Sets a new application callback for the image processing filter to use for forwarding calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf15-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbf15-105">Syntax</span></span>


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="fbf15-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbf15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf15-107">*pWiaTransferCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbf15-107">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf15-108">Type : **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span><span class="sxs-lookup"><span data-stu-id="fbf15-108">Type: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span></span>

<span data-ttu-id="fbf15-109">Spécifie un pointeur vers l’interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) de l’application.</span><span class="sxs-lookup"><span data-stu-id="fbf15-109">Specifies a pointer to the application's [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf15-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbf15-110">Return value</span></span>

<span data-ttu-id="fbf15-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fbf15-111">Type: **HRESULT**</span></span>

<span data-ttu-id="fbf15-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fbf15-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fbf15-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fbf15-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbf15-114">Notes</span><span class="sxs-lookup"><span data-stu-id="fbf15-114">Remarks</span></span>

<span data-ttu-id="fbf15-115">N’appelez pas cette méthode directement à partir de votre application.</span><span class="sxs-lookup"><span data-stu-id="fbf15-115">Do not call this method directly from your application.</span></span>

<span data-ttu-id="fbf15-116">Le filtre de traitement d’image est requis pour libérer l’interface de rappel d’application précédemment stockée avant de définir le nouveau rappel.</span><span class="sxs-lookup"><span data-stu-id="fbf15-116">The image processing filter is required to release the previously stored application callback interface before setting the new callback.</span></span>

<span data-ttu-id="fbf15-117">Si *pWiaTransferCallback* a la **valeur null**, le filtre de traitement d’image doit simplement libérer l’ancien rappel d’application et retourner la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fbf15-117">If *pWiaTransferCallback* is **NULL**, the image processing filter should simply release the old application callback and return S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf15-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbf15-118">Requirements</span></span>



| <span data-ttu-id="fbf15-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbf15-119">Requirement</span></span> | <span data-ttu-id="fbf15-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbf15-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf15-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf15-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf15-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbf15-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fbf15-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf15-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf15-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbf15-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fbf15-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbf15-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbf15-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbf15-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="fbf15-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="fbf15-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fbf15-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fbf15-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




