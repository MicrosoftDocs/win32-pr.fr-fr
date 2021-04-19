---
title: Événement Player. MarkerHit
description: L’événement MarkerHit se produit lorsqu’un marqueur est atteint. | Événement Player. MarkerHit
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Événement MarkerHit lecteur Windows Media
- Événement MarkerHit lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MarkerHit
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532212"
---
# <a name="playermarkerhit-event"></a><span data-ttu-id="cddea-107">Événement Player. MarkerHit</span><span class="sxs-lookup"><span data-stu-id="cddea-107">Player.MarkerHit event</span></span>

<span data-ttu-id="cddea-108">L’événement **MarkerHit** se produit lorsqu’un marqueur est atteint.</span><span class="sxs-lookup"><span data-stu-id="cddea-108">The **MarkerHit** event occurs when a marker is reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="cddea-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cddea-109">Syntax</span></span>


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a><span data-ttu-id="cddea-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cddea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cddea-111">*MarkerNum*</span><span class="sxs-lookup"><span data-stu-id="cddea-111">*MarkerNum*</span></span> 
</dt> <dd>

<span data-ttu-id="cddea-112">**Nombre** (**long**) indiquant le numéro du marqueur qui a été atteint.</span><span class="sxs-lookup"><span data-stu-id="cddea-112">**Number** (**long**) indicating the number of the marker that was hit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cddea-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cddea-113">Return value</span></span>

<span data-ttu-id="cddea-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cddea-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cddea-115">Notes</span><span class="sxs-lookup"><span data-stu-id="cddea-115">Remarks</span></span>

<span data-ttu-id="cddea-116">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="cddea-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="cddea-117">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="cddea-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="cddea-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cddea-118">Requirements</span></span>



| <span data-ttu-id="cddea-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cddea-119">Requirement</span></span> | <span data-ttu-id="cddea-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cddea-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cddea-121">Version</span><span class="sxs-lookup"><span data-stu-id="cddea-121">Version</span></span><br/> | <span data-ttu-id="cddea-122">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="cddea-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cddea-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cddea-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="cddea-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cddea-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cddea-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cddea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cddea-126">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="cddea-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





