---
title: Événement Player. MediaError
description: L’événement MediaError se produit lorsque l’objet Media a une condition d’erreur.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Événement MediaError lecteur Windows Media
- Événement MediaError lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MediaError
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545555"
---
# <a name="playermediaerror-event"></a><span data-ttu-id="9a695-106">Événement Player. MediaError</span><span class="sxs-lookup"><span data-stu-id="9a695-106">Player.MediaError event</span></span>

<span data-ttu-id="9a695-107">L’événement **MediaError** se produit lorsque l’objet **Media** a une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9a695-107">The **MediaError** event occurs when the **Media** object has an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a695-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a695-108">Syntax</span></span>


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a><span data-ttu-id="9a695-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a695-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a695-110">*pMediaObject*</span><span class="sxs-lookup"><span data-stu-id="9a695-110">*pMediaObject*</span></span> 
</dt> <dd>

<span data-ttu-id="9a695-111">Objet **multimédia** qui a une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9a695-111">**Media** object that has an error condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a695-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a695-112">Return value</span></span>

<span data-ttu-id="9a695-113">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9a695-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a695-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9a695-114">Remarks</span></span>

<span data-ttu-id="9a695-115">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="9a695-115">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="9a695-116">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="9a695-116">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a695-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a695-117">Requirements</span></span>



| <span data-ttu-id="9a695-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a695-118">Requirement</span></span> | <span data-ttu-id="9a695-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a695-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a695-120">Version</span><span class="sxs-lookup"><span data-stu-id="9a695-120">Version</span></span><br/> | <span data-ttu-id="9a695-121">Lecteur Windows Media pour Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9a695-121">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="9a695-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9a695-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="9a695-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a695-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a695-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a695-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a695-125">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="9a695-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





