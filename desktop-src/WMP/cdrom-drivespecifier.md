---
title: Cdrom. driveSpecifier
description: La propriété driveSpecifier récupère la lettre du lecteur de CD ou de DVD.
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- Lecteur Windows Media cdrom. driveSpecifier
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fef04f56de87bb6aeb4843e5aedb6e5ed74418a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508405"
---
# <a name="cdromdrivespecifier"></a><span data-ttu-id="57521-104">Cdrom. driveSpecifier</span><span class="sxs-lookup"><span data-stu-id="57521-104">Cdrom.driveSpecifier</span></span>

<span data-ttu-id="57521-105">La propriété **driveSpecifier** récupère la lettre du lecteur de CD ou de DVD.</span><span class="sxs-lookup"><span data-stu-id="57521-105">The **driveSpecifier** property retrieves the CD or DVD drive letter.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a><span data-ttu-id="57521-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="57521-106">Possible Values</span></span>

<span data-ttu-id="57521-107">Cette propriété est une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="57521-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="57521-108">Notes</span><span class="sxs-lookup"><span data-stu-id="57521-108">Remarks</span></span>

<span data-ttu-id="57521-109">En règle générale, les lecteurs de DVD peuvent lire des CD, mais les lecteurs de CD ne peuvent pas lire les DVD.</span><span class="sxs-lookup"><span data-stu-id="57521-109">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span> <span data-ttu-id="57521-110">Cette propriété récupère un spécificateur de lecteur pour un index de lecteur de base zéro dans la plage Récupérée à l’aide de *CdromCollection*. **nombre**.</span><span class="sxs-lookup"><span data-stu-id="57521-110">This property retrieves a drive specifier for a zero-based drive index within the range retrieved using *CdromCollection*.**count**.</span></span> <span data-ttu-id="57521-111">La valeur récupérée prend la forme *x*:, où *x* représente la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="57521-111">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="57521-112">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="57521-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="57521-113">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="57521-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="57521-114">**Lecteur Windows Media 10 Mobile :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="57521-114">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="57521-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="57521-115">Examples</span></span>

<span data-ttu-id="57521-116">L’exemple JScript suivant utilise *cdrom*. **driveSpecifier** pour remplir une zone de texte html nommée myText avec une liste séparée par des virgules des lecteurs CD et DVD disponibles.</span><span class="sxs-lookup"><span data-stu-id="57521-116">The following JScript example uses *Cdrom*.**driveSpecifier** to fill an HTML text area named myText with a comma-separated list of available CD and DVD drives.</span></span> <span data-ttu-id="57521-117">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="57521-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a><span data-ttu-id="57521-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57521-118">Requirements</span></span>



| <span data-ttu-id="57521-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57521-119">Requirement</span></span> | <span data-ttu-id="57521-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="57521-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="57521-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57521-121">Minimum supported client</span></span><br/> | <span data-ttu-id="57521-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57521-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57521-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57521-123">Minimum supported server</span></span><br/> | <span data-ttu-id="57521-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57521-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="57521-125">Version</span><span class="sxs-lookup"><span data-stu-id="57521-125">Version</span></span><br/>                  | <span data-ttu-id="57521-126">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="57521-126">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="57521-127">DLL</span><span class="sxs-lookup"><span data-stu-id="57521-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57521-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57521-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57521-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57521-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57521-130">**Objet cdrom**</span><span class="sxs-lookup"><span data-stu-id="57521-130">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="57521-131">**CdromCollection. Count**</span><span class="sxs-lookup"><span data-stu-id="57521-131">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="57521-132">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="57521-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="57521-133">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="57521-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





