---
title: LISTBOX. popUp
description: L’attribut popUp spécifie une valeur indiquant si l’élément représente un contrôle Popup ou zone de liste.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- LISTBOX. popUp Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542566"
---
# <a name="listboxpopup"></a><span data-ttu-id="87a3f-104">LISTBOX. popUp</span><span class="sxs-lookup"><span data-stu-id="87a3f-104">LISTBOX.popUp</span></span>

<span data-ttu-id="87a3f-105">L’attribut **popUp** spécifie une valeur indiquant si l’élément représente un contrôle Popup ou zone de liste.</span><span class="sxs-lookup"><span data-stu-id="87a3f-105">The **popUp** attribute specifies a value indicating whether the element represents a popup or list box control.</span></span>

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a><span data-ttu-id="87a3f-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="87a3f-106">Possible Values</span></span>

<span data-ttu-id="87a3f-107">Cet attribut est une **valeur booléenne** spécifiée au moment de la conception uniquement.</span><span class="sxs-lookup"><span data-stu-id="87a3f-107">This attribute is a **Boolean** specified at design time only.</span></span>



| <span data-ttu-id="87a3f-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="87a3f-108">Value</span></span> | <span data-ttu-id="87a3f-109">Description</span><span class="sxs-lookup"><span data-stu-id="87a3f-109">Description</span></span>                                |
|-------|--------------------------------------------|
| <span data-ttu-id="87a3f-110">true</span><span class="sxs-lookup"><span data-stu-id="87a3f-110">true</span></span>  | <span data-ttu-id="87a3f-111">L’élément représente un contrôle Popup.</span><span class="sxs-lookup"><span data-stu-id="87a3f-111">The element represents a popup control.</span></span>    |
| <span data-ttu-id="87a3f-112">false</span><span class="sxs-lookup"><span data-stu-id="87a3f-112">false</span></span> | <span data-ttu-id="87a3f-113">L’élément représente un contrôle de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="87a3f-113">The element represents a list box control.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="87a3f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="87a3f-114">Remarks</span></span>

<span data-ttu-id="87a3f-115">L’élément **Popup** représente un contrôle de zone de liste qui s’affiche uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="87a3f-115">The **POPUP** element represents a list box control that is displayed only when needed.</span></span> <span data-ttu-id="87a3f-116">Elle est identique à l’élément **ListBox** , à l’exception de la valeur par défaut de cet attribut, qui modifie le comportement d’affichage.</span><span class="sxs-lookup"><span data-stu-id="87a3f-116">It is identical to the **LISTBOX** element except for the default value of this attribute, which changes the display behavior.</span></span> <span data-ttu-id="87a3f-117">Pour les éléments **ListBox** , la valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="87a3f-117">For **LISTBOX** elements, the default value is false.</span></span> <span data-ttu-id="87a3f-118">Pour les éléments **Popup** , la valeur par défaut est true.</span><span class="sxs-lookup"><span data-stu-id="87a3f-118">For **POPUP** elements, the default value is true.</span></span> <span data-ttu-id="87a3f-119">Au lieu de spécifier cet attribut, l’élément **ListBox** ou **Popup** doit être utilisé en fonction du comportement souhaité.</span><span class="sxs-lookup"><span data-stu-id="87a3f-119">Instead of specifying this attribute, the **LISTBOX** or **POPUP** element should be used to according to the desired behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="87a3f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87a3f-120">Requirements</span></span>



| <span data-ttu-id="87a3f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87a3f-121">Requirement</span></span> | <span data-ttu-id="87a3f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="87a3f-122">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="87a3f-123">Version</span><span class="sxs-lookup"><span data-stu-id="87a3f-123">Version</span></span><br/> | <span data-ttu-id="87a3f-124">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="87a3f-124">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87a3f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87a3f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87a3f-126">**Élément LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="87a3f-126">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="87a3f-127">**POPUP (élément)**</span><span class="sxs-lookup"><span data-stu-id="87a3f-127">**POPUP Element**</span></span>](popup-element.md)
</dt> </dl>

 

 





