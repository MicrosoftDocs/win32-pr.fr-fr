---
title: EDITBOX. getSelectionStart
description: La méthode getSelectionStart récupère la position de départ du texte sélectionné dans le contrôle EditBox.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- EDITBOX. getSelectionStart Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2508119e5b1d46d09b3531582e86caad7e7facbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534928"
---
# <a name="editboxgetselectionstart"></a><span data-ttu-id="e170c-104">EDITBOX. getSelectionStart</span><span class="sxs-lookup"><span data-stu-id="e170c-104">EDITBOX.getSelectionStart</span></span>

<span data-ttu-id="e170c-105">La méthode **getSelectionStart** récupère la position de départ du texte sélectionné dans le contrôle EditBox.</span><span class="sxs-lookup"><span data-stu-id="e170c-105">The **getSelectionStart** method retrieves the starting position of the selected text in the editbox control.</span></span>

``` syntax
        elementID.getSelectionStart()
```

## <a name="parameters"></a><span data-ttu-id="e170c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e170c-106">Parameters</span></span>

<span data-ttu-id="e170c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e170c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e170c-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e170c-108">Return Value</span></span>

<span data-ttu-id="e170c-109">Cette méthode retourne un **nombre** (**long**).</span><span class="sxs-lookup"><span data-stu-id="e170c-109">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e170c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e170c-110">Remarks</span></span>

<span data-ttu-id="e170c-111">Si aucun texte n’est sélectionné, cette méthode retourne la position du point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="e170c-111">If no text is selected, this method returns the position of the insertion point.</span></span>

<span data-ttu-id="e170c-112">Si le contrôle est multiligne, cette méthode retourne l’index de caractère dans le contrôle, et non l’index de ligne.</span><span class="sxs-lookup"><span data-stu-id="e170c-112">If the control is multiline, this method returns the character index in the control, not the line index.</span></span>

<span data-ttu-id="e170c-113">Cette méthode ne peut être appelée qu’une fois que le contrôle est visible.</span><span class="sxs-lookup"><span data-stu-id="e170c-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="e170c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e170c-114">Requirements</span></span>



| <span data-ttu-id="e170c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e170c-115">Requirement</span></span> | <span data-ttu-id="e170c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e170c-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="e170c-117">Version</span><span class="sxs-lookup"><span data-stu-id="e170c-117">Version</span></span><br/> | <span data-ttu-id="e170c-118">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e170c-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e170c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e170c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e170c-120">**Élément EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="e170c-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="e170c-121">**EDITBOX. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="e170c-121">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="e170c-122">**EDITBOX. replaceSelection**</span><span class="sxs-lookup"><span data-stu-id="e170c-122">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> <dt>

[<span data-ttu-id="e170c-123">**EDITBOX. setSelection**</span><span class="sxs-lookup"><span data-stu-id="e170c-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





