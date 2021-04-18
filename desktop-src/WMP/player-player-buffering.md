---
title: Player. Buffering (événement)
description: L’événement de mise en mémoire tampon se produit lorsque le contrôle du lecteur Windows Media démarre ou termine la mise en mémoire tampon ou le téléchargement. | Player. Buffering (événement)
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Mise en mémoire tampon des événements Windows Media Player
- Événement de mise en mémoire tampon Windows Media Player, classe Player
- Classe de lecteur Windows Media Player, événement de mise en mémoire tampon
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526049"
---
# <a name="playerbuffering-event"></a><span data-ttu-id="91c0d-107">Player. Buffering (événement)</span><span class="sxs-lookup"><span data-stu-id="91c0d-107">Player.Buffering event</span></span>

<span data-ttu-id="91c0d-108">L’événement de **mise en mémoire tampon** se produit lorsque le contrôle du lecteur Windows Media démarre ou termine la mise en mémoire tampon ou le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="91c0d-108">The **Buffering** event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c0d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91c0d-109">Syntax</span></span>


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a><span data-ttu-id="91c0d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91c0d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c0d-111">*Start*</span><span class="sxs-lookup"><span data-stu-id="91c0d-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="91c0d-112">**Valeur booléenne** contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="91c0d-112">**Boolean** containing one of the following values.</span></span>



| <span data-ttu-id="91c0d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="91c0d-113">Value</span></span> | <span data-ttu-id="91c0d-114">Description</span><span class="sxs-lookup"><span data-stu-id="91c0d-114">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="91c0d-115">true</span><span class="sxs-lookup"><span data-stu-id="91c0d-115">true</span></span>  | <span data-ttu-id="91c0d-116">La mise en mémoire tampon a démarré.</span><span class="sxs-lookup"><span data-stu-id="91c0d-116">Buffering has started.</span></span> |
| <span data-ttu-id="91c0d-117">false</span><span class="sxs-lookup"><span data-stu-id="91c0d-117">false</span></span> | <span data-ttu-id="91c0d-118">La mise en mémoire tampon s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="91c0d-118">Buffering has ended.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91c0d-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91c0d-119">Return value</span></span>

<span data-ttu-id="91c0d-120">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="91c0d-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91c0d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="91c0d-121">Remarks</span></span>

<span data-ttu-id="91c0d-122">Utilisez cet événement pour déterminer quand la mise en mémoire tampon ou le téléchargement démarre ou s’arrête.</span><span class="sxs-lookup"><span data-stu-id="91c0d-122">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="91c0d-123">Vous pouvez utiliser le même bloc d’événements pour les cas et le *réseau* de test. **bufferingProgress** et *réseau*. **downloadProgress** pour déterminer si le lecteur Windows Media met actuellement en mémoire tampon ou télécharge le contenu.</span><span class="sxs-lookup"><span data-stu-id="91c0d-123">You can use the same event block for both cases and test *Network*.**bufferingProgress** and *Network*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

<span data-ttu-id="91c0d-124">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé en utilisant le nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="91c0d-124">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file by using the parameter name given.</span></span> <span data-ttu-id="91c0d-125">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="91c0d-125">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="91c0d-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91c0d-126">Requirements</span></span>



| <span data-ttu-id="91c0d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91c0d-127">Requirement</span></span> | <span data-ttu-id="91c0d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="91c0d-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91c0d-129">Version</span><span class="sxs-lookup"><span data-stu-id="91c0d-129">Version</span></span><br/> | <span data-ttu-id="91c0d-130">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="91c0d-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="91c0d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="91c0d-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="91c0d-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91c0d-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91c0d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91c0d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c0d-134">**Network. bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="91c0d-134">**Network.bufferingProgress**</span></span>](network-bufferingprogress.md)
</dt> <dt>

[<span data-ttu-id="91c0d-135">**Network. downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="91c0d-135">**Network.downloadProgress**</span></span>](network-downloadprogress.md)
</dt> <dt>

[<span data-ttu-id="91c0d-136">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="91c0d-136">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





