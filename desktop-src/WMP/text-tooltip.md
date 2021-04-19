---
title: TEXT. toolTip
description: L’attribut toolTip spécifie ou récupère le texte d’info-bulle pour le contrôle Text.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- TEXT. toolTip lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545456"
---
# <a name="texttooltip"></a><span data-ttu-id="72523-104">TEXT. toolTip</span><span class="sxs-lookup"><span data-stu-id="72523-104">TEXT.toolTip</span></span>

<span data-ttu-id="72523-105">L’attribut **ToolTip** spécifie ou récupère le texte d’info-bulle pour le contrôle Text.</span><span class="sxs-lookup"><span data-stu-id="72523-105">The **toolTip** attribute specifies or retrieves the ToolTip text for the text control.</span></span>

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a><span data-ttu-id="72523-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="72523-106">Possible Values</span></span>

<span data-ttu-id="72523-107">Cet attribut est une **chaîne** en lecture/écriture d’une longueur maximale de 1024 caractères.</span><span class="sxs-lookup"><span data-stu-id="72523-107">This attribute is a read/write **String** with a maximum length of 1024 characters.</span></span> <span data-ttu-id="72523-108">Il n'a aucune valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="72523-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72523-109">Notes</span><span class="sxs-lookup"><span data-stu-id="72523-109">Remarks</span></span>

<span data-ttu-id="72523-110">Si cet attribut n’est pas spécifié et que le texte de l’attribut de **valeur** est tronqué dans le contrôle de texte, ou si **wordWrap** a la valeur true, l’info-bulle affiche le texte complet de l’attribut **value** .</span><span class="sxs-lookup"><span data-stu-id="72523-110">If this attribute is not specified, and the text in the **value** attribute is truncated in the Text control, or **wordWrap** is set to true, the ToolTip will display the full text of the **value** attribute.</span></span>

<span data-ttu-id="72523-111">Lorsque cet attribut a la valeur "" (chaîne vide), aucune info-bulle n’est affichée.</span><span class="sxs-lookup"><span data-stu-id="72523-111">When this attribute is set to "" (empty string), no ToolTip is displayed.</span></span>

<span data-ttu-id="72523-112">Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .</span><span class="sxs-lookup"><span data-stu-id="72523-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="72523-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72523-113">Requirements</span></span>



| <span data-ttu-id="72523-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72523-114">Requirement</span></span> | <span data-ttu-id="72523-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="72523-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="72523-116">Version</span><span class="sxs-lookup"><span data-stu-id="72523-116">Version</span></span><br/> | <span data-ttu-id="72523-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="72523-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72523-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72523-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72523-119">**Élément de texte**</span><span class="sxs-lookup"><span data-stu-id="72523-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="72523-120">**TEXT. Value**</span><span class="sxs-lookup"><span data-stu-id="72523-120">**TEXT.value**</span></span>](text-value.md)
</dt> <dt>

[<span data-ttu-id="72523-121">**TEXT. wordWrap**</span><span class="sxs-lookup"><span data-stu-id="72523-121">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





