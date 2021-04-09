---
description: Spécifie la vitesse de transmission audio maximale pour le récepteur multimédia DLNA (Digital vivant Network Alliance).
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: Attribut MF_MP2DLNA_AUDIO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c61554f592aefbb863057339d807e23fc96567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951538"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a><span data-ttu-id="09662-103">\_Attribut de \_ \_ vitesse de bits audio MF MP2DLNA \_</span><span class="sxs-lookup"><span data-stu-id="09662-103">MF\_MP2DLNA\_AUDIO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="09662-104">Spécifie la vitesse de transmission audio maximale pour le récepteur multimédia DLNA (Digital vivant Network Alliance).</span><span class="sxs-lookup"><span data-stu-id="09662-104">Specifies the maximum audio bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="09662-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="09662-105">Data type</span></span>

<span data-ttu-id="09662-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="09662-106">**UINT32**</span></span>

<span data-ttu-id="09662-107">La valeur est la vitesse de transmission maximale cible pour le flux audio encodé, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="09662-107">The value is the target maximum bit rate for the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="09662-108">La valeur doit être l’une des vitesses de transmission autorisées pour l’audio MPEG-2 Layer 2 pour DLNA.</span><span class="sxs-lookup"><span data-stu-id="09662-108">The value must be one of the bit rates allowed for MPEG-2 layer 2 audio for DLNA.</span></span> <span data-ttu-id="09662-109">La valeur par défaut est 192000 (192 Kbits/s).</span><span class="sxs-lookup"><span data-stu-id="09662-109">The default value is 192000 (192 Kbps).</span></span>

## <a name="getset"></a><span data-ttu-id="09662-110">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="09662-110">Get/set</span></span>

<span data-ttu-id="09662-111">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="09662-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="09662-112">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="09662-112">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="09662-113">Notes</span><span class="sxs-lookup"><span data-stu-id="09662-113">Remarks</span></span>

<span data-ttu-id="09662-114">Pour définir cet attribut sur le récepteur multimédia DLNA, interrogez le récepteur multimédia pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="09662-114">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="09662-115">Définissez l’attribut avant le début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="09662-115">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="09662-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09662-116">Requirements</span></span>



| <span data-ttu-id="09662-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09662-117">Requirement</span></span> | <span data-ttu-id="09662-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="09662-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09662-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09662-119">Minimum supported client</span></span><br/> | <span data-ttu-id="09662-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09662-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="09662-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09662-121">Minimum supported server</span></span><br/> | <span data-ttu-id="09662-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09662-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="09662-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="09662-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="09662-124"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="09662-124"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09662-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09662-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09662-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="09662-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




