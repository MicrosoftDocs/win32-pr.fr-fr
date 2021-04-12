---
description: 'Indique que le type de sortie a été défini sur le moteur de capture en réponse à IMFCaptureSink2 :: SetOutputType.'
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: Attribut MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5819de6a07f3b6a339400d65ff9260c33b14c592
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321634"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a><span data-ttu-id="7e38b-103">\_Attribut de \_ \_ définition de \_ type de média de sortie du \_ moteur de capture \_ MF</span><span class="sxs-lookup"><span data-stu-id="7e38b-103">MF\_CAPTURE\_ENGINE\_OUTPUT\_MEDIA\_TYPE\_SET attribute</span></span>

<span data-ttu-id="7e38b-104">Indique que le type de sortie a été défini sur le moteur de capture en réponse à [**IMFCaptureSink2 :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="7e38b-104">Indicates that the output type has been set on the capture engine in response to [**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="data-type"></a><span data-ttu-id="7e38b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7e38b-105">Data type</span></span>

<span data-ttu-id="7e38b-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="7e38b-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="7e38b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="7e38b-107">Remarks</span></span>

<span data-ttu-id="7e38b-108">Vous pouvez appeler [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) pour déterminer si l’opération a réussi ou non.</span><span class="sxs-lookup"><span data-stu-id="7e38b-108">You can call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) to find out if the operation was successful or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e38b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e38b-109">Requirements</span></span>



| <span data-ttu-id="7e38b-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e38b-110">Requirement</span></span> | <span data-ttu-id="7e38b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e38b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e38b-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e38b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="7e38b-113">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e38b-113">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="7e38b-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e38b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="7e38b-115">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e38b-115">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e38b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e38b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e38b-117"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e38b-117"><dt>Mfcaptureengine.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e38b-118">MIDL</span><span class="sxs-lookup"><span data-stu-id="7e38b-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7e38b-119"><dt>Mfcaptureengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7e38b-119"><dt>Mfcaptureengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e38b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e38b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e38b-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e38b-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7e38b-122">**IMFCaptureSink2::SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="7e38b-122">**IMFCaptureSink2::SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 




