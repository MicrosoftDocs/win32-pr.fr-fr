---
description: Spécifie le profil et le niveau audio d’un flux de codage audio avancé (AAC).
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: Attribut MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116bfc2b41cff3cbd92fc9a60be150ea598e1cc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533211"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a><span data-ttu-id="35a9f-103">\_Attribut d' \_ \_ indication du \_ niveau de profil audio \_ MF MT AAC \_</span><span class="sxs-lookup"><span data-stu-id="35a9f-103">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION attribute</span></span>

<span data-ttu-id="35a9f-104">Spécifie le profil et le niveau audio d’un flux de codage audio avancé (AAC).</span><span class="sxs-lookup"><span data-stu-id="35a9f-104">Specifies the audio profile and level of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="35a9f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="35a9f-105">Data type</span></span>

<span data-ttu-id="35a9f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="35a9f-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="35a9f-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="35a9f-107">Get/set</span></span>

<span data-ttu-id="35a9f-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="35a9f-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="35a9f-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="35a9f-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="35a9f-110">S'applique à</span><span class="sxs-lookup"><span data-stu-id="35a9f-110">Applies To</span></span>

[<span data-ttu-id="35a9f-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="35a9f-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="35a9f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="35a9f-112">Remarks</span></span>

<span data-ttu-id="35a9f-113">Cet attribut contient la valeur du champ **audioProfileLevelIndication** , tel que défini par la norme ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="35a9f-113">This attribute contains the value of the **audioProfileLevelIndication** field, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="35a9f-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="35a9f-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="35a9f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35a9f-115">Requirements</span></span>



| <span data-ttu-id="35a9f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35a9f-116">Requirement</span></span> | <span data-ttu-id="35a9f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="35a9f-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35a9f-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="35a9f-118">Header</span></span><br/> | <dl> <span data-ttu-id="35a9f-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a9f-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a9f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35a9f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a9f-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35a9f-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="35a9f-122">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="35a9f-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




