---
title: Message CB_GETITEMDATA (winuser. h)
description: Une application envoie un \_ message GETITEMDATA CB à une zone de liste déroulante pour récupérer la valeur fournie par l’application associée à l’élément spécifié dans la zone de liste déroulante.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- CB_GETITEMDATA les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643954cf266c52ccbeae082ffacf317c91bc7b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741453"
---
# <a name="cb_getitemdata-message"></a><span data-ttu-id="5ffe0-104">\_Message GETITEMDATA CB</span><span class="sxs-lookup"><span data-stu-id="5ffe0-104">CB\_GETITEMDATA message</span></span>

<span data-ttu-id="5ffe0-105">Une application envoie un **message \_ GETITEMDATA CB** à une zone de liste déroulante pour récupérer la valeur fournie par l’application associée à l’élément spécifié dans la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="5ffe0-105">An application sends a **CB\_GETITEMDATA** message to a combo box to retrieve the application-supplied value associated with the specified item in the combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ffe0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ffe0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ffe0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ffe0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ffe0-108">Index de base zéro de l'élément.</span><span class="sxs-lookup"><span data-stu-id="5ffe0-108">The zero-based index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="5ffe0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ffe0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ffe0-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="5ffe0-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ffe0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ffe0-111">Return value</span></span>

<span data-ttu-id="5ffe0-112">La valeur de retour est la valeur associée à l’élément.</span><span class="sxs-lookup"><span data-stu-id="5ffe0-112">The return value is the value associated with the item.</span></span> <span data-ttu-id="5ffe0-113">Si une erreur se produit, il s’agit de CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="5ffe0-113">If an error occurs, it is CB\_ERR.</span></span>

<span data-ttu-id="5ffe0-114">Si l’élément se trouve dans une zone de liste déroulante owner-drawn créée sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , la valeur de retour est la valeur contenue dans le paramètre *lParam* du message [**CB \_ ADDSTRING**](cb-addstring.md) ou [**CB \_ INSERTSTRING**](cb-insertstring.md) , qui a ajouté l’élément à la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="5ffe0-114">If the item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the return value is the value contained in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message, that added the item to the combo box.</span></span> <span data-ttu-id="5ffe0-115">Si le **style \_ HASSTRINGS CBS** n’a pas été utilisé, la valeur de retour est le paramètre *lParam* contenu dans un message [**CB \_ SETITEMDATA**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="5ffe0-115">If the **CBS\_HASSTRINGS** style was not used, the return value is the *lParam* parameter contained in a [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ffe0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ffe0-116">Requirements</span></span>



| <span data-ttu-id="5ffe0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ffe0-117">Requirement</span></span> | <span data-ttu-id="5ffe0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ffe0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ffe0-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ffe0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5ffe0-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ffe0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ffe0-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ffe0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5ffe0-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ffe0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ffe0-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ffe0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ffe0-124"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ffe0-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ffe0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ffe0-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ffe0-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5ffe0-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5ffe0-127">**$ \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="5ffe0-127">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="5ffe0-128">**\_INSERTSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="5ffe0-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="5ffe0-129">**\_SETITEMDATA CB**</span><span class="sxs-lookup"><span data-stu-id="5ffe0-129">**CB\_SETITEMDATA**</span></span>](cb-setitemdata.md)
</dt> </dl>

 

 





