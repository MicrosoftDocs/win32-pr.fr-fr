---
title: Message CBEM_DELETEITEM (commctrl. h)
description: Supprime un élément d’un contrôle ComboBoxEx.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- CBEM_DELETEITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509133"
---
# <a name="cbem_deleteitem-message"></a><span data-ttu-id="bbc0b-104">\_Message CBEM DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="bbc0b-104">CBEM\_DELETEITEM message</span></span>

<span data-ttu-id="bbc0b-105">Supprime un élément d’un contrôle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="bbc0b-105">Removes an item from a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbc0b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbc0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbc0b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbc0b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbc0b-108">Index de base zéro de l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="bbc0b-108">The zero-based index of the item to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="bbc0b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbc0b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bbc0b-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bbc0b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbc0b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bbc0b-111">Return value</span></span>

<span data-ttu-id="bbc0b-112">Retourne une valeur INT qui représente le nombre d’éléments restants dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="bbc0b-112">Returns an INT value that represents the number of items remaining in the control.</span></span> <span data-ttu-id="bbc0b-113">Si *iIndex* n’est pas valide, le message retourne CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="bbc0b-113">If *iIndex* is invalid, the message returns CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbc0b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bbc0b-114">Remarks</span></span>

<span data-ttu-id="bbc0b-115">Ce message est mappé au message de contrôle de zone de liste déroulante [**CB \_ DELETESTRING**](cb-deletestring.md).</span><span class="sxs-lookup"><span data-stu-id="bbc0b-115">This message maps to the combo box control message [**CB\_DELETESTRING**](cb-deletestring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc0b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbc0b-116">Requirements</span></span>



| <span data-ttu-id="bbc0b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbc0b-117">Requirement</span></span> | <span data-ttu-id="bbc0b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbc0b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc0b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbc0b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc0b-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbc0b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbc0b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbc0b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc0b-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbc0b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbc0b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bbc0b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbc0b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbc0b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





