---
title: Message WM_DELETEITEM (winuser. h)
description: Envoyé au propriétaire d’une zone de liste ou d’une zone de liste déroulante lorsque la zone de liste ou la zone de liste déroulante est détruite ou lorsque des éléments sont supprimés par le \_ message lb DELETESTRING, lb \_ RESETCONTENT, CB \_ DELETESTRING ou CB \_ RESETCONTENT.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- WM_DELETEITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465146"
---
# <a name="wm_deleteitem-message"></a><span data-ttu-id="7a29a-104">\_Message WM DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="7a29a-104">WM\_DELETEITEM message</span></span>

<span data-ttu-id="7a29a-105">Envoyé au propriétaire d’une zone de liste ou d’une zone de liste déroulante lorsque la zone de liste ou la zone de liste déroulante est détruite ou lorsque des éléments sont supprimés par le message [**lb \_ DELETESTRING**](lb-deletestring.md), [**lb \_ RESETCONTENT**](lb-resetcontent.md), [**CB \_ DELETESTRING**](cb-deletestring.md)ou [**CB \_ RESETCONTENT**](cb-resetcontent.md) .</span><span class="sxs-lookup"><span data-stu-id="7a29a-105">Sent to the owner of a list box or combo box when the list box or combo box is destroyed or when items are removed by the [**LB\_DELETESTRING**](lb-deletestring.md), [**LB\_RESETCONTENT**](lb-resetcontent.md), [**CB\_DELETESTRING**](cb-deletestring.md), or [**CB\_RESETCONTENT**](cb-resetcontent.md) message.</span></span> <span data-ttu-id="7a29a-106">Le système envoie un message **WM \_ DELETEITEM** pour chaque élément supprimé.</span><span class="sxs-lookup"><span data-stu-id="7a29a-106">The system sends a **WM\_DELETEITEM** message for each deleted item.</span></span> <span data-ttu-id="7a29a-107">Le système envoie le message **WM \_ DELETEITEM** pour tout élément de liste ou zone de liste déroulante supprimé avec des données d’élément non nulles.</span><span class="sxs-lookup"><span data-stu-id="7a29a-107">The system sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7a29a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a29a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a29a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a29a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a29a-110">Spécifie l’identificateur du contrôle qui a envoyé le message **WM \_ DELETEITEM** .</span><span class="sxs-lookup"><span data-stu-id="7a29a-110">Specifies the identifier of the control that sent the **WM\_DELETEITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="7a29a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a29a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a29a-112">Pointeur vers une structure [**deleteitemstruct,**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) qui contient des informations sur l’élément supprimé dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="7a29a-112">Pointer to a [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) structure that contains information about the item deleted from a list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a29a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a29a-113">Return value</span></span>

<span data-ttu-id="7a29a-114">Une application doit retourner la **valeur true** si elle traite ce message.</span><span class="sxs-lookup"><span data-stu-id="7a29a-114">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a29a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7a29a-115">Remarks</span></span>

<span data-ttu-id="7a29a-116">Microsoft Windows NT et versions ultérieures : Windows envoie un message **WM \_ DELETEITEM** uniquement pour les éléments supprimés d’une zone de liste owner-drawn (avec le style [**\_ OWNERDRAWFIXED**](list-box-styles.md) ou [**lbs \_ OWNERDRAWVARIABLE**](list-box-styles.md) ) ou la zone de liste déroulante owner-drawn (avec le style [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) ou [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="7a29a-116">Microsoft Windows NT and later: Windows sends a **WM\_DELETEITEM** message only for items deleted from an owner-drawn list box (with the [**LBS\_OWNERDRAWFIXED**](list-box-styles.md) or [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style) or owner-drawn combo box (with the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style).</span></span>

<span data-ttu-id="7a29a-117">Windows 95 : Windows envoie le message **WM \_ DELETEITEM** pour tout élément de liste ou zone de liste déroulante supprimé avec des données d’élément non nulles.</span><span class="sxs-lookup"><span data-stu-id="7a29a-117">Windows 95: Windows sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a29a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a29a-118">Requirements</span></span>



| <span data-ttu-id="7a29a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a29a-119">Requirement</span></span> | <span data-ttu-id="7a29a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a29a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a29a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a29a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7a29a-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a29a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7a29a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a29a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7a29a-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a29a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7a29a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a29a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a29a-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a29a-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a29a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a29a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="7a29a-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="7a29a-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7a29a-129">**\_DELETESTRING CB**</span><span class="sxs-lookup"><span data-stu-id="7a29a-129">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="7a29a-130">**\_RESETCONTENT CB**</span><span class="sxs-lookup"><span data-stu-id="7a29a-130">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="7a29a-131">**DELETEITEMSTRUCT,**</span><span class="sxs-lookup"><span data-stu-id="7a29a-131">**DELETEITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[<span data-ttu-id="7a29a-132">**\_DELETESTRING lb**</span><span class="sxs-lookup"><span data-stu-id="7a29a-132">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="7a29a-133">**\_RESETCONTENT lb**</span><span class="sxs-lookup"><span data-stu-id="7a29a-133">**LB\_RESETCONTENT**</span></span>](lb-resetcontent.md)
</dt> </dl>

 

 





