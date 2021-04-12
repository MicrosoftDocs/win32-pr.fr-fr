---
description: Spécifie le format d’entrée actuel pour le décodeur.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Propriété AVDecCommonInputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7432d2a48727ec144d4206d4a11bfe65ce2c5d2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482281"
---
# <a name="avdeccommoninputformat-property"></a><span data-ttu-id="c5b92-103">Propriété AVDecCommonInputFormat</span><span class="sxs-lookup"><span data-stu-id="c5b92-103">AVDecCommonInputFormat property</span></span>

<span data-ttu-id="c5b92-104">Spécifie le format d’entrée actuel pour le décodeur.</span><span class="sxs-lookup"><span data-stu-id="c5b92-104">Specifies the current input format for the decoder.</span></span>

<span data-ttu-id="c5b92-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c5b92-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="c5b92-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="c5b92-106">Data type</span></span>

<span data-ttu-id="c5b92-107">**BSTR** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="c5b92-107">**BSTR** (**VT\_BSTR**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c5b92-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="c5b92-108">Property GUID</span></span>

<span data-ttu-id="c5b92-109">**CODECAPI \_ AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="c5b92-109">**CODECAPI\_AVDecCommonInputFormat**</span></span>

## <a name="property-value"></a><span data-ttu-id="c5b92-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c5b92-110">Property value</span></span>

<span data-ttu-id="c5b92-111">La valeur de cette propriété est un **BSTR** qui contient la représentation sous forme de chaîne d’un GUID.</span><span class="sxs-lookup"><span data-stu-id="c5b92-111">The value of this property is a **BSTR** that contains the string representation of a GUID.</span></span> <span data-ttu-id="c5b92-112">Les GUID suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="c5b92-112">The following GUIDs are defined.</span></span>



| <span data-ttu-id="c5b92-113">**GUID**</span><span class="sxs-lookup"><span data-stu-id="c5b92-113">**GUID**</span></span>                                            | <span data-ttu-id="c5b92-114">Description</span><span class="sxs-lookup"><span data-stu-id="c5b92-114">Description</span></span>                                    |
|-----------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="c5b92-115">**\_GUID CODECAPI \_ AVDecAudioInputAAC**</span><span class="sxs-lookup"><span data-stu-id="c5b92-115">**CODECAPI\_GUID\_AVDecAudioInputAAC**</span></span>              | <span data-ttu-id="c5b92-116">Codage audio avancé (AAC)</span><span class="sxs-lookup"><span data-stu-id="c5b92-116">Advanced Audio Coding (AAC)</span></span>                    |
| <span data-ttu-id="c5b92-117">**\_GUID CODECAPI \_ AVDecAudioInputDolbyDigitalPlus**</span><span class="sxs-lookup"><span data-stu-id="c5b92-117">**CODECAPI\_GUID\_AVDecAudioInputDolbyDigitalPlus**</span></span> | <span data-ttu-id="c5b92-118">Audio Dolby Digital plus</span><span class="sxs-lookup"><span data-stu-id="c5b92-118">Dolby Digital Plus audio</span></span>                       |
| <span data-ttu-id="c5b92-119">**\_GUID CODECAPI \_ AVDecAudioInputDolby**</span><span class="sxs-lookup"><span data-stu-id="c5b92-119">**CODECAPI\_GUID\_AVDecAudioInputDolby**</span></span>            | <span data-ttu-id="c5b92-120">Audio Dolby</span><span class="sxs-lookup"><span data-stu-id="c5b92-120">Dolby audio</span></span>                                    |
| <span data-ttu-id="c5b92-121">**\_GUID CODECAPI \_ AVDecAudioInputDTS**</span><span class="sxs-lookup"><span data-stu-id="c5b92-121">**CODECAPI\_GUID\_AVDecAudioInputDTS**</span></span>              | <span data-ttu-id="c5b92-122">Fichier audio DTS</span><span class="sxs-lookup"><span data-stu-id="c5b92-122">DTS audio</span></span>                                      |
| <span data-ttu-id="c5b92-123">**\_GUID CODECAPI \_ AVDecAudioInputHEAAC**</span><span class="sxs-lookup"><span data-stu-id="c5b92-123">**CODECAPI\_GUID\_AVDecAudioInputHEAAC**</span></span>            | <span data-ttu-id="c5b92-124">High-Efficiency du codage audio avancé (HE-AAC)</span><span class="sxs-lookup"><span data-stu-id="c5b92-124">High-Efficiency Advanced Audio Coding (HE-AAC)</span></span> |
| <span data-ttu-id="c5b92-125">**\_GUID CODECAPI \_ AVDecAudioInputMPEG**</span><span class="sxs-lookup"><span data-stu-id="c5b92-125">**CODECAPI\_GUID\_AVDecAudioInputMPEG**</span></span>             | <span data-ttu-id="c5b92-126">Audio MPEG</span><span class="sxs-lookup"><span data-stu-id="c5b92-126">MPEG audio</span></span>                                     |
| <span data-ttu-id="c5b92-127">**\_GUID CODECAPI \_ AVDecAudioInputPCM**</span><span class="sxs-lookup"><span data-stu-id="c5b92-127">**CODECAPI\_GUID\_AVDecAudioInputPCM**</span></span>              | <span data-ttu-id="c5b92-128">Audio PCM</span><span class="sxs-lookup"><span data-stu-id="c5b92-128">PCM audio</span></span>                                      |
| <span data-ttu-id="c5b92-129">**\_GUID CODECAPI \_ AVDecAudioInputWMA**</span><span class="sxs-lookup"><span data-stu-id="c5b92-129">**CODECAPI\_GUID\_AVDecAudioInputWMA**</span></span>              | <span data-ttu-id="c5b92-130">Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="c5b92-130">Windows Media Audio</span></span>                            |
| <span data-ttu-id="c5b92-131">**\_GUID CODECAPI \_ AVDecAudioInputWMAPro**</span><span class="sxs-lookup"><span data-stu-id="c5b92-131">**CODECAPI\_GUID\_AVDecAudioInputWMAPro**</span></span>           | <span data-ttu-id="c5b92-132">Windows Media Audio 9 professionnel (WMA Pro)</span><span class="sxs-lookup"><span data-stu-id="c5b92-132">Windows Media Audio 9 Professional (WMA Pro)</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="c5b92-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5b92-133">Requirements</span></span>



| <span data-ttu-id="c5b92-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5b92-134">Requirement</span></span> | <span data-ttu-id="c5b92-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5b92-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b92-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5b92-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b92-137">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="c5b92-137">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c5b92-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5b92-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b92-139">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="c5b92-139">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c5b92-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5b92-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5b92-141"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5b92-141"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5b92-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5b92-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b92-143">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="c5b92-143">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c5b92-144">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="c5b92-144">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




