---
description: Représente les options disponibles lors de l’affichage d’un menu contextuel.
title: Constantes MP_POPUPFLAGS (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113967"
---
# <a name="mp_popupflags-constants"></a><span data-ttu-id="5ab76-103">\_Constantes POPUPFLAGS MP</span><span class="sxs-lookup"><span data-stu-id="5ab76-103">MP\_POPUPFLAGS constants</span></span>

<span data-ttu-id="5ab76-104">Représente les options disponibles lors de l’affichage d’un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="5ab76-104">Represent options available when displaying a pop-up menu.</span></span>



| <span data-ttu-id="5ab76-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="5ab76-105">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="5ab76-106">Description</span><span class="sxs-lookup"><span data-stu-id="5ab76-106">Description</span></span>                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <span data-ttu-id="5ab76-107"><dt>**MPPF \_ SETFOCUS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-107"><dt>**MPPF\_SETFOCUS**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="5ab76-108">Donnez le focus au menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="5ab76-108">Give the pop-up menu the focus.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <span data-ttu-id="5ab76-109"><dt>**MPPF \_ INITIALSELECT**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-109"><dt>**MPPF\_INITIALSELECT**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="5ab76-110">Sélectionnez le premier élément dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="5ab76-110">Select the first item in the pop-up menu.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <span data-ttu-id="5ab76-111"><dt>**MPPF \_ Noanimate**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-111"><dt>**MPPF\_NOANIMATE**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="5ab76-112">N’utilisez pas les animations système par défaut, par exemple en fondu, lors de l’affichage du menu.</span><span class="sxs-lookup"><span data-stu-id="5ab76-112">Do not use the default system animations, for example, fade-in, when displaying the menu.</span></span><br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <span data-ttu-id="5ab76-113"><dt>**MPPF \_ CLAVIER**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-113"><dt>**MPPF\_KEYBOARD**</dt> <dt>0x00000010</dt></span></span> </dl>                | <span data-ttu-id="5ab76-114">Activez le menu à l’aide d’un raccourci clavier.</span><span class="sxs-lookup"><span data-stu-id="5ab76-114">Activate the menu by a keyboard shortcut.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <span data-ttu-id="5ab76-115"><dt>**MPPF \_ Repositionner**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-115"><dt>**MPPF\_REPOSITION**</dt> <dt>0x00000020</dt></span></span> </dl>          | <span data-ttu-id="5ab76-116">Affichez la barre à une autre position, en fonction des modifications apportées au menu.</span><span class="sxs-lookup"><span data-stu-id="5ab76-116">Display the bar in a different position, based on changes to the menu.</span></span><br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <span data-ttu-id="5ab76-117"><dt>**MPPF \_ FORCEZORDER**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-117"><dt>**MPPF\_FORCEZORDER**</dt> <dt>0x00000040</dt></span></span> </dl>       | <span data-ttu-id="5ab76-118">Réservé.</span><span class="sxs-lookup"><span data-stu-id="5ab76-118">Reserved.</span></span> <span data-ttu-id="5ab76-119">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="5ab76-119">Do not use.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <span data-ttu-id="5ab76-120"><dt>**MPPF \_ FINALSELECT**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-120"><dt>**MPPF\_FINALSELECT**</dt> <dt>0x00000080</dt></span></span> </dl>       | <span data-ttu-id="5ab76-121">Sélectionnez le dernier élément dans le menu.</span><span class="sxs-lookup"><span data-stu-id="5ab76-121">Select the last item in the menu.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <span data-ttu-id="5ab76-122"><dt>**MPPF \_ Aligner à \_ gauche**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-122"><dt>**MPPF\_ALIGN\_LEFT**</dt> <dt>0x02000000</dt></span></span> </dl>         | <span data-ttu-id="5ab76-123">**Windows Vista ou version ultérieure**: Alignez le menu contextuel à gauche de la zone spécifiée dans le paramètre *prcExclude* de [**ITrackShellMenu ::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup ::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="5ab76-123">**Windows Vista or later**: Align the pop-up menu to the left of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span> <span data-ttu-id="5ab76-124">Il s’agit de l’alignement par défaut.</span><span class="sxs-lookup"><span data-stu-id="5ab76-124">This is the default alignment.</span></span><br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <span data-ttu-id="5ab76-125"><dt>**MPPF \_ Aligner à \_ droite**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-125"><dt>**MPPF\_ALIGN\_RIGHT**</dt> <dt>0x04000000</dt></span></span> </dl>      | <span data-ttu-id="5ab76-126">**Windows Vista ou version ultérieure**: Alignez le menu contextuel à droite de la zone spécifiée dans le paramètre *prcExclude* de [**ITrackShellMenu ::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup ::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="5ab76-126">**Windows Vista or later**: Align the pop-up menu to the right of the area specified in the *prcExclude* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <span data-ttu-id="5ab76-127"><dt>**MPPF \_ TOP**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-127"><dt>**MPPF\_TOP**</dt> <dt>0x20000000</dt></span></span> </dl>                               | <span data-ttu-id="5ab76-128">Placez le menu contextuel au-dessus du point initial spécifié dans le paramètre *PPT* de [**ITrackShellMenu ::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup ::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span><span class="sxs-lookup"><span data-stu-id="5ab76-128">Position the pop-up menu above the initial point specified in the *ppt* parameter of [**ITrackShellMenu::Popup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) or [**IMenuPopup::Popup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).</span></span><br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <span data-ttu-id="5ab76-129"><dt>**MPPF \_**</dt> <dt>0x40000000</dt> gauche</span><span class="sxs-lookup"><span data-stu-id="5ab76-129"><dt>**MPPF\_LEFT**</dt> <dt>0x40000000</dt></span></span> </dl>                            | <span data-ttu-id="5ab76-130">Placez le menu contextuel à gauche du point initial.</span><span class="sxs-lookup"><span data-stu-id="5ab76-130">Position the pop-up menu to the left of the initial point.</span></span><br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <span data-ttu-id="5ab76-131"><dt>**MPPF \_**</dt> <dt>0x60000000</dt> droit</span><span class="sxs-lookup"><span data-stu-id="5ab76-131"><dt>**MPPF\_RIGHT**</dt> <dt>0x60000000</dt></span></span> </dl>                         | <span data-ttu-id="5ab76-132">Placez le menu contextuel à droite du point initial.</span><span class="sxs-lookup"><span data-stu-id="5ab76-132">Position the pop-up menu to the right of the initial point.</span></span><br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <span data-ttu-id="5ab76-133"><dt>**MPPF \_ BOTTOM**</dt> <dt>(int) 0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-133"><dt>**MPPF\_BOTTOM**</dt> <dt>(int)0x80000000</dt></span></span> </dl>                 | <span data-ttu-id="5ab76-134">Placez le menu contextuel sous le point initial.</span><span class="sxs-lookup"><span data-stu-id="5ab76-134">Position the pop-up menu below the initial point.</span></span><br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <span data-ttu-id="5ab76-135"><dt>**MPPF \_ 0xE0000000 \_ masque de PDV**</dt> <dt>(int)</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-135"><dt>**MPPF\_POS\_MASK**</dt> <dt>(int)0xE0000000</dt></span></span> </dl>          | <span data-ttu-id="5ab76-136">Masque de position de menu.</span><span class="sxs-lookup"><span data-stu-id="5ab76-136">The menu position mask.</span></span><br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="5ab76-137">Notes</span><span class="sxs-lookup"><span data-stu-id="5ab76-137">Remarks</span></span>

<span data-ttu-id="5ab76-138">Ces constantes sont définies dans le fichier ShObjIdl. h à partir de Windows XP Service Pack 1 (SP1) et Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5ab76-138">These constants are defined in the Shobjidl.h file beginning in Windows XP Service Pack 1 (SP1) and Windows Server 2003</span></span>

## <a name="requirements"></a><span data-ttu-id="5ab76-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5ab76-139">Requirements</span></span>



| <span data-ttu-id="5ab76-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ab76-140">Requirement</span></span> | <span data-ttu-id="5ab76-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ab76-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab76-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ab76-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab76-143">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ab76-143">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5ab76-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ab76-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab76-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ab76-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5ab76-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ab76-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ab76-147"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-147"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ab76-148">MIDL</span><span class="sxs-lookup"><span data-stu-id="5ab76-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ab76-149"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ab76-149"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ab76-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ab76-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab76-151">**IMenuPopup ::P opup**</span><span class="sxs-lookup"><span data-stu-id="5ab76-151">**IMenuPopup::Popup**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[<span data-ttu-id="5ab76-152">**ITrackShellMenu ::P opup**</span><span class="sxs-lookup"><span data-stu-id="5ab76-152">**ITrackShellMenu::Popup**</span></span>](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




