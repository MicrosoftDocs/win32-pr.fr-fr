---
title: Événement Player. MediaCollectionAttributeStringChanged
description: L’événement MediaCollectionAttributeStringChanged se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée. | Événement Player. MediaCollectionAttributeStringChanged
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Événement MediaCollectionAttributeStringChanged lecteur Windows Media
- Événement MediaCollectionAttributeStringChanged lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MediaCollectionAttributeStringChanged
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542279"
---
# <a name="playermediacollectionattributestringchanged-event"></a><span data-ttu-id="35fbf-107">Événement Player. MediaCollectionAttributeStringChanged</span><span class="sxs-lookup"><span data-stu-id="35fbf-107">Player.MediaCollectionAttributeStringChanged event</span></span>

<span data-ttu-id="35fbf-108">L’événement **MediaCollectionAttributeStringChanged** se produit lorsqu’une valeur d’attribut de la bibliothèque est modifiée.</span><span class="sxs-lookup"><span data-stu-id="35fbf-108">The **MediaCollectionAttributeStringChanged** event occurs when an attribute value in the library is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="35fbf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35fbf-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="35fbf-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35fbf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fbf-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="35fbf-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="35fbf-112">**Chaîne** spécifiant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="35fbf-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="35fbf-113">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="35fbf-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="35fbf-114">*bstrOldAttribVal*</span><span class="sxs-lookup"><span data-stu-id="35fbf-114">*bstrOldAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="35fbf-115">**Chaîne** spécifiant l’ancienne valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="35fbf-115">**String** specifying the old value of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="35fbf-116">*bstrNewAttribVal*</span><span class="sxs-lookup"><span data-stu-id="35fbf-116">*bstrNewAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="35fbf-117">**Chaîne** spécifiant la nouvelle valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="35fbf-117">**String** specifying the new value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fbf-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35fbf-118">Return value</span></span>

<span data-ttu-id="35fbf-119">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="35fbf-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35fbf-120">Notes</span><span class="sxs-lookup"><span data-stu-id="35fbf-120">Remarks</span></span>

<span data-ttu-id="35fbf-121">Quand un utilisateur modifie des métadonnées de bibliothèque, l’objet **MediaCollection** est mis à jour et cet événement se déclenche pour chaque attribut modifié.</span><span class="sxs-lookup"><span data-stu-id="35fbf-121">When a user modifies library metadata, the **MediaCollection** object is updated and this event fires for each attribute changed.</span></span>

<span data-ttu-id="35fbf-122">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="35fbf-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="35fbf-123">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="35fbf-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="35fbf-124">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="35fbf-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fbf-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35fbf-125">Requirements</span></span>



| <span data-ttu-id="35fbf-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35fbf-126">Requirement</span></span> | <span data-ttu-id="35fbf-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="35fbf-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35fbf-128">Version</span><span class="sxs-lookup"><span data-stu-id="35fbf-128">Version</span></span><br/> | <span data-ttu-id="35fbf-129">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="35fbf-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="35fbf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="35fbf-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="35fbf-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35fbf-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35fbf-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35fbf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fbf-133">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="35fbf-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="35fbf-134">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="35fbf-134">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="35fbf-135">**Player. mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="35fbf-135">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





