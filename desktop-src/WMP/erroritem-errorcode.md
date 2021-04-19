---
title: ErrorItem. errorCode
description: La propriété errorCode récupère le code d’erreur actuel.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- ErrorItem. errorCode Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c934b83b28e510f29b84a45b48bde700968c97b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525139"
---
# <a name="erroritemerrorcode"></a><span data-ttu-id="0be86-104">ErrorItem. errorCode</span><span class="sxs-lookup"><span data-stu-id="0be86-104">ErrorItem.errorCode</span></span>

<span data-ttu-id="0be86-105">La propriété **ErrorCode** récupère le code d’erreur actuel.</span><span class="sxs-lookup"><span data-stu-id="0be86-105">The **errorCode** property retrieves the current error code.</span></span>

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a><span data-ttu-id="0be86-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="0be86-106">Possible Values</span></span>

<span data-ttu-id="0be86-107">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="0be86-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="0be86-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0be86-108">Remarks</span></span>

<span data-ttu-id="0be86-109">Vous devez définir des *paramètres*. **enableErrorDialogs** sur false si vous choisissez d’afficher des messages d’erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="0be86-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="0be86-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="0be86-110">Examples</span></span>

<span data-ttu-id="0be86-111">L’exemple JScript suivant utilise *ErrorItem*. **ErrorCode** dans un gestionnaire d’événements pour afficher le code d’erreur à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0be86-111">The following JScript example uses *ErrorItem*.**errorCode** in an event handler to display the error code to the user.</span></span> <span data-ttu-id="0be86-112">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="0be86-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="0be86-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0be86-113">Requirements</span></span>



| <span data-ttu-id="0be86-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0be86-114">Requirement</span></span> | <span data-ttu-id="0be86-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0be86-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0be86-116">Version</span><span class="sxs-lookup"><span data-stu-id="0be86-116">Version</span></span><br/> | <span data-ttu-id="0be86-117">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0be86-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0be86-118">DLL</span><span class="sxs-lookup"><span data-stu-id="0be86-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="0be86-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0be86-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0be86-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0be86-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be86-121">**Objet ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="0be86-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="0be86-122">**ErrorItem. errorDescription**</span><span class="sxs-lookup"><span data-stu-id="0be86-122">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> </dl>

 

 





