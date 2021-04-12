---
title: Message LVM_GETGROUPINFOBYINDEX (commctrl. h)
description: Obtient des informations sur un groupe spécifié. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetGroupInfoByIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getgroupinfobyindex.htm
keywords:
- LVM_GETGROUPINFOBYINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFOBYINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff801eae55ab4b4194ef23e624ff6eff75fbc25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104458"
---
# <a name="lvm_getgroupinfobyindex-message"></a><span data-ttu-id="4aae8-105">\_Message GETGROUPINFOBYINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="4aae8-105">LVM\_GETGROUPINFOBYINDEX message</span></span>

<span data-ttu-id="4aae8-106">Obtient des informations sur un groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="4aae8-106">Gets information on a specified group.</span></span> <span data-ttu-id="4aae8-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetGroupInfoByIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) .</span><span class="sxs-lookup"><span data-stu-id="4aae8-107">Send this message explicitly or by using the [**ListView\_GetGroupInfoByIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupinfobyindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4aae8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4aae8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aae8-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4aae8-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4aae8-110">Index du groupe.</span><span class="sxs-lookup"><span data-stu-id="4aae8-110">The index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="4aae8-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4aae8-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aae8-112">Pointeur vers une structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) pour recevoir des informations sur le groupe spécifié par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="4aae8-112">A pointer to an [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="4aae8-113">Le processus appelant est chargé d’allouer de la mémoire pour la structure et toutes les mémoires tampons de la structure, telles que celle sur laquelle pointe le membre **pszHeader** .</span><span class="sxs-lookup"><span data-stu-id="4aae8-113">The calling process is responsible for allocating memory for the structure and any buffers in the structure, such as the one pointed to by the **pszHeader** member.</span></span> <span data-ttu-id="4aae8-114">Définissez tous les membres conditionnels de la structure, tels que **cchHeader** , la taille de la mémoire tampon vers laquelle pointe **pszHeader** dans **WCHARs** , y compris le caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="4aae8-114">Set any contingent members of the structure, such as **cchHeader** the size of the buffer pointed to by **pszHeader** in **WCHARs** including the terminating **NULL**.</span></span> <span data-ttu-id="4aae8-115">Définissez **cbSize** sur sizeof (LVGROUP).</span><span class="sxs-lookup"><span data-stu-id="4aae8-115">Set **cbSize** to sizeof(LVGROUP).</span></span>

<span data-ttu-id="4aae8-116">Le récepteur de messages est chargé de définir les membres de structure avec les informations relatives au groupe spécifié par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="4aae8-116">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aae8-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4aae8-117">Return value</span></span>

<span data-ttu-id="4aae8-118">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4aae8-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aae8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4aae8-119">Requirements</span></span>



| <span data-ttu-id="4aae8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4aae8-120">Requirement</span></span> | <span data-ttu-id="4aae8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4aae8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4aae8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aae8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4aae8-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4aae8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4aae8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aae8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4aae8-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4aae8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4aae8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="4aae8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aae8-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aae8-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





