---
title: Événement Player. MediaCollectionAttributeStringAdded
description: L’événement MediaCollectionAttributeStringAdded se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque. | Événement Player. MediaCollectionAttributeStringAdded
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Événement MediaCollectionAttributeStringAdded lecteur Windows Media
- Événement MediaCollectionAttributeStringAdded lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MediaCollectionAttributeStringAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526626"
---
# <a name="playermediacollectionattributestringadded-event"></a><span data-ttu-id="e7d6a-107">Événement Player. MediaCollectionAttributeStringAdded</span><span class="sxs-lookup"><span data-stu-id="e7d6a-107">Player.MediaCollectionAttributeStringAdded event</span></span>

<span data-ttu-id="e7d6a-108">L’événement **MediaCollectionAttributeStringAdded** se produit lorsqu’une valeur d’attribut est ajoutée à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-108">The **MediaCollectionAttributeStringAdded** event occurs when an attribute value is added to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7d6a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7d6a-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringAdded(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="e7d6a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7d6a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7d6a-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="e7d6a-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="e7d6a-112">**Chaîne** spécifiant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="e7d6a-113">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7d6a-114">*bstrAttribVal*</span><span class="sxs-lookup"><span data-stu-id="e7d6a-114">*bstrAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="e7d6a-115">**Chaîne** spécifiant la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-115">**String** specifying the value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7d6a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7d6a-116">Return value</span></span>

<span data-ttu-id="e7d6a-117">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7d6a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e7d6a-118">Remarks</span></span>

<span data-ttu-id="e7d6a-119">Lorsqu’un élément multimédia est ajouté à la bibliothèque, ses métadonnées sont ajoutées à l’objet **MediaCollection** et cet événement est déclenché pour chaque attribut ajouté.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-119">When a media item is added to the library its metadata is added to the **MediaCollection** object and this event is fired for each attribute added.</span></span>

<span data-ttu-id="e7d6a-120">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-120">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="e7d6a-121">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-121">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="e7d6a-122">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-122">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7d6a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7d6a-123">Requirements</span></span>



| <span data-ttu-id="e7d6a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7d6a-124">Requirement</span></span> | <span data-ttu-id="e7d6a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7d6a-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7d6a-126">Version</span><span class="sxs-lookup"><span data-stu-id="e7d6a-126">Version</span></span><br/> | <span data-ttu-id="e7d6a-127">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e7d6a-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e7d6a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e7d6a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="e7d6a-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7d6a-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7d6a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7d6a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7d6a-131">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="e7d6a-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="e7d6a-132">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="e7d6a-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="e7d6a-133">**Player. mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="e7d6a-133">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





