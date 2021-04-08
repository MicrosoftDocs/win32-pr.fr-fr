---
title: Message CB_SETITEMDATA (winuser. h)
description: Une application envoie un \_ message CB SETITEMDATA pour définir la valeur associée à l’élément spécifié dans une zone de liste déroulante.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- CB_SETITEMDATA les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843901"
---
# <a name="cb_setitemdata-message"></a><span data-ttu-id="e09e0-104">\_Message SETITEMDATA CB</span><span class="sxs-lookup"><span data-stu-id="e09e0-104">CB\_SETITEMDATA message</span></span>

<span data-ttu-id="e09e0-105">Une application envoie un message **CB \_ SETITEMDATA** pour définir la valeur associée à l’élément spécifié dans une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="e09e0-105">An application sends a **CB\_SETITEMDATA** message to set the value associated with the specified item in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e09e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e09e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e09e0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e09e0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e09e0-108">Spécifie l’index de base zéro de l’élément.</span><span class="sxs-lookup"><span data-stu-id="e09e0-108">Specifies the item's zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="e09e0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e09e0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e09e0-110">Spécifie la nouvelle valeur à associer à l’élément.</span><span class="sxs-lookup"><span data-stu-id="e09e0-110">Specifies the new value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e09e0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e09e0-111">Return value</span></span>

<span data-ttu-id="e09e0-112">Si une erreur se produit, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="e09e0-112">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="e09e0-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e09e0-113">Remarks</span></span>

<span data-ttu-id="e09e0-114">Si l’élément spécifié se trouve dans une zone de liste déroulante owner-drawn créée sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , ce message remplace la valeur dans le paramètre *lParam* du message [**CB \_ ADDSTRING**](cb-addstring.md) ou [**CB \_ INSERTSTRING**](cb-insertstring.md) qui a ajouté l’élément à la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="e09e0-114">If the specified item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, this message replaces the value in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message that added the item to the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="e09e0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e09e0-115">Requirements</span></span>



| <span data-ttu-id="e09e0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e09e0-116">Requirement</span></span> | <span data-ttu-id="e09e0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e09e0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e09e0-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e09e0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e09e0-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e09e0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e09e0-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e09e0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e09e0-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e09e0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e09e0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e09e0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e09e0-123"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e09e0-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e09e0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e09e0-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="e09e0-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="e09e0-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e09e0-126">**$ \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="e09e0-126">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="e09e0-127">**\_GETITEMDATA CB**</span><span class="sxs-lookup"><span data-stu-id="e09e0-127">**CB\_GETITEMDATA**</span></span>](cb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="e09e0-128">**\_INSERTSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="e09e0-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





