---
description: 'Contient un pointeur vers le jeton qui a été fourni à la méthode IMFMediaStream :: RequestSample.'
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: Attribut MFSampleExtension_Token (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532097"
---
# <a name="mfsampleextension_token-attribute"></a><span data-ttu-id="1ce4e-103">\_Attribut de jeton MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="1ce4e-103">MFSampleExtension\_Token attribute</span></span>

<span data-ttu-id="1ce4e-104">Contient un pointeur vers le jeton qui a été fourni à la méthode [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="1ce4e-104">Contains a pointer to the token that was provided to the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

## <a name="data-type"></a><span data-ttu-id="1ce4e-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1ce4e-105">Data type</span></span>

<span data-ttu-id="1ce4e-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="1ce4e-106">\**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="1ce4e-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="1ce4e-107">Get/set</span></span>

<span data-ttu-id="1ce4e-108">Pour récupérer cet attribut, appelez [_ *IMFAttributes :: GetUnknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="1ce4e-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="1ce4e-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="1ce4e-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="1ce4e-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="1ce4e-110">Applies to</span></span>

[<span data-ttu-id="1ce4e-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="1ce4e-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="1ce4e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1ce4e-112">Remarks</span></span>

<span data-ttu-id="1ce4e-113">Cet attribut s’applique aux exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="1ce4e-113">This attribute applies to media samples.</span></span> <span data-ttu-id="1ce4e-114">La valeur de l’attribut est le pointeur **IUnknown** qui est passé au paramètre *pToken* de la méthode [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="1ce4e-114">The value of the attribute is the **IUnknown** pointer that is passed to the *pToken* parameter of the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span> <span data-ttu-id="1ce4e-115">L’appelant utilise cet attribut pour suivre l’état de la demande.</span><span class="sxs-lookup"><span data-stu-id="1ce4e-115">The caller uses this attribute to track the status of the request.</span></span>

<span data-ttu-id="1ce4e-116">Si vous écrivez une source de média personnalisée, définissez cet attribut sur l’exemple lorsque le flux de média fournit un exemple en réponse à la méthode [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) , sauf si la valeur de *pToken* est **null**.</span><span class="sxs-lookup"><span data-stu-id="1ce4e-116">If you are writing a custom media source, set this attribute on the sample when the media stream delivers a sample in response to the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method, unless the value of *pToken* is **NULL**.</span></span>

<span data-ttu-id="1ce4e-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1ce4e-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce4e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ce4e-118">Requirements</span></span>



| <span data-ttu-id="1ce4e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ce4e-119">Requirement</span></span> | <span data-ttu-id="1ce4e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ce4e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce4e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ce4e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce4e-122">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="1ce4e-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1ce4e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ce4e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce4e-124">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="1ce4e-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1ce4e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ce4e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ce4e-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ce4e-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ce4e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ce4e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce4e-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ce4e-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ce4e-129">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="1ce4e-129">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ce4e-130">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="1ce4e-130">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




