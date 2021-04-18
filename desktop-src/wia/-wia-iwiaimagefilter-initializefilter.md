---
description: Initialise le filtre. Appelé par l’acquisition d’images Windows (WIA) 2,0 avant le téléchargement de chaque image.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'IWiaImageFilter :: InitializeFilter, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519714"
---
# <a name="iwiaimagefilterinitializefilter-method"></a><span data-ttu-id="98598-104">IWiaImageFilter :: InitializeFilter, méthode</span><span class="sxs-lookup"><span data-stu-id="98598-104">IWiaImageFilter::InitializeFilter method</span></span>

<span data-ttu-id="98598-105">Initialise le filtre.</span><span class="sxs-lookup"><span data-stu-id="98598-105">Initializes the filter.</span></span> <span data-ttu-id="98598-106">Appelé par l’acquisition d’images Windows (WIA) 2,0 avant le téléchargement de chaque image.</span><span class="sxs-lookup"><span data-stu-id="98598-106">Called by Windows Image Acquisition (WIA) 2.0 before each image download.</span></span>

## <a name="syntax"></a><span data-ttu-id="98598-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98598-107">Syntax</span></span>


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="98598-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98598-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98598-109">*pWiaItem2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98598-109">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98598-110">Tapez : \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="98598-110">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="98598-111">Spécifie un pointeur vers l’élément [_ *IWiaItem2* \*](-wia-iwiaitem2.md) qui représente l’image d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="98598-111">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item that represents the preview image.</span></span>

</dd> <dt>

<span data-ttu-id="98598-112">*pWiaTransferCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98598-112">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98598-113">Tapez : \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="98598-113">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="98598-114">Spécifie un pointeur vers l’interface [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) de l’application.</span><span class="sxs-lookup"><span data-stu-id="98598-114">Specifies a pointer to the application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98598-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98598-115">Return value</span></span>

<span data-ttu-id="98598-116">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="98598-116">Type: **HRESULT**</span></span>

<span data-ttu-id="98598-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="98598-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="98598-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98598-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="98598-119">Notes</span><span class="sxs-lookup"><span data-stu-id="98598-119">Remarks</span></span>

<span data-ttu-id="98598-120">Cette méthode est appelée lorsqu’une application appelle le [**Téléchargement**](-wia-iwiatransfer-download.md) et lorsqu’une application appelle la fonction du composant WIA 2,0 Preview `GetNewPreview` .</span><span class="sxs-lookup"><span data-stu-id="98598-120">This method is called when an application calls [**Download**](-wia-iwiatransfer-download.md) and when an application calls the WIA 2.0 Preview Component's `GetNewPreview` function.</span></span> <span data-ttu-id="98598-121">**IWiaImageFilter :: InitializeFilter** stocke les références à *pWiaItem2* et *pWiaTransferCallback* à transmettre à ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="98598-121">**IWiaImageFilter::InitializeFilter** stores the references to *pWiaItem2* and *pWiaTransferCallback* to pass into these functions.</span></span> <span data-ttu-id="98598-122">Ces deux pointeurs d’interface doivent être stockés en tant que variables membres et [IUnknown :: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) doit être appelé pour chacun.</span><span class="sxs-lookup"><span data-stu-id="98598-122">These two interface pointers should be stored as member variables and [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) should be called for each.</span></span> <span data-ttu-id="98598-123">Les pointeurs d’interface sont également nécessaires dans l’implémentation du filtre de [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) et [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) lors de l’acquisition d’images.</span><span class="sxs-lookup"><span data-stu-id="98598-123">The interface pointers are also needed in the filter's implementation of [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) and [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) during image acquisition.</span></span>

## <a name="requirements"></a><span data-ttu-id="98598-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98598-124">Requirements</span></span>



| <span data-ttu-id="98598-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98598-125">Requirement</span></span> | <span data-ttu-id="98598-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="98598-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98598-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98598-127">Minimum supported client</span></span><br/> | <span data-ttu-id="98598-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98598-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="98598-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98598-129">Minimum supported server</span></span><br/> | <span data-ttu-id="98598-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98598-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="98598-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="98598-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="98598-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="98598-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="98598-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="98598-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="98598-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="98598-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 
