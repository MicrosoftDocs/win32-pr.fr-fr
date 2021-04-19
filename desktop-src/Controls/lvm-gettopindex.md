---
title: Message LVM_GETTOPINDEX (commctrl. h)
description: Récupère l’index de l’élément le plus visible en mode liste ou rapport. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetTopIndex.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- LVM_GETTOPINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510351"
---
# <a name="lvm_gettopindex-message"></a><span data-ttu-id="bd6db-105">\_Message GETTOPINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="bd6db-105">LVM\_GETTOPINDEX message</span></span>

<span data-ttu-id="bd6db-106">Récupère l’index de l’élément le plus visible en mode liste ou rapport.</span><span class="sxs-lookup"><span data-stu-id="bd6db-106">Retrieves the index of the topmost visible item when in list or report view.</span></span> <span data-ttu-id="bd6db-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetTopIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) .</span><span class="sxs-lookup"><span data-stu-id="bd6db-107">You can send this message explicitly or by using the [**ListView\_GetTopIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd6db-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd6db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd6db-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd6db-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bd6db-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bd6db-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bd6db-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd6db-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bd6db-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bd6db-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd6db-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bd6db-113">Return value</span></span>

<span data-ttu-id="bd6db-114">Retourne l’index de l’élément en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="bd6db-114">Returns the index of the item if successful.</span></span> <span data-ttu-id="bd6db-115">Retourne zéro si le contrôle d’affichage de liste est en mode icône ou petite icône, ou si le contrôle de liste est en mode Détails avec les groupes activés.</span><span class="sxs-lookup"><span data-stu-id="bd6db-115">Returns zero if the list-view control is in icon or small icon view, or if the list-view control is in details view with groups enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd6db-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd6db-116">Requirements</span></span>



| <span data-ttu-id="bd6db-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd6db-117">Requirement</span></span> | <span data-ttu-id="bd6db-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd6db-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6db-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd6db-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bd6db-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd6db-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd6db-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd6db-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bd6db-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd6db-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd6db-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd6db-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd6db-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd6db-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





