---
description: Filtre l’image d’aperçu.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'IWiaImageFilter :: FilterPreviewImage, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543672"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a><span data-ttu-id="1958e-103">IWiaImageFilter :: FilterPreviewImage, méthode</span><span class="sxs-lookup"><span data-stu-id="1958e-103">IWiaImageFilter::FilterPreviewImage method</span></span>

<span data-ttu-id="1958e-104">Filtre l’image d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="1958e-104">Filters the preview image.</span></span>

## <a name="syntax"></a><span data-ttu-id="1958e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1958e-105">Syntax</span></span>


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a><span data-ttu-id="1958e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1958e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1958e-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1958e-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1958e-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="1958e-108">Type: **LONG**</span></span>

<span data-ttu-id="1958e-109">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="1958e-109">Not used.</span></span> <span data-ttu-id="1958e-110">Définit la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="1958e-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1958e-111">*pWiaChildItem2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1958e-111">*pWiaChildItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1958e-112">Tapez : \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="1958e-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="1958e-113">Élément traité.</span><span class="sxs-lookup"><span data-stu-id="1958e-113">The item that is processed.</span></span>

</dd> <dt>

<span data-ttu-id="1958e-114">_InputImageExtents \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1958e-114">_InputImageExtents\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1958e-115">Type : **Rect**</span><span class="sxs-lookup"><span data-stu-id="1958e-115">Type: **RECT**</span></span>

<span data-ttu-id="1958e-116">Coordonnées (sur la zone d’acquisition physique) de l’image que le composant d’aperçu met en cache en interne.</span><span class="sxs-lookup"><span data-stu-id="1958e-116">The coordinates (on the physical acquisition area) of the image that the preview component caches internally.</span></span>

</dd> <dt>

<span data-ttu-id="1958e-117">*pInputStream* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1958e-117">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1958e-118">Type : \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="1958e-118">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="1958e-119">Pointeur vers l’interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) pour les données d’image mises en cache qui sont filtrées.</span><span class="sxs-lookup"><span data-stu-id="1958e-119">A pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) interface for the cached image data that is filtered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1958e-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1958e-120">Return value</span></span>

<span data-ttu-id="1958e-121">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1958e-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1958e-122">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1958e-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1958e-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1958e-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1958e-124">Notes</span><span class="sxs-lookup"><span data-stu-id="1958e-124">Remarks</span></span>

<span data-ttu-id="1958e-125">N’appelez pas cette méthode directement à partir de votre application.</span><span class="sxs-lookup"><span data-stu-id="1958e-125">Do not call this method directly from your application.</span></span>

<span data-ttu-id="1958e-126">*pWiaChildItem2* doit être un élément enfant du *pWiaItem2* qui a été passé dans [**IWiaImageFilter :: InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span><span class="sxs-lookup"><span data-stu-id="1958e-126">*pWiaChildItem2* must be a child item of the *pWiaItem2* that was passed into [**IWiaImageFilter::InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).</span></span>

<span data-ttu-id="1958e-127">*InputImageExtents* est nécessaire, car le filtre de traitement d’image est chargé de couper la zone d’image que *pWiaChildItem2* représente à partir des données d’image transmises par le biais de *pInputStream*.</span><span class="sxs-lookup"><span data-stu-id="1958e-127">*InputImageExtents* is needed because the image processing filter is responsible for cutting out the image area that *pWiaChildItem2* represents from the image data passed in through *pInputStream*.</span></span>

<span data-ttu-id="1958e-128">Une application doit s’assurer que *pWiaChildItem2* a le même format d’image (WIA \_ \_ ), la résolution (WIA \_ IPS \_ XRES et WIA \_ \_ YRES) et la profondeur de bit (WIA de la \_ Loi WIA), \_ car *pWiaItem2* avait été passé dans [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="1958e-128">An application must ensure that *pWiaChildItem2* has the same image format (WIA\_IPA\_FORMAT), resolution (WIA\_IPS\_XRES and WIA\_IPS\_YRES) and bit depth (WIA\_IPA\_DEPTH) as *pWiaItem2* had when it was passed into [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1958e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1958e-129">Requirements</span></span>



| <span data-ttu-id="1958e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1958e-130">Requirement</span></span> | <span data-ttu-id="1958e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="1958e-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1958e-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1958e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1958e-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1958e-133">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1958e-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1958e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1958e-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1958e-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1958e-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="1958e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1958e-137"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="1958e-137"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="1958e-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="1958e-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1958e-139"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1958e-139"><dt>Wia.idl</dt></span></span> </dl> |



 

 
