---
title: EDITBOX. replaceSelection
description: La méthode replaceSelection remplace la sélection actuelle par le texte spécifié.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- EDITBOX. replaceSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540363"
---
# <a name="editboxreplaceselection"></a><span data-ttu-id="00942-104">EDITBOX. replaceSelection</span><span class="sxs-lookup"><span data-stu-id="00942-104">EDITBOX.replaceSelection</span></span>

<span data-ttu-id="00942-105">La méthode **ReplaceSelection** remplace la sélection actuelle par le texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="00942-105">The **replaceSelection** method replaces the current selection with the specified text.</span></span>

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a><span data-ttu-id="00942-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00942-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00942-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span><span class="sxs-lookup"><span data-stu-id="00942-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span></span>
</dt> <dd>

<span data-ttu-id="00942-108">**Chaîne** contenant le texte pour remplacer le texte sélectionné.</span><span class="sxs-lookup"><span data-stu-id="00942-108">**String** containing the text to replace the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00942-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="00942-109">Return Value</span></span>

<span data-ttu-id="00942-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="00942-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00942-111">Notes</span><span class="sxs-lookup"><span data-stu-id="00942-111">Remarks</span></span>

<span data-ttu-id="00942-112">Si aucun texte n’est sélectionné, le texte de remplacement est inséré à l’emplacement actuel du point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="00942-112">If there is no text selected, the replacement text is inserted at the current location of the insertion point.</span></span>

<span data-ttu-id="00942-113">Cette méthode ne peut être appelée qu’une fois que le contrôle est visible.</span><span class="sxs-lookup"><span data-stu-id="00942-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="00942-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00942-114">Requirements</span></span>



| <span data-ttu-id="00942-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00942-115">Requirement</span></span> | <span data-ttu-id="00942-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="00942-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="00942-117">Version</span><span class="sxs-lookup"><span data-stu-id="00942-117">Version</span></span><br/> | <span data-ttu-id="00942-118">Lecteur Windows Media pour Windows XP ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="00942-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="00942-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00942-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00942-120">**Élément EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="00942-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="00942-121">**EDITBOX. getSelectionEnd**</span><span class="sxs-lookup"><span data-stu-id="00942-121">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="00942-122">**EDITBOX. getSelectionStart**</span><span class="sxs-lookup"><span data-stu-id="00942-122">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="00942-123">**EDITBOX. setSelection**</span><span class="sxs-lookup"><span data-stu-id="00942-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





