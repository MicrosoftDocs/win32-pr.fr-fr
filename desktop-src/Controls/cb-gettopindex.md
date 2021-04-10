---
title: Message CB_GETTOPINDEX (winuser. h)
description: Une application envoie le \_ message CB GETTOPINDEX pour récupérer l’index de base zéro du premier élément visible dans la partie zone de liste d’une zone de liste déroulante.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- CB_GETTOPINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942112"
---
# <a name="cb_gettopindex-message"></a><span data-ttu-id="58ec7-104">\_Message GETTOPINDEX CB</span><span class="sxs-lookup"><span data-stu-id="58ec7-104">CB\_GETTOPINDEX message</span></span>

<span data-ttu-id="58ec7-105">Une application envoie le message **CB \_ GETTOPINDEX** pour récupérer l’index de base zéro du premier élément visible dans la partie zone de liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="58ec7-105">An application sends the **CB\_GETTOPINDEX** message to retrieve the zero-based index of the first visible item in the list box portion of a combo box.</span></span> <span data-ttu-id="58ec7-106">Initialement, l’élément avec l’index 0 est en haut de la zone de liste, mais si le contenu de la zone de liste a fait l’objet d’un défilement, un autre élément peut se trouver en haut.</span><span class="sxs-lookup"><span data-stu-id="58ec7-106">Initially, the item with index 0 is at the top of the list box, but if the list box contents have been scrolled, another item may be at the top.</span></span>

## <a name="parameters"></a><span data-ttu-id="58ec7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58ec7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58ec7-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58ec7-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58ec7-109">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="58ec7-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="58ec7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58ec7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58ec7-111">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="58ec7-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58ec7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58ec7-112">Return value</span></span>

<span data-ttu-id="58ec7-113">Si le message est réussi, la valeur de retour est l’index du premier élément visible dans la zone de liste de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="58ec7-113">If the message is successful, the return value is the index of the first visible item in the list box of the combo box.</span></span>

<span data-ttu-id="58ec7-114">Si le message échoue, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="58ec7-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ec7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58ec7-115">Requirements</span></span>



| <span data-ttu-id="58ec7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58ec7-116">Requirement</span></span> | <span data-ttu-id="58ec7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="58ec7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58ec7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58ec7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="58ec7-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58ec7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="58ec7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58ec7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="58ec7-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58ec7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="58ec7-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="58ec7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="58ec7-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58ec7-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ec7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58ec7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ec7-125">**\_SETTOPINDEX CB**</span><span class="sxs-lookup"><span data-stu-id="58ec7-125">**CB\_SETTOPINDEX**</span></span>](cb-settopindex.md)
</dt> </dl>

 

 





