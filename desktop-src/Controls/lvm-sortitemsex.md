---
title: Message LVM_SORTITEMSEX (commctrl. h)
description: Utilise une fonction de comparaison définie par l’application pour trier les éléments d’un contrôle List View. L’index de chaque élément change pour refléter la nouvelle séquence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SortItemsEx.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- LVM_SORTITEMSEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e524b00cb5ff1260eb68e7d86e185e5ae60c75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032427"
---
# <a name="lvm_sortitemsex-message"></a><span data-ttu-id="f5027-106">\_Message SORTITEMSEX LVM</span><span class="sxs-lookup"><span data-stu-id="f5027-106">LVM\_SORTITEMSEX message</span></span>

<span data-ttu-id="f5027-107">Utilise une fonction de comparaison définie par l’application pour trier les éléments d’un contrôle List View.</span><span class="sxs-lookup"><span data-stu-id="f5027-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="f5027-108">L’index de chaque élément change pour refléter la nouvelle séquence.</span><span class="sxs-lookup"><span data-stu-id="f5027-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="f5027-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SortItemsEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) .</span><span class="sxs-lookup"><span data-stu-id="f5027-109">You can send this message explicitly or by using the [**ListView\_SortItemsEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5027-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5027-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5027-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5027-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5027-112">Valeur définie par l’application qui est passée à la fonction de comparaison.</span><span class="sxs-lookup"><span data-stu-id="f5027-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="f5027-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5027-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5027-114">Pointeur vers une fonction de comparaison définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="f5027-114">Pointer to an application-defined comparison function.</span></span> <span data-ttu-id="f5027-115">Elle est appelée au cours de l’opération de tri chaque fois que l’ordre relatif de deux éléments de liste doit être comparé.</span><span class="sxs-lookup"><span data-stu-id="f5027-115">It is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5027-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5027-116">Return value</span></span>

<span data-ttu-id="f5027-117">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f5027-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5027-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f5027-118">Remarks</span></span>

<span data-ttu-id="f5027-119">La fonction de comparaison se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="f5027-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

<span data-ttu-id="f5027-120">Ce message est similaire à [**LVM \_ SORTITEMS**](lvm-sortitems.md), à l’exception du type d’informations passé à la fonction de comparaison.</span><span class="sxs-lookup"><span data-stu-id="f5027-120">This message is similar to [**LVM\_SORTITEMS**](lvm-sortitems.md), except for the type of information passed to the comparison function.</span></span> <span data-ttu-id="f5027-121">Avec **LVM \_ SORTITEMSEX**, *lParam1* est l’index actuel du premier élément, et *lParam2* est l’index actuel du deuxième élément.</span><span class="sxs-lookup"><span data-stu-id="f5027-121">With **LVM\_SORTITEMSEX**, *lParam1* is the current index of the first item, and *lParam2* is the current index of the second item.</span></span> <span data-ttu-id="f5027-122">Vous pouvez envoyer un [**message \_ GETITEMTEXT LVM**](lvm-getitemtext.md) pour récupérer plus d’informations sur un élément, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f5027-122">You can send an [**LVM\_GETITEMTEXT**](lvm-getitemtext.md) message to retrieve more information on an item, if needed.</span></span>

<span data-ttu-id="f5027-123">La fonction de comparaison doit retourner une valeur négative si le premier élément doit précéder le deuxième, une valeur positive si le premier élément doit suivre le deuxième, ou zéro si les deux éléments sont équivalents.</span><span class="sxs-lookup"><span data-stu-id="f5027-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="f5027-124">Durant le processus de tri, le contenu de l’affichage de liste est instable.</span><span class="sxs-lookup"><span data-stu-id="f5027-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="f5027-125">Si la fonction de rappel envoie des messages au contrôle List-View à part de [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="f5027-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5027-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5027-126">Requirements</span></span>



| <span data-ttu-id="f5027-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5027-127">Requirement</span></span> | <span data-ttu-id="f5027-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5027-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5027-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5027-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f5027-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5027-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5027-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5027-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f5027-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5027-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5027-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5027-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5027-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5027-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





