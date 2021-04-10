---
title: Message LVM_SETTEXTBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan du texte dans un contrôle de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetTextBkColor.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- LVM_SETTEXTBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032692"
---
# <a name="lvm_settextbkcolor-message"></a><span data-ttu-id="8181b-105">\_Message SETTEXTBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="8181b-105">LVM\_SETTEXTBKCOLOR message</span></span>

<span data-ttu-id="8181b-106">Définit la couleur d’arrière-plan du texte dans un contrôle de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="8181b-106">Sets the background color of text in a list-view control.</span></span> <span data-ttu-id="8181b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="8181b-107">You can send this message explicitly or by using the [**ListView\_SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8181b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8181b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8181b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8181b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8181b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8181b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8181b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8181b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8181b-112">Nouvelle couleur d’arrière-plan du texte.</span><span class="sxs-lookup"><span data-stu-id="8181b-112">New text background color.</span></span> <span data-ttu-id="8181b-113">Il peut s’agir \_ de CLR None pour aucune couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8181b-113">This can be CLR\_NONE for no background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8181b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8181b-114">Return value</span></span>

<span data-ttu-id="8181b-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8181b-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8181b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8181b-116">Requirements</span></span>



| <span data-ttu-id="8181b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8181b-117">Requirement</span></span> | <span data-ttu-id="8181b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8181b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8181b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8181b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8181b-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8181b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8181b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8181b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8181b-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8181b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8181b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8181b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8181b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8181b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





