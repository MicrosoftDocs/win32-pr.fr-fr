---
description: Spécifie si le pipeline tronque les exemples.
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: Attribut MF_TOPOLOGY_NO_MARKIN_MARKOUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201976"
---
# <a name="mf_topology_no_markin_markout-attribute"></a><span data-ttu-id="1fa45-103">L' \_ attribut MARKOUT de la topologie MF \_ n’a pas de \_ marque \_</span><span class="sxs-lookup"><span data-stu-id="1fa45-103">MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT attribute</span></span>

<span data-ttu-id="1fa45-104">Spécifie si le pipeline tronque les exemples.</span><span class="sxs-lookup"><span data-stu-id="1fa45-104">Specifies whether the pipeline trims samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="1fa45-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1fa45-105">Data type</span></span>

<span data-ttu-id="1fa45-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1fa45-106">**UINT32**</span></span>

<span data-ttu-id="1fa45-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="1fa45-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fa45-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1fa45-108">Remarks</span></span>

<span data-ttu-id="1fa45-109">Par défaut, le pipeline tronque les échantillons pour qu’ils correspondent aux durées de présentation appropriées.</span><span class="sxs-lookup"><span data-stu-id="1fa45-109">By default, the pipeline trims samples to match the correct presentation times.</span></span> <span data-ttu-id="1fa45-110">La suppression est effectuée sur les nœuds de topologie qui ont les attributs [**\_ TOPONODE \_ \_**](mf-toponode-markin-here-attribute.md) et [**MF \_ TOPONODE \_ MARKOUT \_ ici**](mf-toponode-markout-here-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1fa45-110">Trimming is done at the topology nodes that have the [**MF\_TOPONODE\_MARKIN\_HERE**](mf-toponode-markin-here-attribute.md) and [**MF\_TOPONODE\_MARKOUT\_HERE**](mf-toponode-markout-here-attribute.md) attributes.</span></span> <span data-ttu-id="1fa45-111">Si l' **attribut \_ \_ \_ \_ MARKOUT de la topologie MF** n’a pas la valeur **true** sur la topologie, le pipeline ne tronque pas les exemples, et les attributs **MF \_ TOPONODE \_ Mark \_ ici** et **MF \_ TOPONODE \_ MARKOUT \_ ici** sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="1fa45-111">If the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute is set to **TRUE** on the topology, the pipeline does not trim samples, and the **MF\_TOPONODE\_MARKIN\_HERE** and **MF\_TOPONODE\_MARKOUT\_HERE** attributes are ignored.</span></span> <span data-ttu-id="1fa45-112">Si l’attribut n’est pas défini, ou a la valeur **false**, le pipeline tronque les exemples.</span><span class="sxs-lookup"><span data-stu-id="1fa45-112">If the attribute is not set, or has the value **FALSE**, the pipeline trims samples.</span></span>

<span data-ttu-id="1fa45-113">Une application peut définir l’attribut MARKOUT de la **\_ topologie MF \_ no \_ Mark \_** by sur **true** si l’application reçoit des exemples compressés du pipeline et doit recevoir toutes les images clés, qui peuvent être tronquées.</span><span class="sxs-lookup"><span data-stu-id="1fa45-113">An application might set the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute to **TRUE** if the application receives compressed samples from the pipeline and needs to get all of the key frames, which might otherwise be trimmed.</span></span>

<span data-ttu-id="1fa45-114">La valeur par défaut de cet attribut est **false**.</span><span class="sxs-lookup"><span data-stu-id="1fa45-114">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="1fa45-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1fa45-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa45-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fa45-116">Requirements</span></span>



| <span data-ttu-id="1fa45-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fa45-117">Requirement</span></span> | <span data-ttu-id="1fa45-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fa45-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa45-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fa45-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa45-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1fa45-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1fa45-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1fa45-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa45-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1fa45-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1fa45-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fa45-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fa45-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa45-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fa45-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fa45-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa45-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1fa45-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1fa45-127">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1fa45-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1fa45-128">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1fa45-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1fa45-129">**\_Mark MF TOPONODE \_ \_ ici**</span><span class="sxs-lookup"><span data-stu-id="1fa45-129">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="1fa45-130">**\_MARKOUT TOPONODE \_ MF \_ ici**</span><span class="sxs-lookup"><span data-stu-id="1fa45-130">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="1fa45-131">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="1fa45-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




