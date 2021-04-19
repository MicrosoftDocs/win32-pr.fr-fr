---
description: Spécifie un nombre compris entre 0 et 100 qui indique le compromis entre la qualité d’encodage et la vitesse d’encodage.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: Attribut MF_TRANSCODE_QUALITYVSSPEED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4d95fab92276e926189c885dad2ecb8f164a97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535327"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a><span data-ttu-id="2e6a0-103">\_Attribut QUALITYVSSPEED de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="2e6a0-103">MF\_TRANSCODE\_QUALITYVSSPEED attribute</span></span>

<span data-ttu-id="2e6a0-104">Spécifie un nombre compris entre 0 et 100 qui indique le compromis entre la qualité d’encodage et la vitesse d’encodage.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-104">Specifies a number between 0 and 100 that indicates the tradeoff between encoding quality and encoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="2e6a0-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2e6a0-105">Data type</span></span>

<span data-ttu-id="2e6a0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2e6a0-106">**UINT32**</span></span>

<span data-ttu-id="2e6a0-107">La valeur de cette propriété est comprise dans la plage suivante.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-107">The value of this property has the following range.</span></span>



| <span data-ttu-id="2e6a0-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e6a0-108">Value</span></span>                                                                          | <span data-ttu-id="2e6a0-109">Signification</span><span class="sxs-lookup"><span data-stu-id="2e6a0-109">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="2e6a0-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2e6a0-110"><dt>0</dt></span></span> </dl>   | <span data-ttu-id="2e6a0-111">Une qualité inférieure, un encodage plus rapide.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-111">Lower quality, faster encoding.</span></span><br/>  |
| <dl> <span data-ttu-id="2e6a0-112"><dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="2e6a0-112"><dt>100</dt></span></span> </dl> | <span data-ttu-id="2e6a0-113">Qualité supérieure, encodage plus lent.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-113">Higher quality, slower encoding.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="2e6a0-114">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="2e6a0-114">Get/set</span></span>

<span data-ttu-id="2e6a0-115">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="2e6a0-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="2e6a0-116">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="2e6a0-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e6a0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2e6a0-117">Remarks</span></span>

<span data-ttu-id="2e6a0-118">Cet attribut a la même valeur GUID que la propriété [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) définie pour [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)et a la même interprétation.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-118">This attribute has the same GUID value as the [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) property defined for [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi), and has the same interpretation.</span></span>

<span data-ttu-id="2e6a0-119">L’application peut définir cet attribut sur le profil de transcodage avant de générer la topologie de transcodage pour les codecs Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-119">The application can set this attribute on the transcode profile before building the transcode topology for Windows Media codecs.</span></span> <span data-ttu-id="2e6a0-120">La valeur doit être comprise entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-120">The value must be in the range from 0 to 100.</span></span> <span data-ttu-id="2e6a0-121">Pour le flux vidéo, le générateur de topologie de transcodage mappe une valeur à la valeur spécifiée par l’application et fournit la valeur mappée à la propriété **MFPKEY \_ COMPLEXITYEX** de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-121">For video stream, the transcode topology builder maps a value to the application-specified value and supplies the mapped value to the **MFPKEY\_COMPLEXITYEX** property of the encoder.</span></span> <span data-ttu-id="2e6a0-122">Des valeurs inférieures permettent à l’encodeur d’utiliser des algorithmes d’encodage moins compliqués.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-122">Lower values enable the encoder to use less complicated encoding algorithms.</span></span> <span data-ttu-id="2e6a0-123">L’utilisation d’algorithmes plus simples produit une sortie de qualité inférieure, mais le processus d’encodage est plus rapide et nécessite moins de puissance de traitement.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-123">Using simpler algorithms produces lower-quality output, but the encoding process is faster and requires less processing power.</span></span>

<span data-ttu-id="2e6a0-124">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2e6a0-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e6a0-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e6a0-125">Requirements</span></span>



| <span data-ttu-id="2e6a0-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e6a0-126">Requirement</span></span> | <span data-ttu-id="2e6a0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e6a0-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6a0-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e6a0-128">Header</span></span><br/> | <dl> <span data-ttu-id="2e6a0-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e6a0-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e6a0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e6a0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e6a0-131">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2e6a0-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2e6a0-132">API de transcodage</span><span class="sxs-lookup"><span data-stu-id="2e6a0-132">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="2e6a0-133">**IMFTranscodeProfile::SetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="2e6a0-133">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
