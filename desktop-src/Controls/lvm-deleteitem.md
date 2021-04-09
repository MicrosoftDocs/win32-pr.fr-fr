---
title: Message LVM_DELETEITEM (commctrl. h)
description: Supprime un élément d’un contrôle List-View. Vous pouvez envoyer ce message de manière explicite ou à l’aide de la macro de ListView \_ .
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- LVM_DELETEITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19fce5afbbaa6702f296df12acf7dad4edac16fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102904"
---
# <a name="lvm_deleteitem-message"></a><span data-ttu-id="7b221-105">Message de LVM. \_</span><span class="sxs-lookup"><span data-stu-id="7b221-105">LVM\_DELETEITEM message</span></span>

<span data-ttu-id="7b221-106">Supprime un élément d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="7b221-106">Removes an item from a list-view control.</span></span> <span data-ttu-id="7b221-107">Vous pouvez envoyer ce message de manière explicite ou à l’aide de la macro de [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="7b221-107">You can send this message explicitly or by using the [**ListView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b221-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b221-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b221-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b221-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b221-110">Index de l’élément de vue de liste à supprimer.</span><span class="sxs-lookup"><span data-stu-id="7b221-110">The index of the list-view item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="7b221-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b221-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7b221-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7b221-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b221-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b221-113">Return value</span></span>

<span data-ttu-id="7b221-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7b221-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b221-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b221-115">Requirements</span></span>



| <span data-ttu-id="7b221-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b221-116">Requirement</span></span> | <span data-ttu-id="7b221-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b221-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b221-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b221-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7b221-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b221-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b221-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b221-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7b221-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b221-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b221-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b221-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b221-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b221-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





