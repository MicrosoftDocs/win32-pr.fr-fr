---
title: Erreur. errorCount
description: La propriété errorCount récupère le nombre d’erreurs dans la file d’attente d’erreurs.
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- Erreur. errorCount Windows Media Player
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94848023d2cd331545f97d3bea6d92f2fcd4b49c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527991"
---
# <a name="errorerrorcount"></a><span data-ttu-id="b844f-104">Erreur. errorCount</span><span class="sxs-lookup"><span data-stu-id="b844f-104">Error.errorCount</span></span>

<span data-ttu-id="b844f-105">La propriété **errorCount** récupère le nombre d’erreurs dans la file d’attente d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="b844f-105">The **errorCount** property retrieves the number of errors in the error queue.</span></span>

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a><span data-ttu-id="b844f-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b844f-106">Possible Values</span></span>

<span data-ttu-id="b844f-107">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="b844f-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="b844f-108">Notes</span><span class="sxs-lookup"><span data-stu-id="b844f-108">Remarks</span></span>

<span data-ttu-id="b844f-109">Vous devez définir des *paramètres*. **enableErrorDialogs** sur false si vous choisissez d’afficher des messages d’erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="b844f-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="b844f-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="b844f-110">Examples</span></span>

<span data-ttu-id="b844f-111">L’exemple JScript suivant utilise une *erreur*. **errorCount** dans un gestionnaire d’événements pour avertir l’utilisateur de l’erreur la plus récente dans la file d’attente d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="b844f-111">The following JScript example uses *Error*.**errorCount** in an event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="b844f-112">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="b844f-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="b844f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b844f-113">Requirements</span></span>



| <span data-ttu-id="b844f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b844f-114">Requirement</span></span> | <span data-ttu-id="b844f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b844f-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b844f-116">Version</span><span class="sxs-lookup"><span data-stu-id="b844f-116">Version</span></span><br/> | <span data-ttu-id="b844f-117">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b844f-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b844f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="b844f-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="b844f-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b844f-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b844f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b844f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b844f-121">**Error, objet**</span><span class="sxs-lookup"><span data-stu-id="b844f-121">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





