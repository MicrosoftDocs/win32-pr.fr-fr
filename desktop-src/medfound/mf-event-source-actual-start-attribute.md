---
description: Contient l’heure de début à laquelle une source du média redémarre à partir de sa position actuelle.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: Attribut MF_EVENT_SOURCE_ACTUAL_START (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393556"
---
# <a name="mf_event_source_actual_start-attribute"></a><span data-ttu-id="37645-103">\_Attribut de \_ \_ début réel \_ de la source de l’événement MF</span><span class="sxs-lookup"><span data-stu-id="37645-103">MF\_EVENT\_SOURCE\_ACTUAL\_START attribute</span></span>

<span data-ttu-id="37645-104">Contient l’heure de début à laquelle une source du média redémarre à partir de sa position actuelle.</span><span class="sxs-lookup"><span data-stu-id="37645-104">Contains the start time at which a media source restarts from its current position.</span></span>

## <a name="data-type"></a><span data-ttu-id="37645-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="37645-105">Data type</span></span>

<span data-ttu-id="37645-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="37645-106">**UINT64**</span></span>

<span data-ttu-id="37645-107">Traiter en tant que valeur **LongLong** .</span><span class="sxs-lookup"><span data-stu-id="37645-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37645-108">Notes</span><span class="sxs-lookup"><span data-stu-id="37645-108">Remarks</span></span>

<span data-ttu-id="37645-109">Cet attribut est utilisé avec l’événement [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="37645-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="37645-110">L’attribut est pertinent lorsque les données d’événement sont vides (**VT \_ vide**), ce qui indique que la source du média a démarré à partir de la position de lecture actuelle.</span><span class="sxs-lookup"><span data-stu-id="37645-110">The attribute is relevant when the event data is empty (**VT\_EMPTY**), which indicates that the media source started from the current playback position.</span></span> <span data-ttu-id="37645-111">Dans ce cas, l’attribut de **\_ \_ \_ \_ début réel de la source d’événements MF** spécifie l’heure de début réelle.</span><span class="sxs-lookup"><span data-stu-id="37645-111">In that case, the **MF\_EVENT\_SOURCE\_ACTUAL\_START** attribute specifies the actual starting time.</span></span> <span data-ttu-id="37645-112">Si les données d’événement sont des données **VT \_ vides** et que cet attribut n’est pas défini, l’heure de début est supposée être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="37645-112">If the event data is **VT\_EMPTY** and this attribute is not set, the starting time is assumed to be zero.</span></span>

<span data-ttu-id="37645-113">Lorsque les données d’événement [MESourceStarted](mesourcestarted.md) contiennent l’heure de début (**VT \_ i8**), cet attribut ne doit pas être défini.</span><span class="sxs-lookup"><span data-stu-id="37645-113">When the [MESourceStarted](mesourcestarted.md) event data contains the start time (**VT\_I8**), this attribute should not be set.</span></span>

<span data-ttu-id="37645-114">Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="37645-114">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="37645-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="37645-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="37645-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37645-116">Requirements</span></span>



| <span data-ttu-id="37645-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37645-117">Requirement</span></span> | <span data-ttu-id="37645-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="37645-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37645-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37645-119">Minimum supported client</span></span><br/> | <span data-ttu-id="37645-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37645-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="37645-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37645-121">Minimum supported server</span></span><br/> | <span data-ttu-id="37645-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37645-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="37645-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="37645-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="37645-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="37645-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37645-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37645-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37645-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37645-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="37645-127">Attributs d'événement</span><span class="sxs-lookup"><span data-stu-id="37645-127">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="37645-128">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="37645-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="37645-129">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="37645-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




