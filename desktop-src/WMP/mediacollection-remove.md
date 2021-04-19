---
title: MediaCollection. Remove, méthode
description: La méthode Remove supprime un élément de la collection de supports.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- Méthode Remove Windows Media Player
- Remove, méthode lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode Remove
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523981"
---
# <a name="mediacollectionremove-method"></a><span data-ttu-id="75b1b-106">MediaCollection. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="75b1b-106">MediaCollection.remove method</span></span>

<span data-ttu-id="75b1b-107">La méthode **Remove** supprime un élément de la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="75b1b-107">The **remove** method removes an item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b1b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75b1b-108">Syntax</span></span>


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a><span data-ttu-id="75b1b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75b1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75b1b-110">*élément* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75b1b-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b1b-111">Objet **multimédia** à supprimer.</span><span class="sxs-lookup"><span data-stu-id="75b1b-111">**Media** object to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="75b1b-112">*supprimer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75b1b-112">*delete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75b1b-113">**Valeur booléenne** indiquant si l’élément doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="75b1b-113">**Boolean** indicating whether to remove the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75b1b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75b1b-114">Return value</span></span>

<span data-ttu-id="75b1b-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="75b1b-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75b1b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="75b1b-116">Remarks</span></span>

<span data-ttu-id="75b1b-117">Cette méthode supprime un élément de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="75b1b-117">This method deletes an item from the library.</span></span> <span data-ttu-id="75b1b-118">Cette méthode ne supprime pas les fichiers de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="75b1b-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="75b1b-119">Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="75b1b-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="75b1b-120">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="75b1b-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="75b1b-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="75b1b-121">Examples</span></span>

<span data-ttu-id="75b1b-122">L’exemple JScript suivant, après l’invite de l’utilisateur, supprime définitivement le premier élément multimédia de la collection de supports à l’aide de *MediaCollection*. **supprimez**.</span><span class="sxs-lookup"><span data-stu-id="75b1b-122">The following JScript example, after prompting the user, permanently deletes the first media item in the media collection by using *MediaCollection*.**remove**.</span></span> <span data-ttu-id="75b1b-123">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="75b1b-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

```



## <a name="requirements"></a><span data-ttu-id="75b1b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75b1b-124">Requirements</span></span>



| <span data-ttu-id="75b1b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75b1b-125">Requirement</span></span> | <span data-ttu-id="75b1b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="75b1b-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75b1b-127">Version</span><span class="sxs-lookup"><span data-stu-id="75b1b-127">Version</span></span><br/> | <span data-ttu-id="75b1b-128">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="75b1b-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="75b1b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="75b1b-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="75b1b-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75b1b-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75b1b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75b1b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b1b-132">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="75b1b-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="75b1b-133">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="75b1b-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="75b1b-134">**MediaCollection. Add**</span><span class="sxs-lookup"><span data-stu-id="75b1b-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="75b1b-135">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="75b1b-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="75b1b-136">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="75b1b-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





