---
description: Spécifie pour un type de support si les données multimédia sont compressées.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: Attribut MF_MT_COMPRESSED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528239"
---
# <a name="mf_mt_compressed-attribute"></a><span data-ttu-id="e142c-103">\_ \_ Attribut compressé MF MT</span><span class="sxs-lookup"><span data-stu-id="e142c-103">MF\_MT\_COMPRESSED attribute</span></span>

<span data-ttu-id="e142c-104">Spécifie pour un type de support si les données multimédia sont compressées.</span><span class="sxs-lookup"><span data-stu-id="e142c-104">Specifies for a media type whether the media data is compressed.</span></span>

## <a name="data-type"></a><span data-ttu-id="e142c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e142c-105">Data type</span></span>

<span data-ttu-id="e142c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e142c-106">**UINT32**</span></span>

<span data-ttu-id="e142c-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="e142c-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e142c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="e142c-108">Remarks</span></span>

<span data-ttu-id="e142c-109">Si cet attribut a la **valeur true**, le type de média est un format compressé.</span><span class="sxs-lookup"><span data-stu-id="e142c-109">If this attribute is **TRUE**, the media type is a compressed format.</span></span> <span data-ttu-id="e142c-110">Dans le cas contraire, le type de média est décompressé ou le type de compression n’est pas connu.</span><span class="sxs-lookup"><span data-stu-id="e142c-110">Otherwise, either the media type is uncompressed or the compression type is not known.</span></span>

<span data-ttu-id="e142c-111">Il n’est pas garanti que cet attribut soit défini sur **true** pour tous les formats compressés, donc les applications ne doivent généralement pas utiliser cet attribut.</span><span class="sxs-lookup"><span data-stu-id="e142c-111">This attribute is not guaranteed to be set to **TRUE** for all compressed formats, so applications should generally not rely this attribute.</span></span> <span data-ttu-id="e142c-112">La méthode la plus fiable pour déterminer si un format est compressé consiste à conserver une liste de formats connus.</span><span class="sxs-lookup"><span data-stu-id="e142c-112">The most reliable way to determine whether a format is compressed is to maintain a list of known formats.</span></span> <span data-ttu-id="e142c-113">Si une application ne reconnaît pas un format, comme spécifié dans l’attribut de [**\_ sous- \_ type MF MT**](mf-mt-subtype-attribute.md) , elle ne doit pas prendre en part la compression du format.</span><span class="sxs-lookup"><span data-stu-id="e142c-113">If an application does not recognize a format, as specified in the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute, it should not assume anything about the compression of the format.</span></span>

<span data-ttu-id="e142c-114">Pour déterminer si un format utilise la compression temporelle (ce qui signifie que certains échantillons sont calculés comme des deltas à partir d’exemples précédents), vérifiez l’attribut de l’attribut [**MF \_ MT \_ All \_ Samples \_ Independent**](mf-mt-all-samples-independent-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e142c-114">To determine whether a format uses temporal compression (meaning that some samples are computed as deltas from earlier samples), check the [**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) attribute.</span></span>

<span data-ttu-id="e142c-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e142c-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e142c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e142c-116">Requirements</span></span>



| <span data-ttu-id="e142c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e142c-117">Requirement</span></span> | <span data-ttu-id="e142c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e142c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e142c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e142c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e142c-120">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="e142c-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e142c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e142c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e142c-122">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="e142c-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e142c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e142c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e142c-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e142c-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e142c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e142c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e142c-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e142c-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e142c-127">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e142c-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e142c-128">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e142c-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e142c-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e142c-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="e142c-130">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="e142c-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




