---
title: Constantes TF_LBI_ (Ctfutb. h)
description: Les \_ \_ constantes IFA IFA \ sont utilisées avec la méthode ITfLangBarItemSink OnUpdate pour indiquer les éléments de barre de langue qui ont été modifiés.
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511354"
---
# <a name="tf_lbi_-constants"></a><span data-ttu-id="73cd9-103">\_Constantes de TF IFA \_ \*</span><span class="sxs-lookup"><span data-stu-id="73cd9-103">TF\_LBI\_\* Constants</span></span>

<span data-ttu-id="73cd9-104">Les constantes \**tf \_ IFA \_ \** _ sont utilisées avec la méthode [ITfLangBarItemSink :: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) pour indiquer les éléments de barre de langue qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="73cd9-104">The \**TF\_LBI\_\** _ constants are used with the [ITfLangBarItemSink::OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) method to indicate which language bar items changed.</span></span>



| <span data-ttu-id="73cd9-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="73cd9-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="73cd9-106">Description</span><span class="sxs-lookup"><span data-stu-id="73cd9-106">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <span data-ttu-id="73cd9-107"><dt>_ \* TF \_ \_Icône IFA \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="73cd9-107"><dt>_\*TF\_LBI\_ICON\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                                                        | <span data-ttu-id="73cd9-108">L’icône de l’élément a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="73cd9-108">The icon of the item has changed.</span></span> <span data-ttu-id="73cd9-109">La barre de langage appelle [ITfLangBarItemButton :: GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) en réponse à cette notification.</span><span class="sxs-lookup"><span data-stu-id="73cd9-109">The language bar calls [ITfLangBarItemButton::GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) in response to this notification.</span></span><br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <span data-ttu-id="73cd9-110"><dt>**Tf \_ \_Texte IFA**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="73cd9-110"><dt>**TF\_LBI\_TEXT**</dt> <dt>0x00000002</dt></span></span> </dl>                                                        | <span data-ttu-id="73cd9-111">Le texte d’un bouton ou d’un élément de bouton bitmap a changé.</span><span class="sxs-lookup"><span data-stu-id="73cd9-111">The text of a button or bitmap button item has changed.</span></span> <span data-ttu-id="73cd9-112">La barre de langage appelle [ITfLangBarItemButton :: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) ou [ITfLangBarItemBitmapButton :: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), selon ce qui est approprié, en réponse à cette notification.</span><span class="sxs-lookup"><span data-stu-id="73cd9-112">The language bar calls [ITfLangBarItemButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) or [ITfLangBarItemBitmapButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), whichever is appropriate, in response to this notification.</span></span><br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <span data-ttu-id="73cd9-113"><dt>**Tf \_ \_INFOBULLE IFA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="73cd9-113"><dt>**TF\_LBI\_TOOLTIP**</dt> <dt>0x00000004</dt></span></span> </dl>                                               | <span data-ttu-id="73cd9-114">Texte d’info-bulle de l’élément modifié.</span><span class="sxs-lookup"><span data-stu-id="73cd9-114">The tooltip text of the item changed.</span></span> <span data-ttu-id="73cd9-115">La barre de langage appelle [ITfLangBarItem :: GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) en réponse à cette notification.</span><span class="sxs-lookup"><span data-stu-id="73cd9-115">The language bar calls [ITfLangBarItem::GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) in response to this notification.</span></span><br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <span data-ttu-id="73cd9-116"><dt>**Tf \_ IFA \_ bitmap IFA**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="73cd9-116"><dt>**TF\_LBI\_BITMAP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                  | <span data-ttu-id="73cd9-117">Bitmap d’un élément de bouton bitmap ou bitmap modifié.</span><span class="sxs-lookup"><span data-stu-id="73cd9-117">The bitmap of a bitmap or bitmap button item changed.</span></span> <span data-ttu-id="73cd9-118">La barre de langage appelle [ITfLangBarItemBitmap ::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) ou [ITfLangBarItemBitmapButton ::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), selon ce qui est approprié, en réponse à cette notification.</span><span class="sxs-lookup"><span data-stu-id="73cd9-118">The language bar calls [ITfLangBarItemBitmap::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) or [ITfLangBarItemBitmapButton::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), whichever is appropriate, in response to this notification.</span></span><br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <span data-ttu-id="73cd9-119"><dt>**Tf \_ \_Bulle IFA**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="73cd9-119"><dt>**TF\_LBI\_BALLOON**</dt> <dt>0x00000010</dt></span></span> </dl>                                               | <span data-ttu-id="73cd9-120">Les informations relatives à un élément Balloon ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="73cd9-120">The information for a balloon item changed.</span></span> <span data-ttu-id="73cd9-121">La barre de langage appelle [ITfLangBarItemBalloon :: GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) en réponse à cette notification.</span><span class="sxs-lookup"><span data-stu-id="73cd9-121">The language bar calls [ITfLangBarItemBalloon::GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) in response to this notification.</span></span><br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <span data-ttu-id="73cd9-122"><dt>**Tf \_ 0x00010000 \_ État IFA**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="73cd9-122"><dt>**TF\_LBI\_STATUS**</dt> <dt>0x00010000</dt></span></span> </dl>                                                  | <span data-ttu-id="73cd9-123">État de l’élément modifié.</span><span class="sxs-lookup"><span data-stu-id="73cd9-123">The item status changed.</span></span> <span data-ttu-id="73cd9-124">La barre de langage appelle [ITfLangBarItem :: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) en réponse à cette notification.</span><span class="sxs-lookup"><span data-stu-id="73cd9-124">The language bar calls [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) in response to this notification.</span></span><br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <span data-ttu-id="73cd9-125"><dt>**Tf \_ icône IFA \_ BMPALL**</dt> <dt>tf \_ IFA \_ bitmap \| tf \_ IFA \_</dt></span><span class="sxs-lookup"><span data-stu-id="73cd9-125"><dt>**TF\_LBI\_BMPALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>                          | <span data-ttu-id="73cd9-126">Combine une \_ \_ image bitmap TF IFA et une \_ \_ info-bulle TF IFA.</span><span class="sxs-lookup"><span data-stu-id="73cd9-126">Combines TF\_LBI\_BITMAP and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <span data-ttu-id="73cd9-127"><dt>**Tf \_ IFA \_ BMPBTNALL**</dt> <dt>tf \_ IFA \_ bitmap \| tf \_ IFA \_ texte \| tf \_ IFA \_ info-bulle</dt></span><span class="sxs-lookup"><span data-stu-id="73cd9-127"><dt>**TF\_LBI\_BMPBTNALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl> | <span data-ttu-id="73cd9-128">Combine l' \_ \_ image bitmap TF IFA, le \_ texte TF IFA et l' \_ \_ \_ info-bulle TF IFA.</span><span class="sxs-lookup"><span data-stu-id="73cd9-128">Combines TF\_LBI\_BITMAP, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <span data-ttu-id="73cd9-129"><dt>**Tf \_ icône IFA \_ BTNALL**</dt> <dt>tf \_ IFA \_ \| tf \_ IFA \_ texte \| tf \_ IFA \_ info-bulle</dt></span><span class="sxs-lookup"><span data-stu-id="73cd9-129"><dt>**TF\_LBI\_BTNALL**</dt> <dt>TF\_LBI\_ICON\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>            | <span data-ttu-id="73cd9-130">Combine l' \_ icône TF IFA \_ , le \_ texte TF IFA et l' \_ \_ \_ info-bulle TF IFA.</span><span class="sxs-lookup"><span data-stu-id="73cd9-130">Combines TF\_LBI\_ICON, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="73cd9-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73cd9-131">Requirements</span></span>



| <span data-ttu-id="73cd9-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73cd9-132">Requirement</span></span> | <span data-ttu-id="73cd9-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="73cd9-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73cd9-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73cd9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="73cd9-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73cd9-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="73cd9-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73cd9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="73cd9-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73cd9-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73cd9-138">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="73cd9-138">Redistributable</span></span><br/>          | <span data-ttu-id="73cd9-139">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="73cd9-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="73cd9-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="73cd9-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="73cd9-141"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="73cd9-141"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="73cd9-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="73cd9-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="73cd9-143"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="73cd9-143"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73cd9-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73cd9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73cd9-145">ITfLangBarItemSink :: OnUpdate</span><span class="sxs-lookup"><span data-stu-id="73cd9-145">ITfLangBarItemSink::OnUpdate</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





