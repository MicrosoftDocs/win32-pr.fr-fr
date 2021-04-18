---
title: CdromCollection. Count
description: La propriété Count récupère le nombre de lecteurs de CD et de DVD disponibles sur le système.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- CdromCollection. Count lecteur Windows Media
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526463"
---
# <a name="cdromcollectioncount"></a><span data-ttu-id="ecc2f-104">CdromCollection. Count</span><span class="sxs-lookup"><span data-stu-id="ecc2f-104">CdromCollection.count</span></span>

<span data-ttu-id="ecc2f-105">La propriété **Count** récupère le nombre de lecteurs de CD et de DVD disponibles sur le système.</span><span class="sxs-lookup"><span data-stu-id="ecc2f-105">The **count** property retrieves the number of available CD and DVD drives on the system.</span></span>

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a><span data-ttu-id="ecc2f-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="ecc2f-106">Possible Values</span></span>

<span data-ttu-id="ecc2f-107">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="ecc2f-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ecc2f-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ecc2f-108">Remarks</span></span>

<span data-ttu-id="ecc2f-109">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="ecc2f-109">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="ecc2f-110">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ecc2f-110">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ecc2f-111">Les lecteurs de DVD-ROM sont comptés exactement comme les lecteurs de CD.</span><span class="sxs-lookup"><span data-stu-id="ecc2f-111">DVD-ROM drives are counted exactly like CD drives.</span></span> <span data-ttu-id="ecc2f-112">Toutefois, le contrôle du lecteur Windows Media ne prend en charge que les fonctionnalités DVD pour Windows XP ou les systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="ecc2f-112">However, the Windows Media Player control only supports DVD functionality for Windows XP or later operating systems.</span></span> <span data-ttu-id="ecc2f-113">En règle générale, les lecteurs de DVD peuvent lire des CD, mais les lecteurs de CD ne peuvent pas lire les DVD.</span><span class="sxs-lookup"><span data-stu-id="ecc2f-113">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="ecc2f-114">**Lecteur Windows Media 10 Mobile :** Cette méthode retourne toujours 0.</span><span class="sxs-lookup"><span data-stu-id="ecc2f-114">**Windows Media Player 10 Mobile:** This method always returns 0.</span></span>

## <a name="examples"></a><span data-ttu-id="ecc2f-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="ecc2f-115">Examples</span></span>

<span data-ttu-id="ecc2f-116">L’exemple JScript suivant utilise *CdromCollection*. **nombre** pour afficher le nombre de lecteurs de CD et de DVD disponibles sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ecc2f-116">The following JScript example uses *CdromCollection*.**count** to display the number of CD and DVD drives available on the user's computer.</span></span> <span data-ttu-id="ecc2f-117">L’objet Player a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ecc2f-117">The player object was created with ID = "Player".</span></span>


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a><span data-ttu-id="ecc2f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecc2f-118">Requirements</span></span>



| <span data-ttu-id="ecc2f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecc2f-119">Requirement</span></span> | <span data-ttu-id="ecc2f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecc2f-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc2f-121">Version</span><span class="sxs-lookup"><span data-stu-id="ecc2f-121">Version</span></span><br/> | <span data-ttu-id="ecc2f-122">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="ecc2f-122">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="ecc2f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ecc2f-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ecc2f-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecc2f-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecc2f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecc2f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc2f-126">**Objet CdromCollection**</span><span class="sxs-lookup"><span data-stu-id="ecc2f-126">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="ecc2f-127">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ecc2f-127">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ecc2f-128">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ecc2f-128">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





