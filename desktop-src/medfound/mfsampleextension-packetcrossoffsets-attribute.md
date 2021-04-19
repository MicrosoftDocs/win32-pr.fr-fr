---
description: Spécifie les décalages aux limites de charge utile dans un frame pour les exemples protégés.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: Attribut MFSampleExtension_PacketCrossOffsets (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416f41fef9caab3d73c2bdd015d345452ccbd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520432"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a><span data-ttu-id="ce6ba-103">\_Attribut MFSampleExtension PacketCrossOffsets</span><span class="sxs-lookup"><span data-stu-id="ce6ba-103">MFSampleExtension\_PacketCrossOffsets attribute</span></span>

<span data-ttu-id="ce6ba-104">Spécifie les décalages aux limites de charge utile dans un frame pour les exemples protégés.</span><span class="sxs-lookup"><span data-stu-id="ce6ba-104">Specifies the offsets to the payload boundaries in a frame for protected samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="ce6ba-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ce6ba-105">Data type</span></span>

<span data-ttu-id="ce6ba-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="ce6ba-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="ce6ba-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="ce6ba-107">Get/set</span></span>

<span data-ttu-id="ce6ba-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="ce6ba-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="ce6ba-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="ce6ba-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ce6ba-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="ce6ba-110">Applies to</span></span>

[<span data-ttu-id="ce6ba-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="ce6ba-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="ce6ba-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ce6ba-112">Remarks</span></span>

<span data-ttu-id="ce6ba-113">Cet attribut s’applique aux exemples de médias protégés par Windows Media Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="ce6ba-113">This attribute applies to media samples protected by Windows Media Digital Rights Management (DRM).</span></span> <span data-ttu-id="ce6ba-114">La valeur de l’attribut est un tableau de **DWORD** s.</span><span class="sxs-lookup"><span data-stu-id="ce6ba-114">The value of the attribute is an array of **DWORD** s.</span></span> <span data-ttu-id="ce6ba-115">Chaque entrée du tableau correspond au décalage d’une limite de charge utile, par rapport au début du frame.</span><span class="sxs-lookup"><span data-stu-id="ce6ba-115">Each entry in the array is the offset of a payload boundary, relative to the start of the frame.</span></span> <span data-ttu-id="ce6ba-116">Une application peut utiliser ces valeurs lors du déchiffrement et de la reconstruction des frames.</span><span class="sxs-lookup"><span data-stu-id="ce6ba-116">An application can use these values when decrypting and reconstructing the frames.</span></span>

<span data-ttu-id="ce6ba-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ce6ba-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce6ba-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce6ba-118">Requirements</span></span>



| <span data-ttu-id="ce6ba-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce6ba-119">Requirement</span></span> | <span data-ttu-id="ce6ba-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce6ba-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6ba-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce6ba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6ba-122">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="ce6ba-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="ce6ba-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce6ba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6ba-124">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="ce6ba-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ce6ba-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce6ba-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce6ba-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce6ba-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce6ba-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce6ba-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6ba-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce6ba-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce6ba-129">Séparateur ASF</span><span class="sxs-lookup"><span data-stu-id="ce6ba-129">ASF Splitter</span></span>](asf-splitter.md)
</dt> <dt>

[<span data-ttu-id="ce6ba-130">Exemples d’attributs</span><span class="sxs-lookup"><span data-stu-id="ce6ba-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce6ba-131">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="ce6ba-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




