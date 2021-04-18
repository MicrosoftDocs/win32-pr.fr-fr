---
title: Error. clearErrorQueue, méthode
description: La méthode clearErrorQueue efface les erreurs de la file d’attente des erreurs. | Error. clearErrorQueue, méthode
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- méthode clearErrorQueue lecteur Windows Media
- méthode clearErrorQueue lecteur Windows Media, classe d’erreur
- Classe d’erreur lecteur Windows Media, méthode clearErrorQueue
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522795"
---
# <a name="errorclearerrorqueue-method"></a><span data-ttu-id="bfafe-107">Error. clearErrorQueue, méthode</span><span class="sxs-lookup"><span data-stu-id="bfafe-107">Error.clearErrorQueue method</span></span>

<span data-ttu-id="bfafe-108">La méthode **clearErrorQueue** efface les erreurs de la file d’attente des erreurs.</span><span class="sxs-lookup"><span data-stu-id="bfafe-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfafe-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfafe-109">Syntax</span></span>


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a><span data-ttu-id="bfafe-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfafe-110">Parameters</span></span>

<span data-ttu-id="bfafe-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bfafe-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bfafe-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfafe-112">Return value</span></span>

<span data-ttu-id="bfafe-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="bfafe-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfafe-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bfafe-114">Remarks</span></span>

<span data-ttu-id="bfafe-115">Cette méthode est utile pour effacer la file d’attente d’erreurs après le traitement d’une série d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="bfafe-115">This method is useful to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="bfafe-116">Vous devez définir des *paramètres*. **enableErrorDialogs** sur false si vous choisissez d’afficher des messages d’erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="bfafe-116">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="bfafe-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="bfafe-117">Examples</span></span>

<span data-ttu-id="bfafe-118">L’exemple JScript suivant utilise une *erreur*. **clearErrorQueue** dans un gestionnaire d’événements pour vider la file d’attente d’erreurs après l’affichage de toutes les descriptions d’erreur.</span><span class="sxs-lookup"><span data-stu-id="bfafe-118">The following JScript example uses *Error*.**clearErrorQueue** in an event handler to empty the error queue after all error descriptions are displayed.</span></span> <span data-ttu-id="bfafe-119">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="bfafe-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="bfafe-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfafe-120">Requirements</span></span>



| <span data-ttu-id="bfafe-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfafe-121">Requirement</span></span> | <span data-ttu-id="bfafe-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfafe-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bfafe-123">Version</span><span class="sxs-lookup"><span data-stu-id="bfafe-123">Version</span></span><br/> | <span data-ttu-id="bfafe-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bfafe-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bfafe-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bfafe-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="bfafe-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfafe-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfafe-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfafe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfafe-128">**Error, objet**</span><span class="sxs-lookup"><span data-stu-id="bfafe-128">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





