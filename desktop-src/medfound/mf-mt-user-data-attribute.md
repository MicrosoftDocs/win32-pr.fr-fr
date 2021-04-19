---
description: Contient des données de format supplémentaires pour un type de média.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: Attribut MF_MT_USER_DATA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6042ded0e2d441b0f86c5e1f97557959ce08cd1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543525"
---
# <a name="mf_mt_user_data-attribute"></a><span data-ttu-id="af871-103">\_Attribut de \_ données utilisateur MF MT \_</span><span class="sxs-lookup"><span data-stu-id="af871-103">MF\_MT\_USER\_DATA attribute</span></span>

<span data-ttu-id="af871-104">Contient des données de format supplémentaires pour un type de média.</span><span class="sxs-lookup"><span data-stu-id="af871-104">Contains additional format data for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="af871-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="af871-105">Data type</span></span>

<span data-ttu-id="af871-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="af871-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="af871-107">Notes</span><span class="sxs-lookup"><span data-stu-id="af871-107">Remarks</span></span>

<span data-ttu-id="af871-108">La signification des données dans cet attribut dépend du format décrit par le type de média.</span><span class="sxs-lookup"><span data-stu-id="af871-108">The meaning of the data in this attribute depends on the format that is described by the media type.</span></span>



| <span data-ttu-id="af871-109">Type de format</span><span class="sxs-lookup"><span data-stu-id="af871-109">Format Type</span></span>                                                                                                           | <span data-ttu-id="af871-110">Données de format supplémentaires</span><span class="sxs-lookup"><span data-stu-id="af871-110">Additional Format Data</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af871-111">Codec Windows Media.</span><span class="sxs-lookup"><span data-stu-id="af871-111">Windows Media codec.</span></span>                                                                                                  | <span data-ttu-id="af871-112">Données privées du codec.</span><span class="sxs-lookup"><span data-stu-id="af871-112">Codec private data.</span></span>                                                                                                                       |
| <span data-ttu-id="af871-113">La structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) a été convertie.</span><span class="sxs-lookup"><span data-stu-id="af871-113">Converted [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span>   | <span data-ttu-id="af871-114">Données supplémentaires qui apparaissent après la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , à l’exclusion de la table de couleurs ou des masques de couleur.</span><span class="sxs-lookup"><span data-stu-id="af871-114">Extra data that appears after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, not including the color table or color masks.</span></span> |
| <span data-ttu-id="af871-115">La structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ou [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) a été convertie.</span><span class="sxs-lookup"><span data-stu-id="af871-115">Converted [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> | <span data-ttu-id="af871-116">Données supplémentaires qui apparaissent après la structure du format audio.</span><span class="sxs-lookup"><span data-stu-id="af871-116">Extra data that appears after the audio format structure.</span></span>                                                                                 |



 

<span data-ttu-id="af871-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="af871-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="af871-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af871-118">Requirements</span></span>



| <span data-ttu-id="af871-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af871-119">Requirement</span></span> | <span data-ttu-id="af871-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="af871-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af871-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af871-121">Minimum supported client</span></span><br/> | <span data-ttu-id="af871-122">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="af871-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="af871-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af871-123">Minimum supported server</span></span><br/> | <span data-ttu-id="af871-124">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="af871-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="af871-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="af871-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="af871-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="af871-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af871-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af871-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af871-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="af871-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="af871-129">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="af871-129">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="af871-130">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="af871-130">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="af871-131">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="af871-131">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="af871-132">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="af871-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
