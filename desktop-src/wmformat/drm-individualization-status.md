---
title: Énumération DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
description: Le \_ \_ type d’énumération de l’état de l’individualisation DRM définit les États valides pour l’individualisation DRM. | Énumération DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- Format Windows Media d’énumération DRM_INDIVIDUALIZATION_STATUS
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d59a19c58c775ee22d78e17bc09add2825948e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104394024"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a><span data-ttu-id="0405d-106">Énumération DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="0405d-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="0405d-107">Le type d’énumération de l’état de l' **\_ individualisation \_ DRM** définit les États valides pour l' [*individualisation*](wmformat-glossary.md)DRM.</span><span class="sxs-lookup"><span data-stu-id="0405d-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM [*individualization*](wmformat-glossary.md).</span></span> <span data-ttu-id="0405d-108">Quand une application lance l’individualisation à l’aide d’un appel à [**IWMDRMReader :: Individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), la progression de la demande d’individualisation est transporte à l’application via des appels à la méthode [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="0405d-108">When an application initiates individualization with a call to [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), the progress of the individualization request is conveyed to the application through calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="0405d-109">Les messages d’état de l’individualisation utilisent tous le \_ membre de l’élément Individual de WMT du type d’énumération d' [**\_ État WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) comme paramètre d' *État* .</span><span class="sxs-lookup"><span data-stu-id="0405d-109">Individualization status messages will all use the WMT\_INDIVIDUALIZE member of the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type as the *Status* parameter.</span></span> <span data-ttu-id="0405d-110">L’état de l’individualisation est passé à **OnStatus** dans le paramètre *pValue* .</span><span class="sxs-lookup"><span data-stu-id="0405d-110">The status of the individualization is passed to **OnStatus** in the *pValue* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="0405d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0405d-111">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="0405d-112">Constantes</span><span class="sxs-lookup"><span data-stu-id="0405d-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0405d-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI \_ non défini**</span><span class="sxs-lookup"><span data-stu-id="0405d-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="0405d-114">Cette valeur est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0405d-114">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="0405d-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI \_ Begin**</span><span class="sxs-lookup"><span data-stu-id="0405d-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="0405d-116">Indique le début du processus d’individualisation.</span><span class="sxs-lookup"><span data-stu-id="0405d-116">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="0405d-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ réussie**</span><span class="sxs-lookup"><span data-stu-id="0405d-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="0405d-118">Indique que le processus d’individualisation est terminé.</span><span class="sxs-lookup"><span data-stu-id="0405d-118">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="0405d-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**échec de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="0405d-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="0405d-120">Indique que le processus d’individualisation a échoué.</span><span class="sxs-lookup"><span data-stu-id="0405d-120">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="0405d-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI \_ Annuler**</span><span class="sxs-lookup"><span data-stu-id="0405d-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="0405d-122">Indique que le processus d’individualisation a été annulé à la suite d’un appel à [**IWMDRMReader :: CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span><span class="sxs-lookup"><span data-stu-id="0405d-122">Indicates that the individualization process was canceled as the result of a call to [**IWMDRMReader::CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span></span>

</dd> <dt>

<span data-ttu-id="0405d-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**Téléchargement de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="0405d-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="0405d-124">Indique que la mise à niveau de sécurité est en cours de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="0405d-124">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="0405d-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**installation de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="0405d-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="0405d-126">Indique que la mise à niveau de sécurité est en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="0405d-126">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0405d-127">Notes</span><span class="sxs-lookup"><span data-stu-id="0405d-127">Remarks</span></span>

<span data-ttu-id="0405d-128">Cette énumération est utilisée par la structure d' [**\_ \_ État**](wm-individualize-status.md) de l’énumération WM.</span><span class="sxs-lookup"><span data-stu-id="0405d-128">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0405d-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0405d-129">Requirements</span></span>



| <span data-ttu-id="0405d-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0405d-130">Requirement</span></span> | <span data-ttu-id="0405d-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="0405d-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0405d-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0405d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0405d-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0405d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0405d-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0405d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0405d-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0405d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0405d-136">Version</span><span class="sxs-lookup"><span data-stu-id="0405d-136">Version</span></span><br/>                  | <span data-ttu-id="0405d-137">SDK Windows Media Format 7 ou versions ultérieures du kit de développement logiciel (SDK)</span><span class="sxs-lookup"><span data-stu-id="0405d-137">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="0405d-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="0405d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0405d-139"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="0405d-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0405d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0405d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0405d-141">**\_État http \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="0405d-141">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="0405d-142">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="0405d-142">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





