---
title: MediaCollection. getAll, méthode
description: La méthode getAll récupère une sélection contenant tous les éléments multimédias de la bibliothèque.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- méthode getAll lecteur Windows Media
- getAll, méthode lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, getAll, méthode
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1681cd533be4084123cb80cdcc199ab5e1ce2981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540568"
---
# <a name="mediacollectiongetall-method"></a><span data-ttu-id="68c2f-106">MediaCollection. getAll, méthode</span><span class="sxs-lookup"><span data-stu-id="68c2f-106">MediaCollection.getAll method</span></span>

<span data-ttu-id="68c2f-107">La méthode **GetAll** récupère une sélection contenant tous les éléments multimédias de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="68c2f-107">The **getAll** method retrieves a playlist containing all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="68c2f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68c2f-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a><span data-ttu-id="68c2f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68c2f-109">Parameters</span></span>

<span data-ttu-id="68c2f-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="68c2f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68c2f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68c2f-111">Return value</span></span>

<span data-ttu-id="68c2f-112">Cette méthode retourne un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="68c2f-112">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="68c2f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="68c2f-113">Remarks</span></span>

<span data-ttu-id="68c2f-114">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="68c2f-114">To use this method, read access to the library is required.</span></span> <span data-ttu-id="68c2f-115">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="68c2f-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="68c2f-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="68c2f-116">Examples</span></span>

<span data-ttu-id="68c2f-117">L’exemple JScript suivant utilise *MediaCollection*. **GetAll** pour lire des éléments multimédias de manière aléatoire à partir de la collection de médias.</span><span class="sxs-lookup"><span data-stu-id="68c2f-117">The following JScript example uses *MediaCollection*.**getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="68c2f-118">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="68c2f-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="68c2f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68c2f-119">Requirements</span></span>



| <span data-ttu-id="68c2f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68c2f-120">Requirement</span></span> | <span data-ttu-id="68c2f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="68c2f-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68c2f-122">Version</span><span class="sxs-lookup"><span data-stu-id="68c2f-122">Version</span></span><br/> | <span data-ttu-id="68c2f-123">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="68c2f-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="68c2f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="68c2f-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="68c2f-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68c2f-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68c2f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68c2f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c2f-127">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="68c2f-127">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="68c2f-128">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="68c2f-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="68c2f-129">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="68c2f-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="68c2f-130">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="68c2f-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





