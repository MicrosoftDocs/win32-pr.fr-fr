---
title: Message LB_INITSTORAGE (winuser. h)
description: Alloue de la mémoire pour le stockage des éléments de zone de liste. Ce message est utilisé avant qu’une application ajoute un grand nombre d’éléments à une zone de liste.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- LB_INITSTORAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465374"
---
# <a name="lb_initstorage-message"></a><span data-ttu-id="34ea0-105">Message (LB) \_ INITSTORAGE</span><span class="sxs-lookup"><span data-stu-id="34ea0-105">LB\_INITSTORAGE message</span></span>

<span data-ttu-id="34ea0-106">Alloue de la mémoire pour le stockage des éléments de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="34ea0-106">Allocates memory for storing list box items.</span></span> <span data-ttu-id="34ea0-107">Ce message est utilisé avant qu’une application ajoute un grand nombre d’éléments à une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="34ea0-107">This message is used before an application adds a large number of items to a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="34ea0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34ea0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34ea0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34ea0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34ea0-110">Nombre d’éléments à ajouter.</span><span class="sxs-lookup"><span data-stu-id="34ea0-110">The number of items to add.</span></span>

<span data-ttu-id="34ea0-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : le paramètre *wParam* est limité aux valeurs 16 bits.</span><span class="sxs-lookup"><span data-stu-id="34ea0-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="34ea0-112">Cela signifie que les zones de liste ne peuvent pas contenir plus de 32 767 éléments.</span><span class="sxs-lookup"><span data-stu-id="34ea0-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="34ea0-113">Bien que le nombre d’éléments soit limité, la taille totale, en octets, des éléments d’une zone de liste n’est limitée que par la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="34ea0-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="34ea0-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34ea0-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34ea0-115">Quantité de mémoire, en octets, à allouer pour les chaînes d’élément.</span><span class="sxs-lookup"><span data-stu-id="34ea0-115">The amount of memory, in bytes, to allocate for item strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34ea0-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34ea0-116">Return value</span></span>

<span data-ttu-id="34ea0-117">Si le message est réussi, la valeur de retour est le nombre total d’éléments pour lesquels la mémoire a été allouée de façon préallouée, c’est-à-dire le nombre total d’éléments ajoutés par tous les messages de l' **équilibrage \_** de charge de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="34ea0-117">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **LB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="34ea0-118">Si le message échoue, la valeur de retour est LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="34ea0-118">If the message fails, the return value is LB\_ERRSPACE.</span></span>

<span data-ttu-id="34ea0-119">Microsoft Windows NT 4,0 : ce message n’alloue pas la quantité de mémoire spécifiée. Toutefois, elle retourne toujours la valeur spécifiée dans le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="34ea0-119">Microsoft Windows NT 4.0 : This message does not allocate the specified amount of memory; however, it always returns the value specified in the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="34ea0-120">Notes</span><span class="sxs-lookup"><span data-stu-id="34ea0-120">Remarks</span></span>

<span data-ttu-id="34ea0-121">Le message **lb \_ INITSTORAGE** permet d’accélérer l’initialisation des zones de liste qui comportent un grand nombre d’éléments (plus de 100).</span><span class="sxs-lookup"><span data-stu-id="34ea0-121">The **LB\_INITSTORAGE** message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="34ea0-122">Il réserve la quantité de mémoire spécifiée, de sorte que les messages [**lb \_ ADDSTRING**](lb-addstring.md), [**lb \_ INSERTSTRING**](lb-insertstring.md), [**lb \_ dir**](lb-dir.md)et [**\_ ADDFILE lb**](lb-addfile.md) peuvent durer le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="34ea0-122">It reserves the specified amount of memory so that subsequent [**LB\_ADDSTRING**](lb-addstring.md), [**LB\_INSERTSTRING**](lb-insertstring.md), [**LB\_DIR**](lb-dir.md), and [**LB\_ADDFILE**](lb-addfile.md) messages take the shortest possible time.</span></span> <span data-ttu-id="34ea0-123">Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* .</span><span class="sxs-lookup"><span data-stu-id="34ea0-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="34ea0-124">Si vous surestime, la mémoire supplémentaire est allouée. Si vous sous-estimez, l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.</span><span class="sxs-lookup"><span data-stu-id="34ea0-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="34ea0-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34ea0-125">Requirements</span></span>



| <span data-ttu-id="34ea0-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34ea0-126">Requirement</span></span> | <span data-ttu-id="34ea0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="34ea0-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34ea0-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34ea0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="34ea0-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34ea0-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="34ea0-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34ea0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="34ea0-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34ea0-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="34ea0-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="34ea0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="34ea0-133"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34ea0-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34ea0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34ea0-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="34ea0-135">**Référence**</span><span class="sxs-lookup"><span data-stu-id="34ea0-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="34ea0-136">**\_ADDFILE lb**</span><span class="sxs-lookup"><span data-stu-id="34ea0-136">**LB\_ADDFILE**</span></span>](lb-addfile.md)
</dt> <dt>

[<span data-ttu-id="34ea0-137">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="34ea0-137">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="34ea0-138">**direction \_ lb**</span><span class="sxs-lookup"><span data-stu-id="34ea0-138">**LB\_DIR**</span></span>](lb-dir.md)
</dt> <dt>

[<span data-ttu-id="34ea0-139">**\_INSERTSTRING lb**</span><span class="sxs-lookup"><span data-stu-id="34ea0-139">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





