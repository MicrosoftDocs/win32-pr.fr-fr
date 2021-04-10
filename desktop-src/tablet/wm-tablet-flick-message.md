---
description: Envoyé lorsqu’un utilisateur exécute un raccourci stylet. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: Message WM_TABLET_FLICK (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c95598ac23f37918c67eec70c2ed205f8a4fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201390"
---
# <a name="wm_tablet_flick-message"></a><span data-ttu-id="826c9-104">Message du raccourci de \_ tablette WM \_</span><span class="sxs-lookup"><span data-stu-id="826c9-104">WM\_TABLET\_FLICK message</span></span>

<span data-ttu-id="826c9-105">Envoyé lorsqu’un utilisateur exécute un raccourci stylet.</span><span class="sxs-lookup"><span data-stu-id="826c9-105">Sent when a user performs a pen flick.</span></span> <span data-ttu-id="826c9-106">Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="826c9-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a><span data-ttu-id="826c9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="826c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="826c9-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="826c9-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="826c9-109">[**Structure de \_ données de raccourci**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) qui contient des informations sur le raccourci du stylet qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="826c9-109">A [**FLICK\_DATA Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) that contains information about the pen flick that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="826c9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="826c9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="826c9-111">[**Structure de \_ point de mouvement**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) qui spécifie où le raccourci du stylet s’est produit.</span><span class="sxs-lookup"><span data-stu-id="826c9-111">The [**FLICK\_POINT Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) that specifies where the pen flick occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="826c9-112">Notes</span><span class="sxs-lookup"><span data-stu-id="826c9-112">Remarks</span></span>

<span data-ttu-id="826c9-113">Un raccourci stylet est un mouvement de stylet unidirectionnel qui requiert que l’utilisateur contacte le digitaliseur dans un mouvement de raccourci rapide et direct.</span><span class="sxs-lookup"><span data-stu-id="826c9-113">A pen flick is a unidirectional pen gesture that requires the user to contact the digitizer in a quick, straight flicking motion.</span></span> <span data-ttu-id="826c9-114">Un raccourci est caractérisé par une vitesse élevée et un degré élevé d’angles.</span><span class="sxs-lookup"><span data-stu-id="826c9-114">A flick is characterized by high speed and a high degree of straightness.</span></span> <span data-ttu-id="826c9-115">Un raccourci est identifié par sa direction.</span><span class="sxs-lookup"><span data-stu-id="826c9-115">A flick is identified by its direction.</span></span> <span data-ttu-id="826c9-116">Les raccourcis peuvent être effectués dans huit directions correspondant aux directions cardinales et secondaires de la boussole.</span><span class="sxs-lookup"><span data-stu-id="826c9-116">Flicks can be made in eight directions corresponding to the cardinal and secondary compass directions.</span></span>

<span data-ttu-id="826c9-117">Lorsqu’un raccourci de stylet se produit, Windows envoie tout d’abord une application en envoyant un message de **\_ \_ scintillement de tablette WM** , qu’une fenêtre reçoit par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="826c9-117">When a pen flick occurs, Windows first notifies an application by sending a **WM\_TABLET\_FLICK** message, which a window receives through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="826c9-118">Retournez la constante du **\_ \_ \_ masque géré WM WM** , décrite dans [constantes de raccourcis](flicks-constants.md), pour indiquer que l’application a répondu au message de **\_ \_ scintille de la tablette WM** .</span><span class="sxs-lookup"><span data-stu-id="826c9-118">Return the **FLICK\_WM\_HANDLED\_MASK** constant, described in [Flicks Constants](flicks-constants.md), to indicate that the application responded to the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="826c9-119">Si l’application ne retourne pas le masque avec le **\_ WM WM \_ \_ géré**, Windows effectue l’action par défaut spécifiée dans le panneau de configuration raccourcis en envoyant une notification de suivi, telle que [**WM \_ APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM \_ VSCROLL**](../controls/wm-vscroll.md)ou [**WM \_ keyverse**](../inputdev/wm-keydown.md), selon l’action associée au raccourci Pen.</span><span class="sxs-lookup"><span data-stu-id="826c9-119">If the application does not return **FLICK\_WM\_HANDLED\_MASK**, Windows performs the default action specified in the flicks control panel by sending a follow-up notification, such as [**WM\_APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM\_VSCROLL**](../controls/wm-vscroll.md), or [**WM\_KEYDOWN**](../inputdev/wm-keydown.md), depending on which action is associated with the pen flick.</span></span>

<span data-ttu-id="826c9-120">Soyez prudent lors du traitement du message de **\_ \_ raccourci WM** de la tablette.</span><span class="sxs-lookup"><span data-stu-id="826c9-120">Use caution when handling the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="826c9-121">**WM \_ Le \_ raccourci de tablette** est passé via la fonction [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="826c9-121">**WM\_TABLET\_FLICK** is passed via the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="826c9-122">Si vous appelez des méthodes sur une interface COM, cet objet doit être dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="826c9-122">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="826c9-123">Si ce n’est pas le cas, COM lève une exception.</span><span class="sxs-lookup"><span data-stu-id="826c9-123">If not, COM throws an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="826c9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="826c9-124">Requirements</span></span>



| <span data-ttu-id="826c9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="826c9-125">Requirement</span></span> | <span data-ttu-id="826c9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="826c9-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="826c9-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="826c9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="826c9-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="826c9-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="826c9-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="826c9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="826c9-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="826c9-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="826c9-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="826c9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="826c9-132"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="826c9-132"><dt>Tpcshrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="826c9-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="826c9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826c9-134">**structure des données de raccourci \_**</span><span class="sxs-lookup"><span data-stu-id="826c9-134">**flick\_data structure**</span></span>](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[<span data-ttu-id="826c9-135">**message du raccourci de \_ tablette WM \_**</span><span class="sxs-lookup"><span data-stu-id="826c9-135">**wm\_tablet\_flick message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="826c9-136">mouvements de raccourcis</span><span class="sxs-lookup"><span data-stu-id="826c9-136">flicks gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="826c9-137">[réponse aux raccourcis stylet](/previous-versions/windows/desktop/ms703447(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="826c9-137">[responding to pen flicks](/previous-versions/windows/desktop/ms703447(v=vs.85))</span></span>
</dt> </dl>

 

 
