---
title: Méthode MediaCollection. setDeleted
description: La méthode setDeleted déplace l’élément multimédia spécifié vers le dossier éléments supprimés. | Méthode MediaCollection. setDeleted
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- méthode setDeleted lecteur Windows Media
- méthode setDeleted lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode setDeleted
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520885"
---
# <a name="mediacollectionsetdeleted-method"></a><span data-ttu-id="f136d-107">Méthode MediaCollection. setDeleted</span><span class="sxs-lookup"><span data-stu-id="f136d-107">MediaCollection.setDeleted method</span></span>

<span data-ttu-id="f136d-108">La méthode **setDeleted** déplace l’élément multimédia spécifié vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="f136d-108">The **setDeleted** method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="f136d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f136d-109">Syntax</span></span>


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a><span data-ttu-id="f136d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f136d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f136d-111">*élément* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f136d-111">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f136d-112">Objet **multimédia** déplacé.</span><span class="sxs-lookup"><span data-stu-id="f136d-112">**Media** object being moved.</span></span>

</dd> <dt>

<span data-ttu-id="f136d-113">*true* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f136d-113">*true* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f136d-114">Spécifiez toujours cette valeur.</span><span class="sxs-lookup"><span data-stu-id="f136d-114">Always specify this value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f136d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f136d-115">Return value</span></span>

<span data-ttu-id="f136d-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f136d-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f136d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f136d-117">Remarks</span></span>

<span data-ttu-id="f136d-118">Cette méthode ne supprime pas les fichiers de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f136d-118">This method does not remove files from the user's computer.</span></span>

<span data-ttu-id="f136d-119">Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="f136d-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="f136d-120">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f136d-120">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f136d-121">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f136d-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="f136d-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="f136d-122">Examples</span></span>

<span data-ttu-id="f136d-123">L’exemple JScript suivant utilise *MediaCollection*. **setDeleted** pour déplacer un élément multimédia particulier, stocké dans la variable nommée mediaObject, vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="f136d-123">The following JScript example uses *MediaCollection*.**setDeleted** to move a particular media item, stored in the variable named mediaObject, to the deleted items folder.</span></span> <span data-ttu-id="f136d-124">*MediaCollection*. méthode **IsDeleted** teste d’abord si l’élément a déjà été supprimé.</span><span class="sxs-lookup"><span data-stu-id="f136d-124">The *MediaCollection*.**isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="f136d-125">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f136d-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="f136d-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f136d-126">Requirements</span></span>



| <span data-ttu-id="f136d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f136d-127">Requirement</span></span> | <span data-ttu-id="f136d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f136d-128">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f136d-129">Version</span><span class="sxs-lookup"><span data-stu-id="f136d-129">Version</span></span><br/> | <span data-ttu-id="f136d-130">Lecteur Windows Media version 7,0, lecteur Windows Media version 7,1 ou lecteur Windows Media pour Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f136d-130">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="f136d-131">Cette méthode n’est pas prise en charge pour le lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f136d-131">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="f136d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f136d-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="f136d-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f136d-133"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="f136d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f136d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f136d-135">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="f136d-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f136d-136">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="f136d-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="f136d-137">**MediaCollection. isDeleted**</span><span class="sxs-lookup"><span data-stu-id="f136d-137">**MediaCollection.isDeleted**</span></span>](mediacollection-isdeleted.md)
</dt> <dt>

[<span data-ttu-id="f136d-138">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f136d-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f136d-139">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f136d-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





