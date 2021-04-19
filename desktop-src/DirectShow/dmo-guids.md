---
description: Le tableau suivant répertorie les identificateurs globaux uniques (GUID) définis pour les catégories Microsoft DirectX Media Object (DMO). Ces GUID sont définis dans le fichier d’en-tête Dmoreg. h et exportés par la bibliothèque Dmoguids. lib.
ms.assetid: d67debd0-8ecb-41ab-bc6c-b27cba97c65a
title: GUID DMO (Dmoreg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c10d5bd917d6368d398362e76ffa9ea8255933ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539219"
---
# <a name="dmo-guids"></a><span data-ttu-id="2585f-104">GUID DMO</span><span class="sxs-lookup"><span data-stu-id="2585f-104">DMO GUIDs</span></span>

<span data-ttu-id="2585f-105">Le tableau suivant répertorie les identificateurs globaux uniques (GUID) définis pour les catégories Microsoft DirectX Media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="2585f-105">The following table lists the globally unique identifiers (GUIDs) defined for Microsoft DirectX Media Object (DMO) categories.</span></span> <span data-ttu-id="2585f-106">Ces GUID sont définis dans le fichier d’en-tête Dmoreg. h et exportés par la bibliothèque Dmoguids. lib.</span><span class="sxs-lookup"><span data-stu-id="2585f-106">These GUIDs are defined in the header file Dmoreg.h and exported by the Dmoguids.lib library.</span></span>

<span data-ttu-id="2585f-107">Pour énumérer les DMOs enregistrés dans une catégorie, transmettez le GUID correspondant à la fonction [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) .</span><span class="sxs-lookup"><span data-stu-id="2585f-107">To enumerate the DMOs registered in a category, pass the corresponding GUID to the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span>



| <span data-ttu-id="2585f-108">GUID</span><span class="sxs-lookup"><span data-stu-id="2585f-108">GUID</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="2585f-109">Description</span><span class="sxs-lookup"><span data-stu-id="2585f-109">Description</span></span>                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------|
| <span id="DMOCATEGORY_AUDIO_DECODER"></span><span id="dmocategory_audio_decoder"></span><dl> <span data-ttu-id="2585f-110"><dt>**\_DÉcodeur audio DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2585f-110"><dt>**DMOCATEGORY\_AUDIO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="2585f-111">Décodeur audio</span><span class="sxs-lookup"><span data-stu-id="2585f-111">Audio decoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_EFFECT"></span><span id="dmocategory_audio_effect"></span><dl> <span data-ttu-id="2585f-112"><dt>**\_effet audio \_ DMOCATEGORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2585f-112"><dt>**DMOCATEGORY\_AUDIO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="2585f-113">Effet audio</span><span class="sxs-lookup"><span data-stu-id="2585f-113">Audio effect</span></span><br/>         |
| <span id="DMOCATEGORY_AUDIO_ENCODER"></span><span id="dmocategory_audio_encoder"></span><dl> <span data-ttu-id="2585f-114"><dt>**\_encodeur audio DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2585f-114"><dt>**DMOCATEGORY\_AUDIO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="2585f-115">Encodeur audio</span><span class="sxs-lookup"><span data-stu-id="2585f-115">Audio encoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_DECODER"></span><span id="dmocategory_video_decoder"></span><dl> <span data-ttu-id="2585f-116"><dt>**\_DÉcodeur vidéo DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2585f-116"><dt>**DMOCATEGORY\_VIDEO\_DECODER**</dt></span></span> </dl>                       | <span data-ttu-id="2585f-117">Décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2585f-117">Video decoder</span></span><br/>        |
| <span id="DMOCATEGORY_VIDEO_EFFECT"></span><span id="dmocategory_video_effect"></span><dl> <span data-ttu-id="2585f-118"><dt>**DMOCATEGORY \_ \_ effet vidéo**</dt></span><span class="sxs-lookup"><span data-stu-id="2585f-118"><dt>**DMOCATEGORY\_VIDEO\_EFFECT**</dt></span></span> </dl>                          | <span data-ttu-id="2585f-119">Effet vidéo</span><span class="sxs-lookup"><span data-stu-id="2585f-119">Video effect</span></span><br/>         |
| <span id="DMOCATEGORY_VIDEO_ENCODER"></span><span id="dmocategory_video_encoder"></span><dl> <span data-ttu-id="2585f-120"><dt>**\_encodeur vidéo DMOCATEGORY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2585f-120"><dt>**DMOCATEGORY\_VIDEO\_ENCODER**</dt></span></span> </dl>                       | <span data-ttu-id="2585f-121">Encodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2585f-121">Video encoder</span></span><br/>        |
| <span id="DMOCATEGORY_AUDIO_CAPTURE_EFFECT"></span><span id="dmocategory_audio_capture_effect"></span><dl> <span data-ttu-id="2585f-122"><dt>**DMOCATEGORY \_ \_ effet de capture audio \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2585f-122"><dt>**DMOCATEGORY\_AUDIO\_CAPTURE\_EFFECT**</dt></span></span> </dl> | <span data-ttu-id="2585f-123">Effet de capture audio</span><span class="sxs-lookup"><span data-stu-id="2585f-123">Audio capture effect</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2585f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2585f-124">Requirements</span></span>



| <span data-ttu-id="2585f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2585f-125">Requirement</span></span> | <span data-ttu-id="2585f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2585f-126">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2585f-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="2585f-127">Header</span></span><br/> | <dl> <span data-ttu-id="2585f-128"><dt>Dmoreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2585f-128"><dt>Dmoreg.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2585f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2585f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2585f-130">Constantes DMO</span><span class="sxs-lookup"><span data-stu-id="2585f-130">DMO Constants</span></span>](dmo-constants.md)
</dt> </dl>

 

 




