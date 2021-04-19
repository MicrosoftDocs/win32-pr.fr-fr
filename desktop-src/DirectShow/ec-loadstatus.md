---
description: Avertit l’application de la progression lors de l’ouverture d’un fichier réseau.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521715"
---
# <a name="ec_loadstatus"></a><span data-ttu-id="36c09-103">\_LOADSTATUS EC</span><span class="sxs-lookup"><span data-stu-id="36c09-103">EC\_LOADSTATUS</span></span>

<span data-ttu-id="36c09-104">Avertit l’application de la progression lors de l’ouverture d’un fichier réseau.</span><span class="sxs-lookup"><span data-stu-id="36c09-104">Notifies the application of progress when opening a network file.</span></span>

## <a name="parameters"></a><span data-ttu-id="36c09-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36c09-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36c09-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="36c09-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="36c09-107">Code d’état.</span><span class="sxs-lookup"><span data-stu-id="36c09-107">Status code.</span></span> <span data-ttu-id="36c09-108">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="36c09-108">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="36c09-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="36c09-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="36c09-110">Zéro.</span><span class="sxs-lookup"><span data-stu-id="36c09-110">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="36c09-111">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="36c09-111">Default Action</span></span>

<span data-ttu-id="36c09-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="36c09-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="36c09-113">Notes</span><span class="sxs-lookup"><span data-stu-id="36c09-113">Remarks</span></span>

<span data-ttu-id="36c09-114">Le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) et le filtre de [source Windows Media](windows-media-source-filter.md) hérité envoient cet événement.</span><span class="sxs-lookup"><span data-stu-id="36c09-114">The [WM ASF Reader](wm-asf-reader-filter.md) filter and the legacy [Windows Media Source](windows-media-source-filter.md) filter send this event.</span></span> <span data-ttu-id="36c09-115">Le premier paramètre d’événement a l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="36c09-115">The first event parameter has one of the following values.</span></span>



| <span data-ttu-id="36c09-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="36c09-116">Value</span></span>                        | <span data-ttu-id="36c09-117">Description</span><span class="sxs-lookup"><span data-stu-id="36c09-117">Description</span></span>                                    |
|------------------------------|------------------------------------------------|
| <span data-ttu-id="36c09-118">AM \_ LOADSTATUS \_ fermé</span><span class="sxs-lookup"><span data-stu-id="36c09-118">AM\_LOADSTATUS\_CLOSED</span></span>       | <span data-ttu-id="36c09-119">Le filtre source a fermé le fichier.</span><span class="sxs-lookup"><span data-stu-id="36c09-119">The source filter has closed the file.</span></span>         |
| <span data-ttu-id="36c09-120">\_connexion am LOADSTATUS \_</span><span class="sxs-lookup"><span data-stu-id="36c09-120">AM\_LOADSTATUS\_CONNECTING</span></span>   | <span data-ttu-id="36c09-121">Le filtre source se connecte au serveur.</span><span class="sxs-lookup"><span data-stu-id="36c09-121">The source filter is connecting to the server.</span></span> |
| <span data-ttu-id="36c09-122">AM \_ LOADSTATUS \_ LOADINGDESCR</span><span class="sxs-lookup"><span data-stu-id="36c09-122">AM\_LOADSTATUS\_LOADINGDESCR</span></span> | <span data-ttu-id="36c09-123">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="36c09-123">Not used.</span></span>                                      |
| <span data-ttu-id="36c09-124">AM \_ LOADSTATUS \_ LOADINGMCAST</span><span class="sxs-lookup"><span data-stu-id="36c09-124">AM\_LOADSTATUS\_LOADINGMCAST</span></span> | <span data-ttu-id="36c09-125">Non utilisé</span><span class="sxs-lookup"><span data-stu-id="36c09-125">Not used</span></span>                                       |
| <span data-ttu-id="36c09-126">\_recherche LOADSTATUS \_</span><span class="sxs-lookup"><span data-stu-id="36c09-126">AM\_LOADSTATUS\_LOCATING</span></span>     | <span data-ttu-id="36c09-127">Le filtre source recherche les données demandées.</span><span class="sxs-lookup"><span data-stu-id="36c09-127">The source filter is locating requested data.</span></span>  |
| <span data-ttu-id="36c09-128">AM \_ LOADSTATUS \_ ouvert</span><span class="sxs-lookup"><span data-stu-id="36c09-128">AM\_LOADSTATUS\_OPEN</span></span>         | <span data-ttu-id="36c09-129">Le filtre source a ouvert le fichier.</span><span class="sxs-lookup"><span data-stu-id="36c09-129">The source filter has opened the file.</span></span>         |
| <span data-ttu-id="36c09-130">\_ouverture de LOADSTATUS \_</span><span class="sxs-lookup"><span data-stu-id="36c09-130">AM\_LOADSTATUS\_OPENING</span></span>      | <span data-ttu-id="36c09-131">Le filtre source ouvre le fichier.</span><span class="sxs-lookup"><span data-stu-id="36c09-131">The source filter is opening the file.</span></span>         |



 

## <a name="requirements"></a><span data-ttu-id="36c09-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36c09-132">Requirements</span></span>



| <span data-ttu-id="36c09-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36c09-133">Requirement</span></span> | <span data-ttu-id="36c09-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="36c09-134">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36c09-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="36c09-135">Header</span></span><br/> | <dl> <span data-ttu-id="36c09-136"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="36c09-136"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36c09-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36c09-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36c09-138">Codes de notification d’événement</span><span class="sxs-lookup"><span data-stu-id="36c09-138">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="36c09-139">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="36c09-139">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




