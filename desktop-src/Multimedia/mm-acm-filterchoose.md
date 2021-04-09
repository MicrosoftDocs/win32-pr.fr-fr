---
title: Message d’MM_ACM_FILTERCHOOSE (Msacm. h)
description: Le \_ \_ message FILTERCHOOSE ACM mm avertit une fonction de raccordement de boîte de dialogue acmFilterChoose avant d’ajouter un élément à l’une des trois zones de liste déroulante.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- Message MM_ACM_FILTERCHOOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103037"
---
# <a name="mm_acm_filterchoose-message"></a><span data-ttu-id="4f699-104">MM \_ \_ message FILTERCHOOSE ACM</span><span class="sxs-lookup"><span data-stu-id="4f699-104">MM\_ACM\_FILTERCHOOSE message</span></span>

<span data-ttu-id="4f699-105">Le **message \_ \_ FILTERCHOOSE ACM mm** avertit une fonction de raccordement de boîte de dialogue [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) avant d’ajouter un élément à l’une des trois zones de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="4f699-105">The **MM\_ACM\_FILTERCHOOSE** message notifies an [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) dialog box hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="4f699-106">Ce message permet à une application de personnaliser davantage les sélections disponibles via l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4f699-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a><span data-ttu-id="4f699-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f699-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f699-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span><span class="sxs-lookup"><span data-stu-id="4f699-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="4f699-109">Zone de liste déroulante initialisée et opération de vérification ou d’ajout.</span><span class="sxs-lookup"><span data-stu-id="4f699-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="4f699-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f699-110">Requirement</span></span> | <span data-ttu-id="4f699-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f699-111">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f699-112">\_vérification personnalisée \_ FILTERCHOOSE</span><span class="sxs-lookup"><span data-stu-id="4f699-112">FILTERCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="4f699-113">Le paramètre *lParam* est un pointeur vers une structure [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) à ajouter à la zone de liste déroulante nom personnalisé.</span><span class="sxs-lookup"><span data-stu-id="4f699-113">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="4f699-114">\_Ajouter un filtre FILTERCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="4f699-114">FILTERCHOOSE\_FILTER\_ADD</span></span>       | <span data-ttu-id="4f699-115">Le paramètre *lParam* est un pointeur vers une mémoire tampon qui accepte une structure [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) à ajouter à la zone de liste déroulante de filtre.</span><span class="sxs-lookup"><span data-stu-id="4f699-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span> <span data-ttu-id="4f699-116">L’application doit copier la structure de filtre à ajouter à cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="4f699-116">The application must copy the filter structure to be added into this buffer.</span></span> |
| <span data-ttu-id="4f699-117">\_vérification du filtre FILTERCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="4f699-117">FILTERCHOOSE\_FILTER\_VERIFY</span></span>    | <span data-ttu-id="4f699-118">Le paramètre *lParam* est un pointeur vers une structure [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) à ajouter à la zone de liste déroulante de filtre.</span><span class="sxs-lookup"><span data-stu-id="4f699-118">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="4f699-119">FILTERCHOOSE \_ FILTERTAG \_ Add</span><span class="sxs-lookup"><span data-stu-id="4f699-119">FILTERCHOOSE\_FILTERTAG\_ADD</span></span>    | <span data-ttu-id="4f699-120">Le paramètre *lParam* est un pointeur vers une **valeur DWORD** qui accepte une balise de filtre audio Waveform à ajouter à la zone de liste déroulante balise de filtre.</span><span class="sxs-lookup"><span data-stu-id="4f699-120">The *lParam* parameter is a pointer to a **DWORD** that will accept a waveform-audio filter tag to be added to the Filter Tag drop-down list box.</span></span>                                                                                        |
| <span data-ttu-id="4f699-121">FILTERCHOOSE \_ FILTERTAG \_ verify</span><span class="sxs-lookup"><span data-stu-id="4f699-121">FILTERCHOOSE\_FILTERTAG\_VERIFY</span></span> | <span data-ttu-id="4f699-122">Le paramètre *lParam* est une balise de filtre de forme d’onde audio à répertorier dans la zone de liste déroulante balise de filtre.</span><span class="sxs-lookup"><span data-stu-id="4f699-122">The *lParam* parameter is a waveform-audio filter tag to be listed in the Filter Tag drop-down list box.</span></span>                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="4f699-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span><span class="sxs-lookup"><span data-stu-id="4f699-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="4f699-124">Valeur définie par la zone de liste spécifiée dans le paramètre **wParam** .</span><span class="sxs-lookup"><span data-stu-id="4f699-124">Value defined by the list box specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f699-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4f699-125">Return Value</span></span>

<span data-ttu-id="4f699-126">Retourne la **valeur true** si une application gère ce message ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4f699-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f699-127">Notes</span><span class="sxs-lookup"><span data-stu-id="4f699-127">Remarks</span></span>

<span data-ttu-id="4f699-128">Si l’application traite l' \_ \_ opération d’ajout de filtre FILTERCHOOSE, la taille de la mémoire tampon fournie dans *lParam* est déterminée à partir de la fonction [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .</span><span class="sxs-lookup"><span data-stu-id="4f699-128">If the application processes the FILTERCHOOSE\_FILTER\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="4f699-129">Si l’application traite une opération de vérification, l’application doit précéder la valeur de retour avec **SetWindowLong** (HWND, DWL \_ MSGRESULT, (long) **false**) pour empêcher la boîte de dialogue de répertorier cette sélection ou avec **SetWindowLong** (HWND, DWL \_ MSGRESULT, (long)**true**) pour permettre à la boîte de dialogue de répertorier cette sélection.</span><span class="sxs-lookup"><span data-stu-id="4f699-129">If the application processes a verify operation, the application must precede the return value with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG) **FALSE**) to prevent the dialog box from listing this selection or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) to allow the dialog box to list this selection.</span></span> <span data-ttu-id="4f699-130">En cas de traitement d’une opération d’ajout, l’application doit précéder le retour avec **SetWindowLong** (HWND, DWL \_ MSGRESULT, (long)**false**) pour indiquer qu’aucun ajout supplémentaire n’est nécessaire ou avec **SetWindowLong** (HWND, DWL \_ MSGRESULT, (long)**true**) si d’autres ajouts sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="4f699-130">If processing an add operation, the application must precede the return with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**FALSE**) to indicate that no more additions are required or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) if more additions are required.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f699-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f699-131">Requirements</span></span>



| <span data-ttu-id="4f699-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f699-132">Requirement</span></span> | <span data-ttu-id="4f699-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f699-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f699-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f699-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4f699-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f699-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4f699-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f699-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4f699-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f699-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4f699-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f699-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f699-139"><dt>Msacm. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f699-139"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f699-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f699-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f699-141">Gestionnaire de compression audio</span><span class="sxs-lookup"><span data-stu-id="4f699-141">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="4f699-142">Messages de compression audio</span><span class="sxs-lookup"><span data-stu-id="4f699-142">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

 





