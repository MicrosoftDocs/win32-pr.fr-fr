---
title: ErrorItem. errorDescription
description: La propriété errorDescription récupère une description de l’erreur.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- Lecteur Windows Media ErrorItem. errorDescription
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0de19bb67a5846a82e87d091f95a18cd12c5c2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537329"
---
# <a name="erroritemerrordescription"></a><span data-ttu-id="761f2-104">ErrorItem. errorDescription</span><span class="sxs-lookup"><span data-stu-id="761f2-104">ErrorItem.errorDescription</span></span>

<span data-ttu-id="761f2-105">La propriété **errorDescription** récupère une description de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="761f2-105">The **errorDescription** property retrieves a description of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a><span data-ttu-id="761f2-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="761f2-106">Possible Values</span></span>

<span data-ttu-id="761f2-107">Cette propriété est une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="761f2-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="761f2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="761f2-108">Remarks</span></span>

<span data-ttu-id="761f2-109">Vous devez définir des *paramètres*. **enableErrorDialogs** sur false si vous choisissez d’afficher des messages d’erreur personnalisés.</span><span class="sxs-lookup"><span data-stu-id="761f2-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="761f2-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="761f2-110">Examples</span></span>

<span data-ttu-id="761f2-111">L’exemple JScript suivant utilise *ErrorItem*. **errorDescription** dans un gestionnaire d’événements pour afficher le message d’erreur à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="761f2-111">The following JScript example uses *ErrorItem*.**errorDescription** in an event handler to display the error message to the user.</span></span> <span data-ttu-id="761f2-112">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="761f2-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="761f2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="761f2-113">Requirements</span></span>



| <span data-ttu-id="761f2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="761f2-114">Requirement</span></span> | <span data-ttu-id="761f2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="761f2-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="761f2-116">Version</span><span class="sxs-lookup"><span data-stu-id="761f2-116">Version</span></span><br/> | <span data-ttu-id="761f2-117">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="761f2-117">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="761f2-118">DLL</span><span class="sxs-lookup"><span data-stu-id="761f2-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="761f2-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="761f2-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="761f2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="761f2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="761f2-121">**Objet ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="761f2-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





