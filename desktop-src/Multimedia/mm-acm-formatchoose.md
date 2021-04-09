---
title: Message d’MM_ACM_FORMATCHOOSE (Msacm. h)
description: Le \_ message mm ACM \_ FORMATCHOOSE avertit une fonction de raccordement de boîte de dialogue acmFormatChoose avant d’ajouter un élément à l’une des trois zones de liste déroulante.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- Message MM_ACM_FORMATCHOOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743924"
---
# <a name="mm_acm_formatchoose-message"></a><span data-ttu-id="b5ce3-104">MM \_ \_ message FORMATCHOOSE ACM</span><span class="sxs-lookup"><span data-stu-id="b5ce3-104">MM\_ACM\_FORMATCHOOSE message</span></span>

<span data-ttu-id="b5ce3-105">Le message **mm \_ ACM \_ FORMATCHOOSE** avertit une fonction de raccordement de boîte de dialogue [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) avant d’ajouter un élément à l’une des trois zones de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-105">The **MM\_ACM\_FORMATCHOOSE** message notifies an [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) dialog hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="b5ce3-106">Ce message permet à une application de personnaliser davantage les sélections disponibles via l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a><span data-ttu-id="b5ce3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5ce3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ce3-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span><span class="sxs-lookup"><span data-stu-id="b5ce3-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="b5ce3-109">Zone de liste déroulante initialisée et opération de vérification ou d’ajout.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="b5ce3-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5ce3-110">Requirement</span></span> | <span data-ttu-id="b5ce3-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5ce3-111">Value</span></span> |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ce3-112">\_vérification personnalisée \_ FORMATCHOOSE</span><span class="sxs-lookup"><span data-stu-id="b5ce3-112">FORMATCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="b5ce3-113">Le paramètre *lParam* est un pointeur vers une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) à ajouter à la zone de liste déroulante nom personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-113">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="b5ce3-114">FORMATCHOOSE \_ Ajouter au format \_</span><span class="sxs-lookup"><span data-stu-id="b5ce3-114">FORMATCHOOSE\_FORMAT\_ADD</span></span>       | <span data-ttu-id="b5ce3-115">Le paramètre *lParam* est un pointeur vers une mémoire tampon qui accepte une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) à ajouter à la zone de liste déroulante format.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span> <span data-ttu-id="b5ce3-116">L’application doit copier la structure de format à ajouter à cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-116">The application must copy the format structure to be added into this buffer.</span></span> |
| <span data-ttu-id="b5ce3-117">\_vérification du format de FORMATCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="b5ce3-117">FORMATCHOOSE\_FORMAT\_VERIFY</span></span>    | <span data-ttu-id="b5ce3-118">Le paramètre *lParam* est un pointeur vers une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) à ajouter à la zone de liste déroulante format.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-118">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="b5ce3-119">FORMATCHOOSE \_ FORMATTAG \_ Add</span><span class="sxs-lookup"><span data-stu-id="b5ce3-119">FORMATCHOOSE\_FORMATTAG\_ADD</span></span>    | <span data-ttu-id="b5ce3-120">Le paramètre *lParam* est un pointeur vers une variable qui accepte une balise de format audio Waveform à ajouter à la zone de liste déroulante balise de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-120">The *lParam* parameter is a pointer to a variable that will accept a waveform-audio format tag to be added to the Format Tag drop-down list box.</span></span>                                                                                             |
| <span data-ttu-id="b5ce3-121">FORMATCHOOSE \_ FORMATTAG \_ verify</span><span class="sxs-lookup"><span data-stu-id="b5ce3-121">FORMATCHOOSE\_FORMATTAG\_VERIFY</span></span> | <span data-ttu-id="b5ce3-122">Le paramètre *lParam* est une balise de format Waveform Audio à répertorier dans la zone de liste déroulante format de balise.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-122">The *lParam* parameter is a waveform-audio format tag to be listed in the Format Tag drop-down list box.</span></span>                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="b5ce3-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span><span class="sxs-lookup"><span data-stu-id="b5ce3-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="b5ce3-124">Valeur définie par la zone de liste spécifiée dans le paramètre **wParam** .</span><span class="sxs-lookup"><span data-stu-id="b5ce3-124">Value defined by the listbox specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ce3-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b5ce3-125">Return Value</span></span>

<span data-ttu-id="b5ce3-126">Retourne la **valeur true** si une application gère ce message ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5ce3-127">Notes</span><span class="sxs-lookup"><span data-stu-id="b5ce3-127">Remarks</span></span>

<span data-ttu-id="b5ce3-128">Si l’application traite l' \_ opération Add au format FILTERCHOOSE \_ , la taille de la mémoire tampon fournie dans *lParam* est déterminée à partir de la fonction [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .</span><span class="sxs-lookup"><span data-stu-id="b5ce3-128">If the application processes the FILTERCHOOSE\_FORMAT\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="b5ce3-129">Si votre application traite une opération de vérification, elle peut empêcher la boîte de dialogue de répertorier cette sélection en appelant la fonction **SetWindowLong** avec *NINDEX* défini sur DWL \_ MSGRESULT et *lNewLong* défini sur **false** (cast en type de données **long** ).</span><span class="sxs-lookup"><span data-stu-id="b5ce3-129">If your application is processing a verify operation, it can prevent the dialog box from listing this selection by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="b5ce3-130">Pour autoriser la boîte de dialogue à répertorier cette sélection, appelez cette fonction avec *lNewLong* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-130">To allow the dialog box to list this selection, call this function with *lNewLong* set to **TRUE**.</span></span>

<span data-ttu-id="b5ce3-131">Si votre application traite une opération d’ajout, elle peut indiquer qu’aucun ajout supplémentaire n’est requis en appelant la fonction **SetWindowLong** avec *NINDEX* défini sur DWL \_ MSGRESULT et *lNewLong* défini sur **false** (cast en type de données **long** ).</span><span class="sxs-lookup"><span data-stu-id="b5ce3-131">If your application is processing an add operation, it can indicate that no more additions are required by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="b5ce3-132">Pour indiquer que des ajouts supplémentaires sont nécessaires, appelez cette fonction avec *lNewLong* défini sur **true**.</span><span class="sxs-lookup"><span data-stu-id="b5ce3-132">To indicate more additions are required, call this function with *lNewLong* set to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ce3-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5ce3-133">Requirements</span></span>



| <span data-ttu-id="b5ce3-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5ce3-134">Requirement</span></span> | <span data-ttu-id="b5ce3-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5ce3-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ce3-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ce3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b5ce3-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5ce3-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b5ce3-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5ce3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b5ce3-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5ce3-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5ce3-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5ce3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5ce3-141"><dt>Msacm. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5ce3-141"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5ce3-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5ce3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ce3-143">Gestionnaire de compression audio</span><span class="sxs-lookup"><span data-stu-id="b5ce3-143">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b5ce3-144">Messages de compression audio</span><span class="sxs-lookup"><span data-stu-id="b5ce3-144">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

