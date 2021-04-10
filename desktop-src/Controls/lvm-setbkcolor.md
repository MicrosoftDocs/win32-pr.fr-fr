---
title: Message LVM_SETBKCOLOR (commctrl. h)
description: Définit la couleur d’arrière-plan d’un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetBkColor.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- LVM_SETBKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942380"
---
# <a name="lvm_setbkcolor-message"></a><span data-ttu-id="b40cb-105">\_Message SETBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="b40cb-105">LVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="b40cb-106">Définit la couleur d’arrière-plan d’un contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="b40cb-106">Sets the background color of a list-view control.</span></span> <span data-ttu-id="b40cb-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="b40cb-107">You can send this message explicitly or by using the [**ListView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b40cb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b40cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b40cb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b40cb-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b40cb-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b40cb-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b40cb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b40cb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b40cb-112">Couleur d’arrière-plan à définir ou \_ valeur CLR None pour aucune couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b40cb-112">Background color to set or the CLR\_NONE value for no background color.</span></span> <span data-ttu-id="b40cb-113">Les contrôles d’affichage de liste avec des couleurs d’arrière-plan se redessinent beaucoup plus rapidement que ceux sans couleurs d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b40cb-113">List-view controls with background colors redraw themselves significantly faster than those without background colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b40cb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b40cb-114">Return value</span></span>

<span data-ttu-id="b40cb-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b40cb-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b40cb-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b40cb-116">Requirements</span></span>



| <span data-ttu-id="b40cb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b40cb-117">Requirement</span></span> | <span data-ttu-id="b40cb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b40cb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b40cb-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b40cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b40cb-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b40cb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b40cb-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b40cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b40cb-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b40cb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b40cb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b40cb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b40cb-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b40cb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





