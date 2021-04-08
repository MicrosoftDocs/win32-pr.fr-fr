---
title: LVN_GETDISPINFO le code de notification (commctrl. h)
description: Envoyé par un contrôle List-View à sa fenêtre parente. Il s’agit d’une demande de la fenêtre parente pour fournir les informations nécessaires à l’affichage ou au tri d’un élément de liste. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- Contrôles Windows de code de notification LVN_GETDISPINFO
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744004"
---
# <a name="lvn_getdispinfo-notification-code"></a><span data-ttu-id="35ef3-106">\_Code de notification LVN GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="35ef3-106">LVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="35ef3-107">Envoyé par un contrôle List-View à sa fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="35ef3-107">Sent by a list-view control to its parent window.</span></span> <span data-ttu-id="35ef3-108">Il s’agit d’une demande de la fenêtre parente pour fournir les informations nécessaires à l’affichage ou au tri d’un élément de liste.</span><span class="sxs-lookup"><span data-stu-id="35ef3-108">It is a request for the parent window to provide information needed to display or sort a list-view item.</span></span> <span data-ttu-id="35ef3-109">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="35ef3-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="35ef3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35ef3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ef3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35ef3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35ef3-112">Pointeur vers une structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="35ef3-112">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="35ef3-113">En entrée, la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) contenue dans cette structure spécifie le type d’informations requis et identifie l’élément ou le sous-élément d’intérêt.</span><span class="sxs-lookup"><span data-stu-id="35ef3-113">On input, the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure contained in this structure specifies the type of information required and identifies the item or subitem of interest.</span></span> <span data-ttu-id="35ef3-114">Utilisez la structure **LVITEM** pour retourner les informations demandées au contrôle.</span><span class="sxs-lookup"><span data-stu-id="35ef3-114">Use the **LVITEM** structure to return the requested information to the control.</span></span> <span data-ttu-id="35ef3-115">Si votre gestionnaire de messages définit l' \_ indicateur LVIF di \_ SETITEM dans le membre **Mask** de la structure **LVITEM** , le contrôle List-View stocke les informations demandées et ne le redemande pas.</span><span class="sxs-lookup"><span data-stu-id="35ef3-115">If your message handler sets the LVIF\_DI\_SETITEM flag in the **mask** member of the **LVITEM** structure, the list-view control stores the requested information and will not ask for it again.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ef3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35ef3-116">Return value</span></span>

<span data-ttu-id="35ef3-117">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="35ef3-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ef3-118">Notes</span><span class="sxs-lookup"><span data-stu-id="35ef3-118">Remarks</span></span>

<span data-ttu-id="35ef3-119">Le récepteur de notification convertit *lParam* pour récupérer la structure [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="35ef3-119">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="35ef3-120">Le paramètre *wParam* contient le code de notification.</span><span class="sxs-lookup"><span data-stu-id="35ef3-120">The *wParam* parameter contains the notification code.</span></span>

<span data-ttu-id="35ef3-121">Un contrôle List-View envoie le code de notification **LVN \_ GETDISPINFO** pour récupérer des informations d’élément stockées par l’application plutôt que par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="35ef3-121">A list-view control sends the **LVN\_GETDISPINFO** notification code to retrieve item information that is stored by the application rather than the control.</span></span> <span data-ttu-id="35ef3-122">Les informations peuvent être du texte ou des icônes pour un élément.</span><span class="sxs-lookup"><span data-stu-id="35ef3-122">The information can be text or icon information for an item.</span></span> <span data-ttu-id="35ef3-123">Il peut également s’agir d’informations sur l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="35ef3-123">It can also be item state information.</span></span> <span data-ttu-id="35ef3-124">Consultez le [**message \_ SETCALLBACKMASK LVM**](lvm-setcallbackmask.md) pour plus d’informations sur l’implémentation de l’état des éléments sur la base d’un rappel.</span><span class="sxs-lookup"><span data-stu-id="35ef3-124">See the [**LVM\_SETCALLBACKMASK**](lvm-setcallbackmask.md) message for more information on implementing item state on a callback basis.</span></span>

<span data-ttu-id="35ef3-125">Pour plus d’informations sur les rappels de vue de liste, consultez [éléments de rappel et masque de rappel](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="35ef3-125">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="35ef3-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="35ef3-126">Examples</span></span>

<span data-ttu-id="35ef3-127">L’exemple suivant montre comment ce code de notification peut être géré pour définir le texte dans les colonnes d’un affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="35ef3-127">The following example shows how this notification code might be handled to set the text in the columns of a list view.</span></span> <span data-ttu-id="35ef3-128">Les données de chaque élément sont stockées dans la structure suivante.</span><span class="sxs-lookup"><span data-stu-id="35ef3-128">The data for each item is held in the following structure.</span></span>


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



<span data-ttu-id="35ef3-129">Les éléments suivants proviennent du \_ Gestionnaire de notification WM dans la procédure de dialogue.</span><span class="sxs-lookup"><span data-stu-id="35ef3-129">The following is from the WM\_NOTIFY handler in the dialog procedure.</span></span>


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a><span data-ttu-id="35ef3-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35ef3-130">Requirements</span></span>



| <span data-ttu-id="35ef3-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35ef3-131">Requirement</span></span> | <span data-ttu-id="35ef3-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ef3-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35ef3-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35ef3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="35ef3-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35ef3-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35ef3-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35ef3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="35ef3-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35ef3-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35ef3-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="35ef3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="35ef3-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="35ef3-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="35ef3-139">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="35ef3-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="35ef3-140">**LVN \_ GETDISPINFOW** (Unicode) et **LVN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="35ef3-140">**LVN\_GETDISPINFOW** (Unicode) and **LVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="35ef3-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35ef3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ef3-142">**LVN \_ SETDISPINFO**</span><span class="sxs-lookup"><span data-stu-id="35ef3-142">**LVN\_SETDISPINFO**</span></span>](lvn-setdispinfo.md)
</dt> </dl>

 

 





