---
description: Spécifie si les topologies ont une heure de début et de fin globale.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: Attribut MF_SESSION_GLOBAL_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535449"
---
# <a name="mf_session_global_time-attribute"></a><span data-ttu-id="508eb-103">\_Attribut de \_ durée globale de session MF \_</span><span class="sxs-lookup"><span data-stu-id="508eb-103">MF\_SESSION\_GLOBAL\_TIME attribute</span></span>

<span data-ttu-id="508eb-104">Spécifie si les topologies ont une heure de début et de fin globale.</span><span class="sxs-lookup"><span data-stu-id="508eb-104">Specifies whether topologies have a global start and stop time.</span></span>

## <a name="data-type"></a><span data-ttu-id="508eb-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="508eb-105">Data type</span></span>

<span data-ttu-id="508eb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="508eb-106">**UINT32**</span></span>

<span data-ttu-id="508eb-107">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="508eb-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="508eb-108">Notes</span><span class="sxs-lookup"><span data-stu-id="508eb-108">Remarks</span></span>

<span data-ttu-id="508eb-109">Vous pouvez définir cet attribut lorsque vous créez le média sesison à l’aide du paramètre *pConfiguration* de la fonction [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="508eb-109">You can set this attribute when you create the media sesison by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="508eb-110">Si cet attribut est présent et différent de zéro, toutes les topologies transmises à la session de média doivent avoir les attributs de topologie [**MF \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) et de [**\_ topologie MF \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="508eb-110">If this attribute is present and nonzero, then all topologies passed to the Media Session must have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) and [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attributes.</span></span> <span data-ttu-id="508eb-111">Ces attributs spécifient les heures de début et de fin de la topologie par rapport à l’ensemble de la présentation.</span><span class="sxs-lookup"><span data-stu-id="508eb-111">These attributes specify the start and stop times for the topology relative to the entire presentation.</span></span>

<span data-ttu-id="508eb-112">Si cet attribut est absent ou **false**, les topologies ne doivent pas avoir l’attribut de topologie [**MF \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) ou MF de topologie [**MF \_ \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="508eb-112">If this attribute is absent or **FALSE**, the topologies must not have the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) or [**MF\_TOPOLOGY\_PROJECTSTOP**](mf-topology-projectstop-attribute.md) attribute.</span></span>

<span data-ttu-id="508eb-113">Utilisez cet attribut pour créer des séquences de modification.</span><span class="sxs-lookup"><span data-stu-id="508eb-113">Use this attribute to create editing sequences.</span></span> <span data-ttu-id="508eb-114">Pour plus d’informations, consultez [durée de présentation des séquences](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="508eb-114">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="508eb-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="508eb-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="508eb-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="508eb-116">Requirements</span></span>



| <span data-ttu-id="508eb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="508eb-117">Requirement</span></span> | <span data-ttu-id="508eb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="508eb-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="508eb-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="508eb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="508eb-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="508eb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="508eb-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="508eb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="508eb-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="508eb-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="508eb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="508eb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="508eb-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="508eb-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="508eb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="508eb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="508eb-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="508eb-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="508eb-127">Attributs de session multimédia</span><span class="sxs-lookup"><span data-stu-id="508eb-127">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="508eb-128">Durée des présentations de séquence</span><span class="sxs-lookup"><span data-stu-id="508eb-128">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="508eb-129">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="508eb-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="508eb-130">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="508eb-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="508eb-131">**\_PROJECTSTART de topologie \_ MF**</span><span class="sxs-lookup"><span data-stu-id="508eb-131">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> <dt>

[<span data-ttu-id="508eb-132">**\_PROJECTSTOP de topologie \_ MF**</span><span class="sxs-lookup"><span data-stu-id="508eb-132">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




