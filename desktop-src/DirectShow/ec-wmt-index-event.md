---
description: Envoyé lorsqu’une application utilise le filtre d’enregistreur ASF WM pour indexer Windows Media Video fichiers.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532859"
---
# <a name="ec_wmt_index_event-dshowh"></a><span data-ttu-id="3d59c-103">EC_WMT_INDEX_EVENT (DShow. h)</span><span class="sxs-lookup"><span data-stu-id="3d59c-103">EC_WMT_INDEX_EVENT (Dshow.h)</span></span>

<span data-ttu-id="3d59c-104">Envoyé lorsqu’une application utilise le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) pour indexer Windows Media Video fichiers.</span><span class="sxs-lookup"><span data-stu-id="3d59c-104">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) filter to index Windows Media Video files.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d59c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d59c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d59c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3d59c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3d59c-107">Il peut s’agir de l’un des messages d' **\_ État WMT** suivants.</span><span class="sxs-lookup"><span data-stu-id="3d59c-107">Can be one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="3d59c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d59c-108">Value</span></span>                | <span data-ttu-id="3d59c-109">Description</span><span class="sxs-lookup"><span data-stu-id="3d59c-109">Description</span></span>              |
|----------------------|--------------------------|
| <span data-ttu-id="3d59c-110">WMT \_ démarré</span><span class="sxs-lookup"><span data-stu-id="3d59c-110">WMT\_STARTED</span></span>         | <span data-ttu-id="3d59c-111">L’indexation a commencé.</span><span class="sxs-lookup"><span data-stu-id="3d59c-111">Indexing has begun.</span></span>      |
| <span data-ttu-id="3d59c-112">WMT \_ fermé</span><span class="sxs-lookup"><span data-stu-id="3d59c-112">WMT\_CLOSED</span></span>          | <span data-ttu-id="3d59c-113">L’indexation est terminée.</span><span class="sxs-lookup"><span data-stu-id="3d59c-113">Indexing has completed.</span></span>  |
| <span data-ttu-id="3d59c-114">progression de l' \_ index WMT \_</span><span class="sxs-lookup"><span data-stu-id="3d59c-114">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="3d59c-115">L’indexation est en cours.</span><span class="sxs-lookup"><span data-stu-id="3d59c-115">Indexing is in progress.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3d59c-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3d59c-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3d59c-117">Si *lParam1* a été \_ fermé par WMT ou si WMT \_ a démarré, *lParam2* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3d59c-117">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="3d59c-118">Si *lParam1* est en \_ \_ cours d’index WMT, *lParam2* est une **valeur DWORD** qui spécifie la progression actuelle sous la forme d’un pourcentage de la taille totale du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="3d59c-118">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that specifies the current progress as a percentage of the total download size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d59c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d59c-119">Requirements</span></span>



| <span data-ttu-id="3d59c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d59c-120">Requirement</span></span> | <span data-ttu-id="3d59c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d59c-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d59c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d59c-122">Header</span></span><br/> | <dl> <span data-ttu-id="3d59c-123"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d59c-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d59c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d59c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d59c-125">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="3d59c-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3d59c-126">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d59c-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




