---
title: Player. PositionChange (événement)
description: L’événement PositionChange se produit lorsque la position actuelle de l’élément multimédia a été modifiée.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Événement PositionChange lecteur Windows Media
- Événement PositionChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement PositionChange
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526071"
---
# <a name="playerpositionchange-event"></a><span data-ttu-id="45ad5-106">Player. PositionChange (événement)</span><span class="sxs-lookup"><span data-stu-id="45ad5-106">Player.PositionChange event</span></span>

<span data-ttu-id="45ad5-107">L’événement **PositionChange** se produit lorsque la position actuelle de l’élément multimédia a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="45ad5-107">The **PositionChange** event occurs when the current position of the media item has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="45ad5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45ad5-108">Syntax</span></span>


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a><span data-ttu-id="45ad5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45ad5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45ad5-110">*oldPosition*</span><span class="sxs-lookup"><span data-stu-id="45ad5-110">*oldPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="45ad5-111">Nombre (**double**) spécifiant l’ancienne position.</span><span class="sxs-lookup"><span data-stu-id="45ad5-111">Number (**double**) specifying the old position.</span></span>

</dd> <dt>

<span data-ttu-id="45ad5-112">*newPosition*</span><span class="sxs-lookup"><span data-stu-id="45ad5-112">*newPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="45ad5-113">**Nombre** (**double**) spécifiant la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="45ad5-113">**Number** (**double**) specifying the new position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45ad5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45ad5-114">Return value</span></span>

<span data-ttu-id="45ad5-115">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="45ad5-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45ad5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="45ad5-116">Remarks</span></span>

<span data-ttu-id="45ad5-117">Cet événement n’est pas déclenché régulièrement pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="45ad5-117">This event is not raised routinely during playback.</span></span> <span data-ttu-id="45ad5-118">Il se produit uniquement quand un élément change activement la position actuelle de l’élément multimédia en cours d’exécution, par exemple l’utilisateur qui déplace la poignée de recherche ou le code en spécifiant une valeur pour les *contrôles*. **CurrentPosition**.</span><span class="sxs-lookup"><span data-stu-id="45ad5-118">It only occurs when something actively changes the current position of the playing media item, such as the user moving the seek handle or code specifying a value for *Controls*.**currentPosition**.</span></span>

<span data-ttu-id="45ad5-119">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="45ad5-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="45ad5-120">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="45ad5-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="45ad5-121">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="45ad5-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="45ad5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45ad5-122">Requirements</span></span>



| <span data-ttu-id="45ad5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45ad5-123">Requirement</span></span> | <span data-ttu-id="45ad5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="45ad5-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="45ad5-125">Version</span><span class="sxs-lookup"><span data-stu-id="45ad5-125">Version</span></span><br/> | <span data-ttu-id="45ad5-126">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="45ad5-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="45ad5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="45ad5-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="45ad5-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45ad5-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45ad5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45ad5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ad5-130">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="45ad5-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





