---
title: Message LVM_SETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Définit des styles étendus dans les contrôles d’affichage de liste. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro ListView SetExtendedListViewStyle ou ListView \_ SetExtendedListViewStyleEx.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- LVM_SETEXTENDEDLISTVIEWSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d36869283d863bef7b31187a002125c9cd79bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941673"
---
# <a name="lvm_setextendedlistviewstyle-message"></a><span data-ttu-id="de302-105">\_Message SETEXTENDEDLISTVIEWSTYLE LVM</span><span class="sxs-lookup"><span data-stu-id="de302-105">LVM\_SETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="de302-106">Définit des styles étendus dans les contrôles d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="de302-106">Sets extended styles in list-view controls.</span></span> <span data-ttu-id="de302-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) ou [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .</span><span class="sxs-lookup"><span data-stu-id="de302-107">You can send this message explicitly or use the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) or [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="de302-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de302-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de302-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de302-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de302-110">Valeur **DWORD** qui spécifie les styles de *lParam* à affecter.</span><span class="sxs-lookup"><span data-stu-id="de302-110">**DWORD** value that specifies which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="de302-111">Ce paramètre peut être une combinaison de [**styles de List-View étendus**](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="de302-111">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="de302-112">Seuls les styles étendus dans *wParam* seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="de302-112">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="de302-113">Tous les autres styles seront conservés tels quels.</span><span class="sxs-lookup"><span data-stu-id="de302-113">All other styles will be maintained as they are.</span></span> <span data-ttu-id="de302-114">Si ce paramètre est égal à zéro, tous les styles de *lParam* sont affectés.</span><span class="sxs-lookup"><span data-stu-id="de302-114">If this parameter is zero, all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="de302-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de302-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de302-116">Valeur **DWORD** qui spécifie les styles de contrôle de vue de liste étendus à définir.</span><span class="sxs-lookup"><span data-stu-id="de302-116">**DWORD** value that specifies the extended list-view control styles to set.</span></span> <span data-ttu-id="de302-117">Ce paramètre peut être une combinaison de [**styles de List-View étendus**](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="de302-117">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="de302-118">Les styles qui ne sont pas définis, mais qui sont spécifiés dans *wParam*, sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="de302-118">Styles that are not set, but that are specified in *wParam*, are removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de302-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de302-119">Return value</span></span>

<span data-ttu-id="de302-120">Retourne une valeur **DWORD** qui contient les styles de contrôle de vue de liste étendus précédents.</span><span class="sxs-lookup"><span data-stu-id="de302-120">Returns a **DWORD** value that contains the previous extended list-view control styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="de302-121">Notes</span><span class="sxs-lookup"><span data-stu-id="de302-121">Remarks</span></span>

<span data-ttu-id="de302-122">Le paramètre *wParam* vous permet de modifier un ou plusieurs styles étendus sans avoir à récupérer d’abord les styles existants.</span><span class="sxs-lookup"><span data-stu-id="de302-122">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="de302-123">Par exemple, si vous transmettez [**LVS \_ ex \_ FULLROWSELECT**](extended-list-view-styles.md) pour *wParam* et 0 pour *lParam*, le style **LVS \_ ex \_ FULLROWSELECT** sera effacé, mais tous les autres styles resteront les mêmes.</span><span class="sxs-lookup"><span data-stu-id="de302-123">For example, if you pass [**LVS\_EX\_FULLROWSELECT**](extended-list-view-styles.md) for *wParam* and 0 for *lParam*, the **LVS\_EX\_FULLROWSELECT** style will be cleared but all other styles will remain the same.</span></span>

<span data-ttu-id="de302-124">Pour des raisons de compatibilité descendante, la macro [**\_ SetExtendedListViewStyle ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) n’a pas été mise à jour pour utiliser *wParam*.</span><span class="sxs-lookup"><span data-stu-id="de302-124">For backward compatibility reasons, the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) macro has not been updated to use *wParam*.</span></span> <span data-ttu-id="de302-125">Pour utiliser la valeur *wParam* , utilisez la macro [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .</span><span class="sxs-lookup"><span data-stu-id="de302-125">To use the *wParam* value, use the [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

<span data-ttu-id="de302-126">Lorsque vous utilisez ce message pour définir le style de [**\_ cases à \_ cocher LVS ex**](extended-list-view-styles.md) , tout index d’image d’état précédemment défini sera ignoré.</span><span class="sxs-lookup"><span data-stu-id="de302-126">When you use this message to set the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style, any previously set state image index will be discarded.</span></span> <span data-ttu-id="de302-127">Toutes les cases à cocher seront initialisées à l’état non vérifié.</span><span class="sxs-lookup"><span data-stu-id="de302-127">All check boxes will be initialized to the unchecked state.</span></span> <span data-ttu-id="de302-128">L’index d’image d’État est contenu dans les bits 12 à 15 du membre d' **État** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="de302-128">The state image index is contained in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="de302-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de302-129">Requirements</span></span>



| <span data-ttu-id="de302-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de302-130">Requirement</span></span> | <span data-ttu-id="de302-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="de302-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de302-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de302-132">Minimum supported client</span></span><br/> | <span data-ttu-id="de302-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de302-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de302-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de302-134">Minimum supported server</span></span><br/> | <span data-ttu-id="de302-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de302-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de302-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="de302-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="de302-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="de302-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





