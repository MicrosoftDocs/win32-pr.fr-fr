---
description: Spécifie l’entrée actuelle dans la zone de description de l’exemple pour un type de média MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: Attribut MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530635"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a><span data-ttu-id="b879d-103">\_Attribut d' \_ entrée d’exemple de \_ \_ \_ ligne de code MPEG4 MF</span><span class="sxs-lookup"><span data-stu-id="b879d-103">MF\_MT\_MPEG4\_CURRENT\_SAMPLE\_ENTRY attribute</span></span>

<span data-ttu-id="b879d-104">Spécifie l’entrée actuelle dans la zone de description de l’exemple pour un type de média MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="b879d-104">Specifies the current entry in the sample description box for an MPEG-4 media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="b879d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b879d-105">Data type</span></span>

<span data-ttu-id="b879d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b879d-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b879d-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="b879d-107">Get/set</span></span>

<span data-ttu-id="b879d-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b879d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b879d-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b879d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b879d-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="b879d-110">Applies to</span></span>

[<span data-ttu-id="b879d-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b879d-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="b879d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b879d-112">Remarks</span></span>

<span data-ttu-id="b879d-113">Dans un fichier MP4 ou 3GP, la zone Description de l’exemple décrit l’encodage utilisé pour un flux dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="b879d-113">In an MP4 or 3GP file, the sample description box describes the encoding used for a stream in the file.</span></span> <span data-ttu-id="b879d-114">La zone Description de l’exemple peut contenir plusieurs entrées.</span><span class="sxs-lookup"><span data-stu-id="b879d-114">The sample description box can contain multiple entries.</span></span> <span data-ttu-id="b879d-115">Cet attribut spécifie l’entrée à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b879d-115">This attribute specifies which entry to use.</span></span> <span data-ttu-id="b879d-116">La valeur est un index de base zéro dans la liste.</span><span class="sxs-lookup"><span data-stu-id="b879d-116">The value is a zero-based index into the list.</span></span>

<span data-ttu-id="b879d-117">Actuellement, la seule valeur prise en charge est 0.</span><span class="sxs-lookup"><span data-stu-id="b879d-117">Currently, the only supported value is 0.</span></span> <span data-ttu-id="b879d-118">L’attribut a été défini pour une future extensibilité.</span><span class="sxs-lookup"><span data-stu-id="b879d-118">The attribute has been defined for future extensibility.</span></span>

<span data-ttu-id="b879d-119">La source du fichier MPEG-4 définit toujours la valeur sur 0.</span><span class="sxs-lookup"><span data-stu-id="b879d-119">The MPEG-4 file source always sets the value to 0.</span></span> <span data-ttu-id="b879d-120">Les récepteurs de fichiers MP4 et 3GP ignorent la valeur de cet attribut si elle est présente.</span><span class="sxs-lookup"><span data-stu-id="b879d-120">The MP4 and 3GP file sinks ignore the value of this attribute if it is present.</span></span>

<span data-ttu-id="b879d-121">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b879d-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b879d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b879d-122">Requirements</span></span>



| <span data-ttu-id="b879d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b879d-123">Requirement</span></span> | <span data-ttu-id="b879d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b879d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b879d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b879d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b879d-126">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b879d-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b879d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b879d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b879d-128">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b879d-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b879d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="b879d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b879d-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b879d-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b879d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b879d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b879d-132">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b879d-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b879d-133">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="b879d-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="b879d-134">\_Exemple de \_ Description du MPEG4 MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="b879d-134">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION</span></span>](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




