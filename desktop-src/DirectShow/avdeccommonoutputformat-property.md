---
description: Spécifie le format de sortie du décodeur.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Propriété AVDecCommonOutputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522479"
---
# <a name="avdeccommonoutputformat-property"></a><span data-ttu-id="076f8-103">Propriété AVDecCommonOutputFormat</span><span class="sxs-lookup"><span data-stu-id="076f8-103">AVDecCommonOutputFormat property</span></span>

<span data-ttu-id="076f8-104">Spécifie le format de sortie du décodeur.</span><span class="sxs-lookup"><span data-stu-id="076f8-104">Specifies the output format for the decoder.</span></span>

<span data-ttu-id="076f8-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="076f8-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="076f8-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="076f8-106">Data type</span></span>

<span data-ttu-id="076f8-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="076f8-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="076f8-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="076f8-108">Property GUID</span></span>

<span data-ttu-id="076f8-109">**CODECAPI \_ AVDecCommonOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="076f8-109">**CODECAPI\_AVDecCommonOutputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="076f8-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="076f8-110">Property value</span></span>



| <span data-ttu-id="076f8-111">GUID</span><span class="sxs-lookup"><span data-stu-id="076f8-111">GUID</span></span>                                                               | <span data-ttu-id="076f8-112">Description</span><span class="sxs-lookup"><span data-stu-id="076f8-112">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="076f8-113">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM</span><span class="sxs-lookup"><span data-stu-id="076f8-113">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM</span></span>                        | <span data-ttu-id="076f8-114">Audio PCM, utilisant un nombre quelconque de canaux</span><span class="sxs-lookup"><span data-stu-id="076f8-114">PCM audio, using any number of channels</span></span>                                                                                                                                                                             |
| <span data-ttu-id="076f8-115">\_Casque CODECAPI GUID \_ AVDecAudioOutputFormat \_ PCM \_</span><span class="sxs-lookup"><span data-stu-id="076f8-115">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Headphones</span></span>            | <span data-ttu-id="076f8-116">Audio stéréo stéréo, à l’aide de gauche uniquement/droit uniquement (Lo/RO) downmix</span><span class="sxs-lookup"><span data-stu-id="076f8-116">Stereo PCM audio, using left-only/right-only (Lo/Ro) downmix</span></span>                                                                                                                                                        |
| <span data-ttu-id="076f8-117">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ stéréo \_ automatique</span><span class="sxs-lookup"><span data-stu-id="076f8-117">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_Auto</span></span>          | <span data-ttu-id="076f8-118">Audio stéréo PCM, en utilisant la sélection automatique du mode stéréo downmix (Lo/RO ou lt/RT).</span><span class="sxs-lookup"><span data-stu-id="076f8-118">Stereo PCM audio, using automatic selection of the stereo downmix mode (Lo/Ro or Lt/Rt).</span></span> <span data-ttu-id="076f8-119">Vous pouvez utiliser cette valeur pour les formats audio dans lesquels le flux d’entrée définit le mode downmix préféré, tel que Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="076f8-119">You can use this value for audio formats in which the input stream defines the preferred downmix mode, such as Dolby AC-3.</span></span> |
| <span data-ttu-id="076f8-120">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ stéréo \_ MatrixEncoded</span><span class="sxs-lookup"><span data-stu-id="076f8-120">CODECAPI\_GUID\_AVDecAudioOutputFormat\_PCM\_Stereo\_MatrixEncoded</span></span> | <span data-ttu-id="076f8-121">Audio stéréo stéréo, utilisant des downmix stéréo encodées en matrice (LT/RT)</span><span class="sxs-lookup"><span data-stu-id="076f8-121">Stereo PCM audio, using matrix-encoded stereo downmix (Lt/Rt)</span></span>                                                                                                                                                       |
| <span data-ttu-id="076f8-122">\_Binaire CODECAPI GUID \_ AVDecAudioOutputFormat \_ SPDIF \_</span><span class="sxs-lookup"><span data-stu-id="076f8-122">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_Bitstream</span></span>           | <span data-ttu-id="076f8-123">S/PDIF (format de flux binaire compressé Sony/Philips Digital Interface), tel que défini par IEC-60958</span><span class="sxs-lookup"><span data-stu-id="076f8-123">S/PDIF (Sony/Philips Digital Interface Format) compressed bitstream, as defined by IEC-60958</span></span>                                                                                                                        |
| <span data-ttu-id="076f8-124">CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM</span><span class="sxs-lookup"><span data-stu-id="076f8-124">CODECAPI\_GUID\_AVDecAudioOutputFormat\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="076f8-125">Stéréo PCM S/PDIF, comme défini par IEC-60958</span><span class="sxs-lookup"><span data-stu-id="076f8-125">S/PDIF PCM stereo, as defined by IEC-60958</span></span>                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="076f8-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="076f8-126">Requirements</span></span>



| <span data-ttu-id="076f8-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="076f8-127">Requirement</span></span> | <span data-ttu-id="076f8-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="076f8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="076f8-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="076f8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="076f8-130">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="076f8-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="076f8-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="076f8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="076f8-132">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="076f8-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="076f8-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="076f8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="076f8-134"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="076f8-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="076f8-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="076f8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="076f8-136">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="076f8-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="076f8-137">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="076f8-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




