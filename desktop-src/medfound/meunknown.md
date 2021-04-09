---
description: Type d’événement inconnu. Vous pouvez utiliser cette valeur pour initialiser des variables de type MediaEventType, mais un composant ne doit jamais déclencher l’événement MEUnknown.
ms.assetid: 786b69f4-8713-41db-829a-c13512baa3f1
title: Événement MEUnknown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a768fde2939b7e32ed8d1007d2988c2e54cc6726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951546"
---
# <a name="meunknown-event"></a><span data-ttu-id="ec55b-104">Événement MEUnknown</span><span class="sxs-lookup"><span data-stu-id="ec55b-104">MEUnknown event</span></span>

<span data-ttu-id="ec55b-105">Type d’événement inconnu.</span><span class="sxs-lookup"><span data-stu-id="ec55b-105">Unknown event type.</span></span> <span data-ttu-id="ec55b-106">Vous pouvez utiliser cette valeur pour initialiser des variables de type **MediaEventType**, mais un composant ne doit jamais déclencher l’événement MEUnknown</span><span class="sxs-lookup"><span data-stu-id="ec55b-106">You can use this value to initialize variables of type **MediaEventType**, but a component should never raise the MEUnknown event</span></span>

## <a name="event-values"></a><span data-ttu-id="ec55b-107">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="ec55b-107">Event values</span></span>

<span data-ttu-id="ec55b-108">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="ec55b-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ec55b-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ec55b-109">VARTYPE</span></span>              | <span data-ttu-id="ec55b-110">Description</span><span class="sxs-lookup"><span data-stu-id="ec55b-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ec55b-111">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="ec55b-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ec55b-112">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="ec55b-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ec55b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec55b-113">Requirements</span></span>



| <span data-ttu-id="ec55b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec55b-114">Requirement</span></span> | <span data-ttu-id="ec55b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec55b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec55b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec55b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec55b-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec55b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ec55b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec55b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec55b-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec55b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ec55b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec55b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec55b-121"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec55b-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec55b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec55b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec55b-123">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ec55b-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




