---
description: Spécifie l’heure de début de la présentation.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: Attribut MF_TOPONODE_MEDIASTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab00727cc328bfd6ba780050160fb21eecbb96f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525796"
---
# <a name="mf_toponode_mediastart-attribute"></a><span data-ttu-id="41124-103">\_ \_ Attribut MEDIASTART TOPONODE MF</span><span class="sxs-lookup"><span data-stu-id="41124-103">MF\_TOPONODE\_MEDIASTART attribute</span></span>

<span data-ttu-id="41124-104">Spécifie l’heure de début de la présentation.</span><span class="sxs-lookup"><span data-stu-id="41124-104">Specifies the start time of the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="41124-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="41124-105">Data type</span></span>

<span data-ttu-id="41124-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="41124-106">**UINT64**</span></span>

<span data-ttu-id="41124-107">Traiter en tant que valeur **LongLong** .</span><span class="sxs-lookup"><span data-stu-id="41124-107">Treat as a **LONGLONG** value.</span></span>

## <a name="getset"></a><span data-ttu-id="41124-108">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="41124-108">Get/set</span></span>

<span data-ttu-id="41124-109">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="41124-109">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="41124-110">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="41124-110">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="41124-111">S’applique à</span><span class="sxs-lookup"><span data-stu-id="41124-111">Applies to</span></span>

[<span data-ttu-id="41124-112">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="41124-112">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a><span data-ttu-id="41124-113">Notes</span><span class="sxs-lookup"><span data-stu-id="41124-113">Remarks</span></span>

<span data-ttu-id="41124-114">Cet attribut spécifie la position dans la source où la lecture commence, en unités de 100 nanosecondes, par rapport au démarrage de la source.</span><span class="sxs-lookup"><span data-stu-id="41124-114">This attribute specifies the position in the source where playback starts, in 100-nanosecond units, relative to the start the source.</span></span> <span data-ttu-id="41124-115">Si l’attribut n’est pas défini, la lecture commence à zéro (le début du fichier).</span><span class="sxs-lookup"><span data-stu-id="41124-115">If the attribute is not set, playback starts at zero (the start of the file).</span></span> <span data-ttu-id="41124-116">Par exemple, pour démarrer la lecture à la marque de 5 secondes, définissez cet attribut sur 50 millions.</span><span class="sxs-lookup"><span data-stu-id="41124-116">For example, to start playback at the 5-second mark, set this attribute to 50000000.</span></span> <span data-ttu-id="41124-117">Définissez l’attribut sur les nœuds sources dans la topologie (nœuds avec le type égal à **\_ nœud de topologie MF \_ \_ SOURCESTREAM**).</span><span class="sxs-lookup"><span data-stu-id="41124-117">Set the attribute on the source nodes in the topology (nodes with type equal to **MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="41124-118">Définissez l’attribut avant d’appeler [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="41124-118">Set the attribute before calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

> [!Note]  
> <span data-ttu-id="41124-119">Si vous insérez manuellement un décodeur dans la topologie, vous devez également définir les attributs [MF \_ TOPONODE \_ Mark \_ ici](mf-toponode-markin-here-attribute.md) et [MF \_ TOPONODE \_ MARKOUT \_ ici](mf-toponode-markout-here-attribute.md) sur le nœud décodeur.</span><span class="sxs-lookup"><span data-stu-id="41124-119">If you manually insert a decoder into the topology, you must also set the [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) and [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) attributes on the decoder node.</span></span>

 

<span data-ttu-id="41124-120">Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="41124-120">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="41124-121">Toutefois, les valeurs négatives ne sont pas significatives.</span><span class="sxs-lookup"><span data-stu-id="41124-121">However, negative values are not meaningful.</span></span>

<span data-ttu-id="41124-122">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="41124-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="41124-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41124-123">Requirements</span></span>



| <span data-ttu-id="41124-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41124-124">Requirement</span></span> | <span data-ttu-id="41124-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="41124-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41124-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41124-126">Minimum supported client</span></span><br/> | <span data-ttu-id="41124-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41124-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="41124-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41124-128">Minimum supported server</span></span><br/> | <span data-ttu-id="41124-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41124-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="41124-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="41124-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="41124-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41124-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41124-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41124-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41124-133">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="41124-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="41124-134">Durée des présentations de séquence</span><span class="sxs-lookup"><span data-stu-id="41124-134">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="41124-135">Attributs de nœud de topologie</span><span class="sxs-lookup"><span data-stu-id="41124-135">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="41124-136">**\_MEDIASTOP TOPONODE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="41124-136">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




