---
title: Événement Player. Error
description: L’événement d’erreur se produit lorsqu’il y a une condition d’erreur.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Événement d’erreur lecteur Windows Media
- Événement d’erreur lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement d’erreur
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533109"
---
# <a name="playererror-event"></a><span data-ttu-id="c4990-106">Événement Player. Error</span><span class="sxs-lookup"><span data-stu-id="c4990-106">Player.Error event</span></span>

<span data-ttu-id="c4990-107">L’événement d' **erreur** se produit lorsqu’il y a une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c4990-107">The **Error** event occurs when there is an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4990-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4990-108">Syntax</span></span>


```JScript
Player.Error()
```



## <a name="parameters"></a><span data-ttu-id="c4990-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4990-109">Parameters</span></span>

<span data-ttu-id="c4990-110">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="c4990-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4990-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4990-111">Return value</span></span>

<span data-ttu-id="c4990-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c4990-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="c4990-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="c4990-113">Examples</span></span>

<span data-ttu-id="c4990-114">L’exemple JScript suivant crée un gestionnaire d’événements pour afficher le texte de description de la première erreur dans la file d’attente d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="c4990-114">The following JScript example creates an event handler to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="c4990-115">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c4990-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="c4990-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4990-116">Requirements</span></span>



| <span data-ttu-id="c4990-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4990-117">Requirement</span></span> | <span data-ttu-id="c4990-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4990-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c4990-119">Version</span><span class="sxs-lookup"><span data-stu-id="c4990-119">Version</span></span><br/> | <span data-ttu-id="c4990-120">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c4990-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c4990-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c4990-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="c4990-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4990-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4990-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4990-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4990-124">**ErrorItem. errorDescription**</span><span class="sxs-lookup"><span data-stu-id="c4990-124">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> <dt>

[<span data-ttu-id="c4990-125">**Erreur. élément**</span><span class="sxs-lookup"><span data-stu-id="c4990-125">**Error.item**</span></span>](error-item.md)
</dt> <dt>

[<span data-ttu-id="c4990-126">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="c4990-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





