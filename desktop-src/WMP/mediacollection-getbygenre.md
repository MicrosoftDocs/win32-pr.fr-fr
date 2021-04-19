---
title: Méthode MediaCollection. getByGenre
description: La méthode getByGenre récupère une sélection des éléments multimédias avec le genre spécifié.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- méthode getByGenre lecteur Windows Media
- méthode getByGenre lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getByGenre
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537467"
---
# <a name="mediacollectiongetbygenre-method"></a><span data-ttu-id="de3ba-106">Méthode MediaCollection. getByGenre</span><span class="sxs-lookup"><span data-stu-id="de3ba-106">MediaCollection.getByGenre method</span></span>

<span data-ttu-id="de3ba-107">La méthode **getByGenre** récupère une sélection des éléments multimédias avec le genre spécifié.</span><span class="sxs-lookup"><span data-stu-id="de3ba-107">The **getByGenre** method retrieves a playlist of the media items with the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="de3ba-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de3ba-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a><span data-ttu-id="de3ba-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de3ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3ba-110">*genre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de3ba-110">*genre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de3ba-111">**Chaîne** contenant le nom du genre.</span><span class="sxs-lookup"><span data-stu-id="de3ba-111">**String** containing the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de3ba-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de3ba-112">Return value</span></span>

<span data-ttu-id="de3ba-113">Cette méthode retourne un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="de3ba-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="de3ba-114">Notes</span><span class="sxs-lookup"><span data-stu-id="de3ba-114">Remarks</span></span>

<span data-ttu-id="de3ba-115">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="de3ba-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="de3ba-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="de3ba-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="de3ba-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="de3ba-117">Examples</span></span>

<span data-ttu-id="de3ba-118">L’exemple JScript suivant utilise *MediaCollection*. **getByGenre** pour récupérer une sélection d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="de3ba-118">The following JScript example uses *MediaCollection*.**getByGenre** to retrieve a playlist of media items.</span></span> <span data-ttu-id="de3ba-119">La sélection contient des éléments dont le genre est spécifié par l’utilisateur dans un élément d’entrée de texte HTML nommé GetGenre.</span><span class="sxs-lookup"><span data-stu-id="de3ba-119">The playlist contains items with the genre specified by the user in an HTML TEXT input element named GetGenre.</span></span> <span data-ttu-id="de3ba-120">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="de3ba-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="de3ba-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de3ba-121">Requirements</span></span>



| <span data-ttu-id="de3ba-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de3ba-122">Requirement</span></span> | <span data-ttu-id="de3ba-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="de3ba-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de3ba-124">Version</span><span class="sxs-lookup"><span data-stu-id="de3ba-124">Version</span></span><br/> | <span data-ttu-id="de3ba-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="de3ba-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="de3ba-126">DLL</span><span class="sxs-lookup"><span data-stu-id="de3ba-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="de3ba-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de3ba-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de3ba-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de3ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3ba-129">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="de3ba-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="de3ba-130">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="de3ba-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="de3ba-131">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="de3ba-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="de3ba-132">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="de3ba-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





