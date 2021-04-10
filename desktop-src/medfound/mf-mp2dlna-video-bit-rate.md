---
description: Spécifie la vitesse de transmission vidéo maximale pour le récepteur multimédia DLNA (Digital vivant Network Alliance).
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: Attribut MF_MP2DLNA_VIDEO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201986"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a><span data-ttu-id="ad201-103">\_Attribut de \_ \_ vitesse de transmission vidéo MP2DLNA MF \_</span><span class="sxs-lookup"><span data-stu-id="ad201-103">MF\_MP2DLNA\_VIDEO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="ad201-104">Spécifie la vitesse de transmission vidéo maximale pour le récepteur multimédia DLNA (Digital vivant Network Alliance).</span><span class="sxs-lookup"><span data-stu-id="ad201-104">Specifies the maximum video bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad201-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ad201-105">Data type</span></span>

<span data-ttu-id="ad201-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ad201-106">**UINT32**</span></span>

<span data-ttu-id="ad201-107">La valeur est la vitesse de transmission maximale cible pour le flux vidéo encodé, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="ad201-107">The value is the target maximum bit rate for the encoded video stream, in bits per second.</span></span> <span data-ttu-id="ad201-108">La valeur maximale est 9,8 millions (9,8 Mbits/s), qui est également la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad201-108">The maximum value is 9800000 (9.8 Mbps), which is also the default value.</span></span>

## <a name="getset"></a><span data-ttu-id="ad201-109">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="ad201-109">Get/set</span></span>

<span data-ttu-id="ad201-110">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ad201-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ad201-111">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ad201-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad201-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ad201-112">Remarks</span></span>

<span data-ttu-id="ad201-113">Pour définir cet attribut sur le récepteur multimédia DLNA, interrogez le récepteur multimédia pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="ad201-113">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="ad201-114">Définissez l’attribut avant le début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="ad201-114">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad201-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad201-115">Requirements</span></span>



| <span data-ttu-id="ad201-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad201-116">Requirement</span></span> | <span data-ttu-id="ad201-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad201-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad201-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad201-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ad201-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad201-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ad201-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad201-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ad201-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad201-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ad201-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad201-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad201-123"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad201-123"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad201-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad201-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad201-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad201-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




