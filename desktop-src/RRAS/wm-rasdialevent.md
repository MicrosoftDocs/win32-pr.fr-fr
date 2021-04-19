---
title: Message WM_RASDIALEVENT (RAS. h)
description: Le système d’exploitation envoie un \_ message WM RASDIALEVENT à une procédure de fenêtre lorsqu’un changement d’événement d’État se produit pendant un processus de connexion RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- WM_RASDIALEVENT message RAS
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510730"
---
# <a name="wm_rasdialevent-message"></a><span data-ttu-id="dd3a6-104">\_Message WM RASDIALEVENT</span><span class="sxs-lookup"><span data-stu-id="dd3a6-104">WM\_RASDIALEVENT message</span></span>

<span data-ttu-id="dd3a6-105">Le système d’exploitation envoie un message **WM \_ RASDIALEVENT** à une procédure de fenêtre lorsqu’un changement d’événement d’État se produit pendant un processus de connexion RAS.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-105">The operating system sends a **WM\_RASDIALEVENT** message to a window procedure when a change of state event occurs during a RAS connection process.</span></span> <span data-ttu-id="dd3a6-106">Cela se produit lorsqu’une fenêtre a été spécifiée pour gérer les notifications de tels événements à l’aide du paramètre de *notificateur* de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span><span class="sxs-lookup"><span data-stu-id="dd3a6-106">This happens when a window has been specified to handle notifications of such events by using the *notifier* parameter of [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span></span>

<span data-ttu-id="dd3a6-107">Les deux paramètres de message sont équivalents aux paramètres des mêmes noms utilisés avec les fonctions de rappel [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) et [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="dd3a6-107">The two message parameters are equivalent to the parameters of the same names that are used with [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span>


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a><span data-ttu-id="dd3a6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd3a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd3a6-109">*rasconnstate*</span><span class="sxs-lookup"><span data-stu-id="dd3a6-109">*rasconnstate*</span></span> 
</dt> <dd>

<span data-ttu-id="dd3a6-110">Valeur de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-110">Value of *wParam*.</span></span> <span data-ttu-id="dd3a6-111">Équivalent au paramètre *rasconnstate* des fonctions de rappel [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) et [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="dd3a6-111">Equivalent to the *rasconnstate* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="dd3a6-112">Spécifie une valeur d’énumérateur [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) qui indique l’état que le processus de connexion d’accès à distance rasdial va entrer.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-112">Specifies a [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumerator value that indicates the state the RasDial remote access connection process is about to enter.</span></span>

</dd> <dt>

<span data-ttu-id="dd3a6-113">*dwError*</span><span class="sxs-lookup"><span data-stu-id="dd3a6-113">*dwError*</span></span> 
</dt> <dd>

<span data-ttu-id="dd3a6-114">Valeur de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-114">Value of *lParam*.</span></span> <span data-ttu-id="dd3a6-115">Équivalent au paramètre *dwError* des fonctions de rappel [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) et [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="dd3a6-115">Equivalent to the *dwError* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="dd3a6-116">Une valeur différente de zéro indique l’erreur qui s’est produite, ou zéro si aucune erreur ne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-116">A nonzero value indicates the error that has occurred, or zero if no error has occurred.</span></span>

<span data-ttu-id="dd3a6-117">[**Rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) envoie ce message avec *dwError* défini à zéro lors de l’entrée à chaque État de connexion.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-117">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) sends this message with *dwError* set to zero upon entry to each connection state.</span></span> <span data-ttu-id="dd3a6-118">Si une erreur se produit dans un État, le message est renvoyé pour l’État, cette fois avec une valeur *dwError* différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-118">If an error occurs within a state, the message is sent again for the state, this time with a nonzero *dwError* value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd3a6-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd3a6-119">Return value</span></span>

<span data-ttu-id="dd3a6-120">Si une application traite ce message, elle doit retourner la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="dd3a6-120">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd3a6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd3a6-121">Requirements</span></span>



| <span data-ttu-id="dd3a6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd3a6-122">Requirement</span></span> | <span data-ttu-id="dd3a6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd3a6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dd3a6-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd3a6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dd3a6-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd3a6-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dd3a6-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd3a6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dd3a6-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd3a6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dd3a6-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd3a6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd3a6-129"><dt>RAS. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd3a6-129"><dt>Ras.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd3a6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd3a6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd3a6-131">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="dd3a6-131">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="dd3a6-132">Messages du service d’accès à distance</span><span class="sxs-lookup"><span data-stu-id="dd3a6-132">Remote Access Service Messages</span></span>](remote-access-service-messages.md)
</dt> <dt>

[<span data-ttu-id="dd3a6-133">**RasDial**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-133">**RasDial**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[<span data-ttu-id="dd3a6-134">**RasDialFunc**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-134">**RasDialFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[<span data-ttu-id="dd3a6-135">**RasDialFunc1**</span><span class="sxs-lookup"><span data-stu-id="dd3a6-135">**RasDialFunc1**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

<span data-ttu-id="dd3a6-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dd3a6-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span></span>
</dt> </dl>

 

