---
title: MediaCollection. isDeleted, méthode
description: La méthode isDeleted récupère une valeur indiquant si l’élément multimédia spécifié se trouve dans le dossier éléments supprimés.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- isDeleted, méthode Windows Media Player
- isDeleted, méthode lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode isDeleted
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522794"
---
# <a name="mediacollectionisdeleted-method"></a><span data-ttu-id="5289c-106">MediaCollection. isDeleted, méthode</span><span class="sxs-lookup"><span data-stu-id="5289c-106">MediaCollection.isDeleted method</span></span>

<span data-ttu-id="5289c-107">La méthode **IsDeleted** récupère une valeur indiquant si l’élément multimédia spécifié se trouve dans le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="5289c-107">The **isDeleted** method retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="5289c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5289c-108">Syntax</span></span>


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="5289c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5289c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5289c-110">*élément* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5289c-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5289c-111">Objet **multimédia** qui peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="5289c-111">**Media** object that might be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5289c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5289c-112">Return value</span></span>

<span data-ttu-id="5289c-113">Cette méthode retourne une **valeur booléenne**.</span><span class="sxs-lookup"><span data-stu-id="5289c-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5289c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5289c-114">Remarks</span></span>

<span data-ttu-id="5289c-115">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="5289c-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5289c-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5289c-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="5289c-117">**Lecteur Windows Media 10 Mobile :** Cette méthode retourne toujours **false**.</span><span class="sxs-lookup"><span data-stu-id="5289c-117">**Windows Media Player 10 Mobile:** This method always returns **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="5289c-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="5289c-118">Examples</span></span>

<span data-ttu-id="5289c-119">L’exemple JScript suivant utilise *MediaCollection*. **IsDeleted** pour tester si un élément multimédia particulier, stocké dans la variable nommée mediaObject, se trouve dans le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="5289c-119">The following JScript example uses *MediaCollection*.**isDeleted** to test whether a particular media item, stored in the variable named mediaObject, is in the deleted items folder.</span></span> <span data-ttu-id="5289c-120">Si l’élément multimédia n’a pas déjà été supprimé, il est déplacé vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="5289c-120">If the media item has not been deleted already, it is moved to the deleted items folder.</span></span> <span data-ttu-id="5289c-121">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5289c-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="5289c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5289c-122">Requirements</span></span>



| <span data-ttu-id="5289c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5289c-123">Requirement</span></span> | <span data-ttu-id="5289c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5289c-124">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5289c-125">Version</span><span class="sxs-lookup"><span data-stu-id="5289c-125">Version</span></span><br/> | <span data-ttu-id="5289c-126">Lecteur Windows Media version 7,0, lecteur Windows Media version 7,1 ou lecteur Windows Media pour Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5289c-126">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="5289c-127">Cette méthode n’est pas prise en charge pour le lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5289c-127">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="5289c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5289c-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="5289c-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5289c-129"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="5289c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5289c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5289c-131">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="5289c-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="5289c-132">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="5289c-132">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="5289c-133">**MediaCollection.setDeleted**</span><span class="sxs-lookup"><span data-stu-id="5289c-133">**MediaCollection.setDeleted**</span></span>](mediacollection-setdeleted.md)
</dt> <dt>

[<span data-ttu-id="5289c-134">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5289c-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5289c-135">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5289c-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





