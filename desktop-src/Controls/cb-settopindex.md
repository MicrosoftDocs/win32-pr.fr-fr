---
title: Message CB_SETTOPINDEX (winuser. h)
description: Une application envoie le \_ message CB SETTOPINDEX pour s’assurer qu’un élément particulier est visible dans la zone de liste d’une zone de liste déroulante.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- CB_SETTOPINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740117"
---
# <a name="cb_settopindex-message"></a><span data-ttu-id="63aca-104">\_Message SETTOPINDEX CB</span><span class="sxs-lookup"><span data-stu-id="63aca-104">CB\_SETTOPINDEX message</span></span>

<span data-ttu-id="63aca-105">Une application envoie le message **CB \_ SETTOPINDEX** pour s’assurer qu’un élément particulier est visible dans la zone de liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="63aca-105">An application sends the **CB\_SETTOPINDEX** message to ensure that a particular item is visible in the list box of a combo box.</span></span> <span data-ttu-id="63aca-106">Le système fait défiler le contenu de la zone de liste afin que l’élément spécifié apparaisse en haut de la zone de liste ou que la plage de défilement maximale ait été atteinte.</span><span class="sxs-lookup"><span data-stu-id="63aca-106">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="63aca-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63aca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63aca-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63aca-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63aca-109">Spécifie l’index de base zéro de l’élément de liste.</span><span class="sxs-lookup"><span data-stu-id="63aca-109">Specifies the zero-based index of the list item.</span></span>

</dd> <dt>

<span data-ttu-id="63aca-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63aca-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63aca-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="63aca-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63aca-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63aca-112">Return value</span></span>

<span data-ttu-id="63aca-113">Si le message réussit, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="63aca-113">If the message is successful, the return value is zero.</span></span>

<span data-ttu-id="63aca-114">Si le message échoue, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="63aca-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="63aca-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63aca-115">Requirements</span></span>



| <span data-ttu-id="63aca-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63aca-116">Requirement</span></span> | <span data-ttu-id="63aca-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="63aca-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63aca-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63aca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63aca-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63aca-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="63aca-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63aca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63aca-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63aca-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="63aca-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="63aca-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="63aca-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63aca-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63aca-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63aca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63aca-125">**\_GETTOPINDEX CB**</span><span class="sxs-lookup"><span data-stu-id="63aca-125">**CB\_GETTOPINDEX**</span></span>](cb-gettopindex.md)
</dt> </dl>

 

 





