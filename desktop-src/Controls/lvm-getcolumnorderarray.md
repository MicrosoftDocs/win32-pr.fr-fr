---
title: Message LVM_GETCOLUMNORDERARRAY (commctrl. h)
description: Obtient l’ordre de gauche à droite actuel des colonnes dans un contrôle de vue de liste. Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro ListView GetColumnOrderArray.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- LVM_GETCOLUMNORDERARRAY les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032359"
---
# <a name="lvm_getcolumnorderarray-message"></a><span data-ttu-id="b188d-105">\_Message GETCOLUMNORDERARRAY LVM</span><span class="sxs-lookup"><span data-stu-id="b188d-105">LVM\_GETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="b188d-106">Obtient l’ordre de gauche à droite actuel des colonnes dans un contrôle de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="b188d-106">Gets the current left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="b188d-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro [**ListView \_ GetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) .</span><span class="sxs-lookup"><span data-stu-id="b188d-107">You can send this message explicitly or use the [**ListView\_GetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b188d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b188d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b188d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b188d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b188d-110">Nombre de colonnes dans le contrôle d’affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="b188d-110">The number of columns in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="b188d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b188d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b188d-112">Pointeur vers un tableau d’entiers qui reçoit les valeurs d’index des colonnes dans le contrôle de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="b188d-112">A pointer to an array of integers that receives the index values of the columns in the list-view control.</span></span> <span data-ttu-id="b188d-113">Le tableau doit être suffisamment grand pour contenir les éléments *wParam* .</span><span class="sxs-lookup"><span data-stu-id="b188d-113">The array must be large enough to hold *wParam* elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b188d-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b188d-114">Return value</span></span>

<span data-ttu-id="b188d-115">En cas de réussite, retourne une valeur différente de zéro et la mémoire tampon au niveau de *lParam* reçoit l’index de colonne de chaque colonne dans le contrôle dans l’ordre dans lequel elles apparaissent de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="b188d-115">If successful, returns nonzero, and the buffer at *lParam* receives the column index of each column in the control in the order they appear from left to right.</span></span> <span data-ttu-id="b188d-116">Sinon, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="b188d-116">Otherwise, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b188d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b188d-117">Requirements</span></span>



| <span data-ttu-id="b188d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b188d-118">Requirement</span></span> | <span data-ttu-id="b188d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b188d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b188d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b188d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b188d-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b188d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b188d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b188d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b188d-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b188d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b188d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b188d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b188d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b188d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





