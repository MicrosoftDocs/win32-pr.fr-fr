---
title: Message LVM_GETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Obtient les styles étendus en cours d’utilisation pour un contrôle List-View donné. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetExtendedListViewStyle.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- LVM_GETEXTENDEDLISTVIEWSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032355"
---
# <a name="lvm_getextendedlistviewstyle-message"></a><span data-ttu-id="a474f-105">\_Message GETEXTENDEDLISTVIEWSTYLE LVM</span><span class="sxs-lookup"><span data-stu-id="a474f-105">LVM\_GETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="a474f-106">Obtient les styles étendus en cours d’utilisation pour un contrôle List-View donné.</span><span class="sxs-lookup"><span data-stu-id="a474f-106">Gets the extended styles that are currently in use for a given list-view control.</span></span> <span data-ttu-id="a474f-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) .</span><span class="sxs-lookup"><span data-stu-id="a474f-107">You can send this message explicitly or use the [**ListView\_GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a474f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a474f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a474f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a474f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a474f-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a474f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a474f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a474f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a474f-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a474f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a474f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a474f-113">Return value</span></span>

<span data-ttu-id="a474f-114">Retourne une **valeur DWORD** qui représente les styles en cours d’utilisation pour un contrôle List View donné.</span><span class="sxs-lookup"><span data-stu-id="a474f-114">Returns a **DWORD** that represents the styles currently in use for a given list-view control.</span></span> <span data-ttu-id="a474f-115">Cette valeur peut être une combinaison de [styles de List-View étendus](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="a474f-115">This value can be a combination of [Extended List-View Styles](extended-list-view-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a474f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a474f-116">Requirements</span></span>



| <span data-ttu-id="a474f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a474f-117">Requirement</span></span> | <span data-ttu-id="a474f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a474f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a474f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a474f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a474f-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a474f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a474f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a474f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a474f-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a474f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a474f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="a474f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a474f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a474f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





