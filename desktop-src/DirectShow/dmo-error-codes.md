---
description: Le tableau suivant contient les codes d’erreur spécifiques à Microsoft DirectX Media Objects (DMOs). Ces codes d’erreur sont définis dans le fichier d’en-tête Mediaerr. h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: Codes d’erreur DMO (Mediaerr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534889"
---
# <a name="dmo-error-codes"></a><span data-ttu-id="d2561-104">Codes d’erreur DMO</span><span class="sxs-lookup"><span data-stu-id="d2561-104">DMO Error Codes</span></span>

<span data-ttu-id="d2561-105">Le tableau suivant contient les codes d’erreur spécifiques à Microsoft DirectX Media Objects (DMOs).</span><span class="sxs-lookup"><span data-stu-id="d2561-105">The following table contains error codes that are specific to Microsoft DirectX Media Objects (DMOs).</span></span> <span data-ttu-id="d2561-106">Ces codes d’erreur sont définis dans le fichier d’en-tête Mediaerr. h.</span><span class="sxs-lookup"><span data-stu-id="d2561-106">These error codes are defined in the header file Mediaerr.h.</span></span>



| <span data-ttu-id="d2561-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="d2561-107">Constant/value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="d2561-108">Description</span><span class="sxs-lookup"><span data-stu-id="d2561-108">Description</span></span>                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <span data-ttu-id="d2561-109"><dt>**DMO \_ \_INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="d2561-109"><dt>**DMO\_E\_INVALIDSTREAMINDEX**</dt> <dt>0x80040201</dt></span></span> </dl> | <span data-ttu-id="d2561-110">Index de flux non valide.</span><span class="sxs-lookup"><span data-stu-id="d2561-110">Invalid stream index.</span></span><br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <span data-ttu-id="d2561-111"><dt>**DMO \_ \_INVALIDTYPE**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="d2561-111"><dt>**DMO\_E\_INVALIDTYPE**</dt> <dt>0x80040202</dt></span></span> </dl>                      | <span data-ttu-id="d2561-112">Type de média non valide.</span><span class="sxs-lookup"><span data-stu-id="d2561-112">Invalid media type.</span></span><br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <span data-ttu-id="d2561-113"><dt>**DMO \_ \_Type E \_ non \_ défini**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="d2561-113"><dt>**DMO\_E\_TYPE\_NOT\_SET**</dt> <dt>0x80040203</dt></span></span> </dl>                 | <span data-ttu-id="d2561-114">Le type de média n’a pas été défini.</span><span class="sxs-lookup"><span data-stu-id="d2561-114">Media type was not set.</span></span> <span data-ttu-id="d2561-115">Un ou plusieurs flux nécessitent un type de média avant que cette opération puisse être effectuée.</span><span class="sxs-lookup"><span data-stu-id="d2561-115">One or more streams require a media type before this operation can be performed.</span></span><br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <span data-ttu-id="d2561-116"><dt>**DMO \_ \_NOTACCEPTING**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="d2561-116"><dt>**DMO\_E\_NOTACCEPTING**</dt> <dt>0x80040204</dt></span></span> </dl>                   | <span data-ttu-id="d2561-117">Impossible d’accepter les données sur ce flux.</span><span class="sxs-lookup"><span data-stu-id="d2561-117">Data cannot be accepted on this stream.</span></span> <span data-ttu-id="d2561-118">Vous devrez peut-être traiter davantage de données de sortie. consultez [**IMediaObject ::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span><span class="sxs-lookup"><span data-stu-id="d2561-118">You might need to process more output data; see [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).</span></span><br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <span data-ttu-id="d2561-119"><dt>**DMO \_ \_Type E \_ non \_ accepté**</dt> <dt>0x80040205</dt></span><span class="sxs-lookup"><span data-stu-id="d2561-119"><dt>**DMO\_E\_TYPE\_NOT\_ACCEPTED**</dt> <dt>0x80040205</dt></span></span> </dl>  | <span data-ttu-id="d2561-120">Le type de média n’a pas été accepté.</span><span class="sxs-lookup"><span data-stu-id="d2561-120">Media type was not accepted.</span></span><br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <span data-ttu-id="d2561-121"><dt>**DMO \_ E \_ \_ plus d' \_ éléments**</dt> <dt>0x80040206</dt></span><span class="sxs-lookup"><span data-stu-id="d2561-121"><dt>**DMO\_E\_NO\_MORE\_ITEMS**</dt> <dt>0x80040206</dt></span></span> </dl>              | <span data-ttu-id="d2561-122">L’index de type de média est hors limites.</span><span class="sxs-lookup"><span data-stu-id="d2561-122">Media-type index is out of range.</span></span><br/>                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="d2561-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2561-123">Requirements</span></span>



| <span data-ttu-id="d2561-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2561-124">Requirement</span></span> | <span data-ttu-id="d2561-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2561-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2561-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2561-126">Header</span></span><br/> | <dl> <span data-ttu-id="d2561-127"><dt>Mediaerr. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2561-127"><dt>Mediaerr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2561-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2561-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2561-129">Constantes DMO</span><span class="sxs-lookup"><span data-stu-id="d2561-129">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




