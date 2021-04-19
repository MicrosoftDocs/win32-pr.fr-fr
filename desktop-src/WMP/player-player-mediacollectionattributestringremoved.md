---
title: Événement Player. MediaCollectionAttributeStringRemoved
description: L’événement MediaCollectionAttributeStringRemoved se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque. | Événement Player. MediaCollectionAttributeStringRemoved
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Événement MediaCollectionAttributeStringRemoved lecteur Windows Media
- Événement MediaCollectionAttributeStringRemoved lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MediaCollectionAttributeStringRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b85dfd566c507f6ae5557134ac95544e42d688
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527979"
---
# <a name="playermediacollectionattributestringremoved-event"></a><span data-ttu-id="24a3c-107">Événement Player. MediaCollectionAttributeStringRemoved</span><span class="sxs-lookup"><span data-stu-id="24a3c-107">Player.MediaCollectionAttributeStringRemoved event</span></span>

<span data-ttu-id="24a3c-108">L’événement **MediaCollectionAttributeStringRemoved** se produit lorsqu’une valeur d’attribut est supprimée de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="24a3c-108">The **MediaCollectionAttributeStringRemoved** event occurs when an attribute value is removed from the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a3c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24a3c-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringRemoved(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="24a3c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24a3c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a3c-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="24a3c-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="24a3c-112">**Chaîne** spécifiant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="24a3c-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="24a3c-113">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="24a3c-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="24a3c-114">*bstrAttribVal*</span><span class="sxs-lookup"><span data-stu-id="24a3c-114">*bstrAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="24a3c-115">**Chaîne** spécifiant la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="24a3c-115">**String** specifying the value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a3c-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24a3c-116">Return value</span></span>

<span data-ttu-id="24a3c-117">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="24a3c-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a3c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="24a3c-118">Remarks</span></span>

<span data-ttu-id="24a3c-119">Lorsqu’un élément multimédia est supprimé de la bibliothèque, ses métadonnées sont supprimées de l’objet **MediaCollection** et cet événement est déclenché pour chaque attribut supprimé.</span><span class="sxs-lookup"><span data-stu-id="24a3c-119">When a media item is removed from the library, its metadata is removed from the **MediaCollection** object and this event is fired for each attribute removed.</span></span>

<span data-ttu-id="24a3c-120">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="24a3c-120">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="24a3c-121">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="24a3c-121">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="24a3c-122">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="24a3c-122">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a3c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24a3c-123">Requirements</span></span>



| <span data-ttu-id="24a3c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24a3c-124">Requirement</span></span> | <span data-ttu-id="24a3c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="24a3c-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24a3c-126">Version</span><span class="sxs-lookup"><span data-stu-id="24a3c-126">Version</span></span><br/> | <span data-ttu-id="24a3c-127">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="24a3c-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="24a3c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="24a3c-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="24a3c-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24a3c-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a3c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24a3c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a3c-131">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="24a3c-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="24a3c-132">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="24a3c-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="24a3c-133">**Player. mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="24a3c-133">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





