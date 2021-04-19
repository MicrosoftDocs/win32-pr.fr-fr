---
title: EDITBOX. setSelection
description: La méthode setSelection sélectionne le texte dans le contrôle zone d’édition à partir de l’index de début spécifié jusqu’à l’index de fin spécifié.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- Windows Media Player. setSelection. setSelection
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532233"
---
# <a name="editboxsetselection"></a><span data-ttu-id="edcf6-104">EDITBOX. setSelection</span><span class="sxs-lookup"><span data-stu-id="edcf6-104">EDITBOX.setSelection</span></span>

<span data-ttu-id="edcf6-105">La méthode **SetSelection** sélectionne le texte dans le contrôle zone d’édition à partir de l’index de début spécifié jusqu’à l’index de fin spécifié.</span><span class="sxs-lookup"><span data-stu-id="edcf6-105">The **setSelection** method selects the text in the edit box control from the specified start index to the specified end index.</span></span>

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a><span data-ttu-id="edcf6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edcf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edcf6-107"><span id="start"></span><span id="START"></span>*activer*</span><span class="sxs-lookup"><span data-stu-id="edcf6-107"><span id="start"></span><span id="START"></span>*start*</span></span>
</dt> <dd>

<span data-ttu-id="edcf6-108">**Nombre** (**long**) contenant l’index de caractère de la position de départ du texte sélectionné.</span><span class="sxs-lookup"><span data-stu-id="edcf6-108">**Number** (**long**) containing the character index of the starting position of the selected text.</span></span>

</dd> <dt>

<span data-ttu-id="edcf6-109"><span id="end"></span><span id="END"></span>*effet*</span><span class="sxs-lookup"><span data-stu-id="edcf6-109"><span id="end"></span><span id="END"></span>*end*</span></span>
</dt> <dd>

<span data-ttu-id="edcf6-110">**Nombre** (**long**) contenant l’index de caractère de la position de fin du texte sélectionné.</span><span class="sxs-lookup"><span data-stu-id="edcf6-110">**Number** (**long**) containing the character index of the ending position of the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edcf6-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="edcf6-111">Return Value</span></span>

<span data-ttu-id="edcf6-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="edcf6-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="edcf6-113">Notes</span><span class="sxs-lookup"><span data-stu-id="edcf6-113">Remarks</span></span>

<span data-ttu-id="edcf6-114">Si le début est égal à 0 et que la fin est égale à 1, tout le texte du contrôle de zone d’édition est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="edcf6-114">If the start is 0 and the end is  1, all of the text in the edit box control is selected.</span></span> <span data-ttu-id="edcf6-115">Si le début est 1, toute sélection actuelle est désélectionnée.</span><span class="sxs-lookup"><span data-stu-id="edcf6-115">If the start is  1, any current selection is deselected.</span></span>

<span data-ttu-id="edcf6-116">Cette méthode ne peut être appelée qu’une fois que le contrôle est visible.</span><span class="sxs-lookup"><span data-stu-id="edcf6-116">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="edcf6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edcf6-117">Requirements</span></span>



| <span data-ttu-id="edcf6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edcf6-118">Requirement</span></span> | <span data-ttu-id="edcf6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="edcf6-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="edcf6-120">Version</span><span class="sxs-lookup"><span data-stu-id="edcf6-120">Version</span></span><br/> | <span data-ttu-id="edcf6-121">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="edcf6-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="edcf6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edcf6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edcf6-123">**Élément EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="edcf6-123">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="edcf6-124">**EDITBOX. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="edcf6-124">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="edcf6-125">**EDITBOX. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="edcf6-125">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="edcf6-126">**EDITBOX. replaceSelection**</span><span class="sxs-lookup"><span data-stu-id="edcf6-126">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> </dl>

 

 





