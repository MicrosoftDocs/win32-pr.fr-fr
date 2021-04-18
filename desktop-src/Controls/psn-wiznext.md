---
title: PSN_WIZNEXT le code de notification (Prsht. h)
description: Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton suivant dans un Assistant. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- Contrôles Windows de code de notification PSN_WIZNEXT
topic_type:
- apiref
api_name:
- PSN_WIZNEXT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 145591b725548ffc4175541fd37db8f285533590
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511786"
---
# <a name="psn_wiznext-notification-code"></a><span data-ttu-id="050f8-105">\_Code de notification PSN WIZNEXT</span><span class="sxs-lookup"><span data-stu-id="050f8-105">PSN\_WIZNEXT notification code</span></span>

<span data-ttu-id="050f8-106">Notifie une page sur laquelle l’utilisateur a cliqué sur le bouton **suivant** dans un Assistant.</span><span class="sxs-lookup"><span data-stu-id="050f8-106">Notifies a page that the user has clicked the **Next** button in a wizard.</span></span> <span data-ttu-id="050f8-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="050f8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="050f8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="050f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="050f8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="050f8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="050f8-110">Pointeur vers une structure [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="050f8-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="050f8-111">Cette structure contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) en tant que premier membre, **HDR**. Le membre **hwndFrom** de cette structure **NMHDR** contient le handle de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="050f8-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="050f8-112">Le membre **lParam** de la structure **PSHNOTIFY** ne contient aucune information.</span><span class="sxs-lookup"><span data-stu-id="050f8-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="050f8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="050f8-113">Return value</span></span>

<span data-ttu-id="050f8-114">Retourne 0 pour permettre à l’Assistant de passer à la page suivante.</span><span class="sxs-lookup"><span data-stu-id="050f8-114">Return 0 to allow the wizard to go to the next page.</span></span> <span data-ttu-id="050f8-115">Retourne-1 pour empêcher l’Assistant de modifier les pages.</span><span class="sxs-lookup"><span data-stu-id="050f8-115">Return -1 to prevent the wizard from changing pages.</span></span> <span data-ttu-id="050f8-116">Pour afficher une page particulière, retournez son identificateur de ressource de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="050f8-116">To display a particular page, return its dialog resource identifier.</span></span> <span data-ttu-id="050f8-117">Si la boîte de dialogue a été spécifiée avec l’indicateur [**PSP \_ DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) , cette notification retourne le pointeur vers le modèle de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="050f8-117">If the dialog was specified with the [**PSP\_DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) flag, this notification returns the pointer to the dialog template.</span></span>

## <a name="remarks"></a><span data-ttu-id="050f8-118">Notes</span><span class="sxs-lookup"><span data-stu-id="050f8-118">Remarks</span></span>

<span data-ttu-id="050f8-119">Pour définir la valeur de retour, la procédure de la boîte de dialogue de la page doit appeler la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) avec la valeur de **\_ MSGRESULT DWL** et retourner **true**.</span><span class="sxs-lookup"><span data-stu-id="050f8-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the **DWL\_MSGRESULT** value and return **TRUE**.</span></span> <span data-ttu-id="050f8-120">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="050f8-120">For example:</span></span>

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> <span data-ttu-id="050f8-121">La feuille de propriétés est en cours de manipulation de la liste de pages lorsque le \_ Code de notification PSN WIZNEXT est envoyé.</span><span class="sxs-lookup"><span data-stu-id="050f8-121">The property sheet is in the process of manipulating the list of pages when the PSN\_WIZNEXT notification code is sent.</span></span> <span data-ttu-id="050f8-122">Vous pouvez ajouter, insérer ou supprimer des pages en réponse à ces codes de notification, mais une attention particulière doit être prise si vous insérez ou supprimez des pages avant la page actuelle.</span><span class="sxs-lookup"><span data-stu-id="050f8-122">You can add, insert, or remove pages in response to these notification codes, but special care must be taken if you insert or remove pages before the current page.</span></span>

 

<span data-ttu-id="050f8-123">Si vous insérez ou supprimez des pages avant la page actuelle, vous devez retourner (via la **\_ MSGRESULT** de l’DWL) une valeur différente de zéro pour spécifier la nouvelle page souhaitée.</span><span class="sxs-lookup"><span data-stu-id="050f8-123">If you insert or remove pages before the current page, you must return (through **DWL\_MSGRESULT**) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="050f8-124">Notez, toutefois, que si vous insérez ou supprimez une page qui se trouve avant la page actuelle (avec un index plus petit que la page active), [PSN \_ KILLACTIVE](psn-killactive.md) peut être envoyé à la mauvaise page.</span><span class="sxs-lookup"><span data-stu-id="050f8-124">Note, however, that if you insert or remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

<span data-ttu-id="050f8-125">Pour cette raison, il est recommandé que les assistants qui ajoutent et suppriment des pages dynamiquement en réponse à PSN \_ WIZNEXT et [PSN \_ WIZBACK](psn-wizback.md) le fassent uniquement aux pages situées à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="050f8-125">For this reason, it is recommended that wizards that add and remove pages dynamically in response to PSN\_WIZNEXT and [PSN\_WIZBACK](psn-wizback.md) do so only to pages at the end of the list.</span></span> <span data-ttu-id="050f8-126">Si vous souhaitez que votre Assistant supprime les pages avec précision, conservez les pages dynamiques à la fin de la liste et retournez aux pages permanentes avant de les supprimer.</span><span class="sxs-lookup"><span data-stu-id="050f8-126">If you want your wizard to remove pages accurately, keep the dynamic pages at the end of the list and jump back to permanent pages before deleting them.</span></span>

<span data-ttu-id="050f8-127">Supposons, par exemple, qu’un Assistant se compose d’une page d’introduction, d’une série de pages dynamiques et d’une page de fin, et que vous souhaitez supprimer les pages dynamiques lorsque l’utilisateur atteint la page de fin.</span><span class="sxs-lookup"><span data-stu-id="050f8-127">For example, suppose a wizard consists of an introductory page, a series of dynamic pages, and a completion page, and you want to delete the dynamic pages when the user reaches the completion page.</span></span>

1.  <span data-ttu-id="050f8-128">L’Assistant commence par deux pages : « introduction » et « fin ».</span><span class="sxs-lookup"><span data-stu-id="050f8-128">The wizard would begin with two pages, "Introduction" and "Completion."</span></span> <span data-ttu-id="050f8-129">L’utilisateur commence sur la page « Introduction ».</span><span class="sxs-lookup"><span data-stu-id="050f8-129">The user begins on the "Introduction" page.</span></span>
    1.  <span data-ttu-id="050f8-130">Introduction (l’utilisateur est ici)</span><span class="sxs-lookup"><span data-stu-id="050f8-130">Introduction (User is here)</span></span>
    2.  <span data-ttu-id="050f8-131">Completion</span><span class="sxs-lookup"><span data-stu-id="050f8-131">Completion</span></span>
2.  <span data-ttu-id="050f8-132">Lorsque l’utilisateur quitte l’introduction, l’Assistant ajoute les pages dynamiques et place l’utilisateur sur la première page dynamique en retournant (via l' **\_ MSGRESULT**) l’identificateur de boîte de dialogue de la page « dynamique 1 ».</span><span class="sxs-lookup"><span data-stu-id="050f8-132">When the user navigates away from "Introduction," the wizard adds the dynamic pages and places the user at the first dynamic page by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Dynamic 1."</span></span> <span data-ttu-id="050f8-133">Dans cet exemple, il existe trois pages dynamiques.</span><span class="sxs-lookup"><span data-stu-id="050f8-133">In this example, there are three dynamic pages.</span></span>
    1.  <span data-ttu-id="050f8-134">Introduction</span><span class="sxs-lookup"><span data-stu-id="050f8-134">Introduction</span></span>
    2.  <span data-ttu-id="050f8-135">Completion</span><span class="sxs-lookup"><span data-stu-id="050f8-135">Completion</span></span>
    3.  <span data-ttu-id="050f8-136">Dynamique 1 (l’utilisateur est ici)</span><span class="sxs-lookup"><span data-stu-id="050f8-136">Dynamic 1 (User is here)</span></span>
    4.  <span data-ttu-id="050f8-137">Dynamique 2</span><span class="sxs-lookup"><span data-stu-id="050f8-137">Dynamic 2</span></span>
    5.  <span data-ttu-id="050f8-138">Dynamique 3</span><span class="sxs-lookup"><span data-stu-id="050f8-138">Dynamic 3</span></span>
3.  <span data-ttu-id="050f8-139">Une fois que l’utilisateur a navigué dans les pages dynamiques vers « Dynamic 3 », puis accède à la page suivante, l’application doit placer l’utilisateur sur la page « achèvement ».</span><span class="sxs-lookup"><span data-stu-id="050f8-139">After the user navigates through the dynamic pages to "Dynamic 3" and then navigates to the next page, the application should place the user at the page "Completion."</span></span> <span data-ttu-id="050f8-140">Là encore, cela se fait en retournant (via **DWL \_ MSGRESULT**) l’identificateur de boîte de dialogue de la page « achèvement ».</span><span class="sxs-lookup"><span data-stu-id="050f8-140">Again, this is done by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Completion."</span></span>
    1.  <span data-ttu-id="050f8-141">Introduction</span><span class="sxs-lookup"><span data-stu-id="050f8-141">Introduction</span></span>
    2.  <span data-ttu-id="050f8-142">Achèvement (l’utilisateur est ici)</span><span class="sxs-lookup"><span data-stu-id="050f8-142">Completion (User is here)</span></span>
    3.  <span data-ttu-id="050f8-143">Dynamique 1</span><span class="sxs-lookup"><span data-stu-id="050f8-143">Dynamic 1</span></span>
    4.  <span data-ttu-id="050f8-144">Dynamique 2</span><span class="sxs-lookup"><span data-stu-id="050f8-144">Dynamic 2</span></span>
    5.  <span data-ttu-id="050f8-145">Dynamique 3</span><span class="sxs-lookup"><span data-stu-id="050f8-145">Dynamic 3</span></span>
4.  <span data-ttu-id="050f8-146">L’application peut ensuite supprimer les trois pages dynamiques (numérotées de trois à cinq) en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="050f8-146">The application can then remove the three dynamic pages (numbered three through five) safely.</span></span>
    1.  <span data-ttu-id="050f8-147">Introduction</span><span class="sxs-lookup"><span data-stu-id="050f8-147">Introduction</span></span>
    2.  <span data-ttu-id="050f8-148">Achèvement (l’utilisateur est ici)</span><span class="sxs-lookup"><span data-stu-id="050f8-148">Completion (User is here)</span></span>

<span data-ttu-id="050f8-149">Notez que cette technique est nécessaire uniquement si votre Assistant supprime les pages dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="050f8-149">Note that this technique is necessary only if your wizard removes pages dynamically.</span></span> <span data-ttu-id="050f8-150">Si votre Assistant ajoute uniquement des pages dynamiquement, ce processus n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="050f8-150">If your wizard only adds pages dynamically, this process is not necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="050f8-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="050f8-151">Requirements</span></span>



| <span data-ttu-id="050f8-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="050f8-152">Requirement</span></span> | <span data-ttu-id="050f8-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="050f8-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="050f8-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="050f8-154">Minimum supported client</span></span><br/> | <span data-ttu-id="050f8-155">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="050f8-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="050f8-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="050f8-156">Minimum supported server</span></span><br/> | <span data-ttu-id="050f8-157">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="050f8-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="050f8-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="050f8-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="050f8-159"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="050f8-159"><dt>Prsht.h</dt></span></span> </dl> |



 

