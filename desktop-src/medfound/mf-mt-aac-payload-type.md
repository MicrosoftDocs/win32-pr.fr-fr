---
description: Spécifie le type de charge utile d’un flux d’encodage audio avancé (AAC).
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: Attribut MF_MT_AAC_PAYLOAD_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525350"
---
# <a name="mf_mt_aac_payload_type-attribute"></a><span data-ttu-id="5d9ea-103">\_Attribut de \_ \_ type de charge utile MT MT AAC \_</span><span class="sxs-lookup"><span data-stu-id="5d9ea-103">MF\_MT\_AAC\_PAYLOAD\_TYPE attribute</span></span>

<span data-ttu-id="5d9ea-104">Spécifie le type de charge utile d’un flux d’encodage audio avancé (AAC).</span><span class="sxs-lookup"><span data-stu-id="5d9ea-104">Specifies the payload type of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="5d9ea-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5d9ea-105">Data type</span></span>

<span data-ttu-id="5d9ea-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5d9ea-106">**UINT32**</span></span>

<span data-ttu-id="5d9ea-107">Les valeurs suivantes sont possibles.</span><span class="sxs-lookup"><span data-stu-id="5d9ea-107">The following values are possible.</span></span>



| <span data-ttu-id="5d9ea-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d9ea-108">Value</span></span>                                                                        | <span data-ttu-id="5d9ea-109">Signification</span><span class="sxs-lookup"><span data-stu-id="5d9ea-109">Meaning</span></span>                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d9ea-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5d9ea-110"><dt>0</dt></span></span> </dl> | <span data-ttu-id="5d9ea-111">Le flux contient uniquement des éléments de bloc de données brutes \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5d9ea-111">The stream contains raw\_data\_block elements only.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="5d9ea-112"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5d9ea-112"><dt>1</dt></span></span> </dl> | <span data-ttu-id="5d9ea-113">Flux de transport des données audio (ADTS).</span><span class="sxs-lookup"><span data-stu-id="5d9ea-113">Audio Data Transport Stream (ADTS).</span></span> <span data-ttu-id="5d9ea-114">Le flux contient une \_ séquence ADTS, telle que définie par MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="5d9ea-114">The stream contains an adts\_sequence, as defined by MPEG-2.</span></span><br/>                       |
| <dl> <span data-ttu-id="5d9ea-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5d9ea-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5d9ea-116">Format d’échange de données audio (ADIF).</span><span class="sxs-lookup"><span data-stu-id="5d9ea-116">Audio Data Interchange Format (ADIF).</span></span> <span data-ttu-id="5d9ea-117">Le flux contient une \_ séquence ADIF, telle que définie par MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="5d9ea-117">The stream contains an adif\_sequence, as defined by MPEG-2.</span></span><br/>                     |
| <dl> <span data-ttu-id="5d9ea-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5d9ea-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="5d9ea-119">Le flux contient un flux de transport audio MPEG-4 avec une couche de synchronisation (garantie) et une couche multiplex (LATM).</span><span class="sxs-lookup"><span data-stu-id="5d9ea-119">The stream contains an MPEG-4 audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="5d9ea-120">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="5d9ea-120">Get/set</span></span>

<span data-ttu-id="5d9ea-121">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5d9ea-121">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5d9ea-122">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="5d9ea-122">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5d9ea-123">S'applique à</span><span class="sxs-lookup"><span data-stu-id="5d9ea-123">Applies To</span></span>

[<span data-ttu-id="5d9ea-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5d9ea-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="5d9ea-125">Notes</span><span class="sxs-lookup"><span data-stu-id="5d9ea-125">Remarks</span></span>

<span data-ttu-id="5d9ea-126">Le \_ type de charge utile de l’option MF MT \_ AAC \_ \_ est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5d9ea-126">MF\_MT\_AAC\_PAYLOAD\_TYPE is optional.</span></span> <span data-ttu-id="5d9ea-127">Si cet attribut n’est pas spécifié, la valeur par défaut 0 est utilisée, qui spécifie que le flux contient uniquement des éléments de bloc de données brutes \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5d9ea-127">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw\_data\_block elements only.</span></span>

<span data-ttu-id="5d9ea-128">S’applique uniquement à **MFAudioFormat \_ AAC**.</span><span class="sxs-lookup"><span data-stu-id="5d9ea-128">Applies only to **MFAudioFormat\_AAC**.</span></span>

<span data-ttu-id="5d9ea-129">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5d9ea-129">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d9ea-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d9ea-130">Requirements</span></span>



| <span data-ttu-id="5d9ea-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d9ea-131">Requirement</span></span> | <span data-ttu-id="5d9ea-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d9ea-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d9ea-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d9ea-133">Header</span></span><br/> | <dl> <span data-ttu-id="5d9ea-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d9ea-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d9ea-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d9ea-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d9ea-136">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5d9ea-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5d9ea-137">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="5d9ea-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




