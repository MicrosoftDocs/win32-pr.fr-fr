---
title: Message LVM_SORTITEMS (commctrl. h)
description: Utilise une fonction de comparaison définie par l’application pour trier les éléments d’un contrôle List View. L’index de chaque élément change pour refléter la nouvelle séquence. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SortItems.
ms.assetid: ed3d5cec-69af-49a1-9cb7-eb5da1163071
keywords:
- LVM_SORTITEMS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SORTITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aba6e739a15eec5e951d7c3ead04aa36a8201f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942925"
---
# <a name="lvm_sortitems-message"></a><span data-ttu-id="5e859-106">\_Message SORTITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="5e859-106">LVM\_SORTITEMS message</span></span>

<span data-ttu-id="5e859-107">Utilise une fonction de comparaison définie par l’application pour trier les éléments d’un contrôle List View.</span><span class="sxs-lookup"><span data-stu-id="5e859-107">Uses an application-defined comparison function to sort the items of a list-view control.</span></span> <span data-ttu-id="5e859-108">L’index de chaque élément change pour refléter la nouvelle séquence.</span><span class="sxs-lookup"><span data-stu-id="5e859-108">The index of each item changes to reflect the new sequence.</span></span> <span data-ttu-id="5e859-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) .</span><span class="sxs-lookup"><span data-stu-id="5e859-109">You can send this message explicitly or by using the [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e859-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e859-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e859-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e859-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e859-112">Valeur définie par l’application qui est passée à la fonction de comparaison.</span><span class="sxs-lookup"><span data-stu-id="5e859-112">Application-defined value that is passed to the comparison function.</span></span>

</dd> <dt>

<span data-ttu-id="5e859-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e859-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e859-114">Pointeur vers la fonction de comparaison définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="5e859-114">Pointer to the application-defined comparison function.</span></span> <span data-ttu-id="5e859-115">La fonction de comparaison est appelée au cours de l’opération de tri chaque fois que l’ordre relatif de deux éléments de liste doit être comparé.</span><span class="sxs-lookup"><span data-stu-id="5e859-115">The comparison function is called during the sort operation each time the relative order of two list items needs to be compared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e859-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e859-116">Return value</span></span>

<span data-ttu-id="5e859-117">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5e859-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e859-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5e859-118">Remarks</span></span>

<span data-ttu-id="5e859-119">La fonction de comparaison se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="5e859-119">The comparison function has the following form:</span></span>

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);
```

<span data-ttu-id="5e859-120">Le paramètre *lParam1* est la valeur associée au premier élément comparé, tandis que le paramètre *lParam2* est la valeur associée au deuxième élément.</span><span class="sxs-lookup"><span data-stu-id="5e859-120">The *lParam1* parameter is the value associated with the first item being compared, and the *lParam2* parameter is the value associated with the second item.</span></span> <span data-ttu-id="5e859-121">Il s’agit des valeurs qui ont été spécifiées dans le membre **lParam** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) des éléments quand elles ont été insérées dans la liste.</span><span class="sxs-lookup"><span data-stu-id="5e859-121">These are the values that were specified in the **lParam** member of the items' [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure when they were inserted into the list.</span></span> <span data-ttu-id="5e859-122">Le paramètre *wParam* de [**ListView \_ SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)est passé à la fonction de rappel comme troisième paramètre.</span><span class="sxs-lookup"><span data-stu-id="5e859-122">The [**ListView\_SortItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitems)'s *wParam* parameter is passed to the callback function as its third parameter.</span></span>

<span data-ttu-id="5e859-123">La fonction de comparaison doit retourner une valeur négative si le premier élément doit précéder le deuxième, une valeur positive si le premier élément doit suivre le deuxième, ou zéro si les deux éléments sont équivalents.</span><span class="sxs-lookup"><span data-stu-id="5e859-123">The comparison function must return a negative value if the first item should precede the second, a positive value if the first item should follow the second, or zero if the two items are equivalent.</span></span>

> [!Note]  
> <span data-ttu-id="5e859-124">Durant le processus de tri, le contenu de l’affichage de liste est instable.</span><span class="sxs-lookup"><span data-stu-id="5e859-124">During the sorting process, the list-view contents are unstable.</span></span> <span data-ttu-id="5e859-125">Si la fonction de rappel envoie des messages au contrôle List-View à part de [**LVM \_ GetItem**](lvm-getitem.md) ([**ListView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="5e859-125">If the callback function sends any messages to the list-view control aside from [**LVM\_GETITEM**](lvm-getitem.md) ([**ListView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)), the results are unpredictable.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5e859-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e859-126">Requirements</span></span>



| <span data-ttu-id="5e859-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e859-127">Requirement</span></span> | <span data-ttu-id="5e859-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e859-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e859-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e859-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5e859-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e859-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e859-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e859-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5e859-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e859-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e859-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e859-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e859-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e859-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





