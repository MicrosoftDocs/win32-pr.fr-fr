---
title: Énumération WMT_RIGHTS (wmdrmsdk. h)
description: Définit les droits qui peuvent être spécifiés dans une licence DRM.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- Format Windows Media d’énumération WMT_RIGHTS
- Format Windows Media d’énumération
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536256"
---
# <a name="wmt_rights-enumeration"></a><span data-ttu-id="3f440-105">\_Énumération des droits WMT</span><span class="sxs-lookup"><span data-stu-id="3f440-105">WMT\_RIGHTS enumeration</span></span>

<span data-ttu-id="3f440-106">Le type d’énumération des **\_ droits WMT** définit les droits qui peuvent être spécifiés dans une licence DRM.</span><span class="sxs-lookup"><span data-stu-id="3f440-106">The **WMT\_RIGHTS** enumeration type defines the rights that may be specified in a DRM license.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f440-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f440-107">Syntax</span></span>


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a><span data-ttu-id="3f440-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="3f440-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3f440-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**lecture d’un \_ droit WMT \_**</span><span class="sxs-lookup"><span data-stu-id="3f440-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT\_RIGHT\_PLAYBACK**</span></span>
</dt> <dd>

<span data-ttu-id="3f440-110">Spécifie le droit de lire le contenu sans restriction.</span><span class="sxs-lookup"><span data-stu-id="3f440-110">Specifies the right to play content without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="3f440-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**\_copie appropriée \_ \_ de WMT vers un \_ \_ appareil non SDMI \_**</span><span class="sxs-lookup"><span data-stu-id="3f440-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="3f440-112">Spécifie le droit de copier le contenu sur un appareil non conforme à l’initiative de Secure Digital Music (SDMI).</span><span class="sxs-lookup"><span data-stu-id="3f440-112">Specifies the right to copy content to a device not compliant with the Secure Digital Music Initiative (SDMI).</span></span>

</dd> <dt>

<span data-ttu-id="3f440-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**\_copie d’un droit WMT \_ \_ sur \_ CD**</span><span class="sxs-lookup"><span data-stu-id="3f440-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT\_RIGHT\_COPY\_TO\_CD**</span></span>
</dt> <dd>

<span data-ttu-id="3f440-114">Spécifie le droit de copier le contenu sur un CD.</span><span class="sxs-lookup"><span data-stu-id="3f440-114">Specifies the right to copy content to a CD.</span></span>

</dd> <dt>

<span data-ttu-id="3f440-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**\_copie d’un droit WMT \_ vers un \_ \_ \_ appareil SDMI**</span><span class="sxs-lookup"><span data-stu-id="3f440-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="3f440-116">Spécifie le droit de copier le contenu sur un appareil compatible avec SDMI.</span><span class="sxs-lookup"><span data-stu-id="3f440-116">Specifies the right to copy content to a device compliant with the SDMI.</span></span>

</dd> <dt>

<span data-ttu-id="3f440-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ juste \_ une \_ fois**</span><span class="sxs-lookup"><span data-stu-id="3f440-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT\_RIGHT\_ONE\_TIME**</span></span>
</dt> <dd>

<span data-ttu-id="3f440-118">Spécifie le droit de lire le contenu une seule fois.</span><span class="sxs-lookup"><span data-stu-id="3f440-118">Specifies the right to play content one time only.</span></span>

</dd> <dt>

<span data-ttu-id="3f440-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**\_flux d’enregistrement approprié de WMT \_ \_ \_ protégé**</span><span class="sxs-lookup"><span data-stu-id="3f440-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT\_RIGHT\_SAVE\_STREAM\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="3f440-120">Spécifie le droit d’enregistrer le contenu à partir d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="3f440-120">Specifies the right to save content from a server.</span></span>

</dd> <dt>

<span data-ttu-id="3f440-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**\_copie à droite WMT \_**</span><span class="sxs-lookup"><span data-stu-id="3f440-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT\_RIGHT\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="3f440-122">Spécifie le droit de copier le contenu.</span><span class="sxs-lookup"><span data-stu-id="3f440-122">Specifies the right to copy content.</span></span> <span data-ttu-id="3f440-123">Windows Media DRM 10 régule les appareils sur lesquels le contenu peut être copié à l’aide des niveaux de protection de sortie (OPLs).</span><span class="sxs-lookup"><span data-stu-id="3f440-123">Windows Media DRM 10 regulates the devices to which the content can be copied by using output protection levels (OPLs).</span></span>

</dd> <dt>

<span data-ttu-id="3f440-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**la \_ bonne \_ lecture collaborative de WMT \_**</span><span class="sxs-lookup"><span data-stu-id="3f440-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT\_RIGHT\_COLLABORATIVE\_PLAY**</span></span>
</dt> <dd>

<span data-ttu-id="3f440-125">Spécifie le droit de lire le contenu dans le cadre d’un scénario en ligne dans lequel plusieurs participants peuvent transmettre des chansons de leur collection vers une playlist partagée.</span><span class="sxs-lookup"><span data-stu-id="3f440-125">Specifies the right to play content as part of an online scenario where multiple participants can contribute songs from their collection to a shared playlist.</span></span>

</dd> <dt>

<span data-ttu-id="3f440-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**\_ \_ déclencheur SDMI à droite WMT \_**</span><span class="sxs-lookup"><span data-stu-id="3f440-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT\_RIGHT\_SDMI\_TRIGGER**</span></span>
</dt> <dd>

<span data-ttu-id="3f440-127">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="3f440-127">Reserved for future use.</span></span> <span data-ttu-id="3f440-128">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="3f440-128">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="3f440-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**\_ \_ NOMORECOPIES SDMI à droite WMT \_**</span><span class="sxs-lookup"><span data-stu-id="3f440-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT\_RIGHT\_SDMI\_NOMORECOPIES**</span></span>
</dt> <dd>

<span data-ttu-id="3f440-130">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="3f440-130">Reserved for future use.</span></span> <span data-ttu-id="3f440-131">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="3f440-131">Do not use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f440-132">Notes</span><span class="sxs-lookup"><span data-stu-id="3f440-132">Remarks</span></span>

<span data-ttu-id="3f440-133">Ces valeurs sont des indicateurs binaires, donc un ou plusieurs peuvent être définis en les associant à **l’opérateur de bits or.**</span><span class="sxs-lookup"><span data-stu-id="3f440-133">These values are bit flags, so one or more can be set by combining them with the bitwise **OR** operator.</span></span>

<span data-ttu-id="3f440-134">Si vous utilisez Windows Media DRM 10 **, \_ le \_ droit \_ de copie WMT sur un \_ \_ \_ appareil non-SDMI**, **\_ le droit \_ d’effectuer une copie de l’appareil WMT vers le \_ \_ \_ périphérique SDMI** et **le remplacement \_ d’WMT dans le \_ \_ \_ CD** sont remplacés par le droit de **\_ \_ copie de WMT**.</span><span class="sxs-lookup"><span data-stu-id="3f440-134">When using Windows Media DRM 10, **WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**, **WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**, and **WMT\_RIGHT\_COPY\_TO\_CD** are superseded by **WMT\_RIGHT\_COPY**.</span></span> <span data-ttu-id="3f440-135">Les limitations sur les appareils sur lesquels le contenu peut être copié sont spécifiées à l’aide de niveaux de protection de sortie (OPLs).</span><span class="sxs-lookup"><span data-stu-id="3f440-135">Limitations on the devices to which the content may be copied are specified by using output protection levels (OPLs).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f440-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f440-136">Requirements</span></span>



| <span data-ttu-id="3f440-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f440-137">Requirement</span></span> | <span data-ttu-id="3f440-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f440-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f440-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f440-139">Header</span></span><br/> | <dl> <span data-ttu-id="3f440-140"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f440-140"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f440-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f440-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f440-142">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="3f440-142">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





