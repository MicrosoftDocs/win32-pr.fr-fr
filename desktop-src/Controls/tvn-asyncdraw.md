---
title: TVN_ASYNCDRAW le code de notification (commctrl. h)
description: Envoyé par un contrôle Tree-View à son parent lorsque le dessin d’une icône ou d’une superposition a échoué. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- Contrôles Windows de code de notification TVN_ASYNCDRAW
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106542868"
---
# <a name="tvn_asyncdraw-notification-code"></a><span data-ttu-id="61df5-105">\_Code de notification TVN ASYNCDRAW</span><span class="sxs-lookup"><span data-stu-id="61df5-105">TVN\_ASYNCDRAW notification code</span></span>

<span data-ttu-id="61df5-106">Envoyé par un contrôle Tree-View à son parent lorsque le dessin d’une icône ou d’une superposition a échoué.</span><span class="sxs-lookup"><span data-stu-id="61df5-106">Sent by a tree-view control to its parent when the drawing of a icon or overlay has failed.</span></span> <span data-ttu-id="61df5-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="61df5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="61df5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61df5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61df5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61df5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61df5-110">Pointeur vers une structure [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) .</span><span class="sxs-lookup"><span data-stu-id="61df5-110">Pointer to an [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="61df5-111">La structure **NMTVASYNCDRAW** contient la raison de l’échec du dessin.</span><span class="sxs-lookup"><span data-stu-id="61df5-111">The **NMTVASYNCDRAW** structure contains the reason the draw failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61df5-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61df5-112">Return value</span></span>

<span data-ttu-id="61df5-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="61df5-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61df5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="61df5-114">Remarks</span></span>

<span data-ttu-id="61df5-115">Le contrôle Tree-View doit avoir le style étendu [**TV \_ ex \_ DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="61df5-115">The tree-view control must have the [**TVS\_EX\_DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="61df5-116">Notez que cela équivaut à l’indicateur LVN ASYNCDRAWN de l’affichage \_ des listes et à son style correspondant.</span><span class="sxs-lookup"><span data-stu-id="61df5-116">Note that this is equivalent to list-view's LVN\_ASYNCDRAWN flag and its corresponding style.</span></span>

<span data-ttu-id="61df5-117">Ce contrôle ne dessine pas de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="61df5-117">This control does not draw asynchronously.</span></span> <span data-ttu-id="61df5-118">Le mode asynchrone est utilisé dans le contexte selon lequel le contrôle Tree-View n’extrait pas de façon synchrone une image si elle n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="61df5-118">Asynchronous is used in the context that the tree-view control does not synchronously extract an image if it is not available.</span></span> <span data-ttu-id="61df5-119">(Par exemple, l’image peut ne pas être disponible si le contrôle d’arborescence utilise une liste d’images éparses, dans la mesure où l’image peut être déchargée.) Au lieu de cela, lorsqu’une image n’est pas disponible, le contrôle demande de manière synchrone à la parente l’action à entreprendre en lui envoyant une \_ notification ASYNCDRAW TVN avec une structure [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) .</span><span class="sxs-lookup"><span data-stu-id="61df5-119">(For instance, the image may not be available if the tree-view control uses a sparse image list, since the image may be unloaded.) Instead, when an image is not available, the control synchronously asks the parent what action to take by sending the parent an TVN\_ASYNCDRAW notification with a [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="61df5-120">Le membre **HR** de cette structure décrit la raison de l’échec du dessin du contrôle.</span><span class="sxs-lookup"><span data-stu-id="61df5-120">The **hr** member of this structure describes the reason the control's draw failed.</span></span> <span data-ttu-id="61df5-121">Un résultat **HR** de E \_ en attente signifie que l’image n’est pas présente (l’image doit être extraite).</span><span class="sxs-lookup"><span data-stu-id="61df5-121">An **hr** result of E\_PENDING means the image is not present at all (the image needs to be extracted).</span></span> <span data-ttu-id="61df5-122">Success indique que l’image est présente mais pas à la qualité d’image requise.</span><span class="sxs-lookup"><span data-stu-id="61df5-122">Success indicates that the image is present but not at the required image quality.</span></span>

<span data-ttu-id="61df5-123">Le parent définit le membre **dwRetFlags** de la structure pour informer le contrôle de la procédure à suivre.</span><span class="sxs-lookup"><span data-stu-id="61df5-123">The parent sets the **dwRetFlags** member of the structure to inform the control how to proceed.</span></span> <span data-ttu-id="61df5-124">Par exemple, le parent peut retourner une autre image, dans le membre **iRetImageIndex** , pour le contrôle à dessiner.</span><span class="sxs-lookup"><span data-stu-id="61df5-124">For instance, the parent may return another image, in the **iRetImageIndex** member, for the control to draw.</span></span> <span data-ttu-id="61df5-125">Dans ce cas, le parent définit le membre **dwRetFlags** sur adrf \_ DRAWIMAGE.</span><span class="sxs-lookup"><span data-stu-id="61df5-125">In this case, the parent sets the **dwRetFlags** member to ADRF\_DRAWIMAGE.</span></span> <span data-ttu-id="61df5-126">Si le contrôle trouve que l’image retournée n’a pas été extraite, une autre \_ notification TVN ASYNCDRAW peut être envoyée par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="61df5-126">If the control finds the returned image has not been extracted, yet another TVN\_ASYNCDRAW notification may be sent by the control.</span></span>

<span data-ttu-id="61df5-127">Si une image n’est pas disponible, l’idée derrière asynchrone consiste à autoriser le parent à effectuer l’extraction en arrière-plan afin que l’extraction ne bloque pas le thread d’interface utilisateur, autrement dit, le thread sur lequel se trouve le contrôle.</span><span class="sxs-lookup"><span data-stu-id="61df5-127">If an image is not available, the idea behind asynchronous is to allow the parent do the extraction in the background so that extraction does not block the UI thread, that is, the thread the control is on.</span></span> <span data-ttu-id="61df5-128">Le parent peut retourner ADRF \_ DRAWNOTHING au contrôle, puis lancer un thread d’arrière-plan pour extraire l’icône.</span><span class="sxs-lookup"><span data-stu-id="61df5-128">The parent may return ADRF\_DRAWNOTHING to the control, then launch a background thread to extract the icon.</span></span> <span data-ttu-id="61df5-129">Une fois extrait, le parent peut définir l’icône dans le contrôle TreeView avec la macro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span><span class="sxs-lookup"><span data-stu-id="61df5-129">Once extracted, the parent may set the icon in the treeview control with macro [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span></span> <span data-ttu-id="61df5-130">Cela amène l’arborescence à invalider l’élément et à le repeindre avec l’image extraite dans la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="61df5-130">This causes tree-view to invalidate the item and eventually repaint it with the extracted image in the image list.</span></span>

<span data-ttu-id="61df5-131">L’exemple de code suivant, à utiliser dans le cadre d’un programme plus volumineux, montre comment un parent peut traiter deux codes de retour possibles dans cette notification par un contrôle et déterminer l’action que le contrôle doit prendre.</span><span class="sxs-lookup"><span data-stu-id="61df5-131">The following code example, to be used as part of a larger program, shows how a parent may process two possible return codes in this notification by a control, and decide what action the control should take.</span></span> <span data-ttu-id="61df5-132">La définition de **dwRetFlags** n’est pas affichée.</span><span class="sxs-lookup"><span data-stu-id="61df5-132">Setting **dwRetFlags** is not shown.</span></span>


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a><span data-ttu-id="61df5-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61df5-133">Requirements</span></span>



| <span data-ttu-id="61df5-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61df5-134">Requirement</span></span> | <span data-ttu-id="61df5-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="61df5-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61df5-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61df5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="61df5-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61df5-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61df5-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61df5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="61df5-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61df5-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61df5-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="61df5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="61df5-141"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61df5-141"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





