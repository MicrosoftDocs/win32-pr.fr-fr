---
title: Méthode MediaCollection. getByAuthor
description: La méthode getByAuthor récupère une sélection des éléments multimédias par l’auteur spécifié.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- méthode getByAuthor lecteur Windows Media
- méthode getByAuthor lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getByAuthor
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eae0928250e37e76bf3a39f38b43bef8a5691c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525342"
---
# <a name="mediacollectiongetbyauthor-method"></a><span data-ttu-id="a7154-106">Méthode MediaCollection. getByAuthor</span><span class="sxs-lookup"><span data-stu-id="a7154-106">MediaCollection.getByAuthor method</span></span>

<span data-ttu-id="a7154-107">La méthode **getByAuthor** récupère une sélection des éléments multimédias par l’auteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7154-107">The **getByAuthor** method retrieves a playlist of the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7154-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7154-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a><span data-ttu-id="a7154-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7154-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7154-110">*auteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a7154-110">*author* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7154-111">**Chaîne** contenant le nom de l’auteur.</span><span class="sxs-lookup"><span data-stu-id="a7154-111">**String** containing the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7154-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7154-112">Return value</span></span>

<span data-ttu-id="a7154-113">Cette méthode retourne un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="a7154-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7154-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a7154-114">Remarks</span></span>

<span data-ttu-id="a7154-115">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="a7154-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="a7154-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a7154-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a7154-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="a7154-117">Examples</span></span>

<span data-ttu-id="a7154-118">L’exemple JScript suivant utilise *MediaCollection*. **getByAuthor** pour récupérer une sélection d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="a7154-118">The following JScript example uses *MediaCollection*.**getByAuthor** to retrieve a playlist of media items.</span></span> <span data-ttu-id="a7154-119">La sélection contient des éléments correspondant à l’auteur spécifié par l’utilisateur dans un élément d’entrée de texte HTML nommé GetAuthor.</span><span class="sxs-lookup"><span data-stu-id="a7154-119">The playlist contains items matching the author specified by the user in an HTML TEXT input element named GetAuthor.</span></span> <span data-ttu-id="a7154-120">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a7154-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
               Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="a7154-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7154-121">Requirements</span></span>



| <span data-ttu-id="a7154-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7154-122">Requirement</span></span> | <span data-ttu-id="a7154-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7154-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a7154-124">Version</span><span class="sxs-lookup"><span data-stu-id="a7154-124">Version</span></span><br/> | <span data-ttu-id="a7154-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a7154-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a7154-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a7154-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="a7154-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7154-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7154-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7154-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7154-129">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="a7154-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="a7154-130">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="a7154-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="a7154-131">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a7154-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a7154-132">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a7154-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





