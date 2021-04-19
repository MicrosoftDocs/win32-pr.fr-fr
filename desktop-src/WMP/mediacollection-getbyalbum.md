---
title: Méthode MediaCollection. getByAlbum
description: La méthode GetByAlbum récupère une sélection contenant les éléments multimédias de l’album spécifié.
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- méthode getByAlbum lecteur Windows Media
- méthode getByAlbum lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getByAlbum
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d94cdfa880288893e9659b73b01bc754ac59bbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543249"
---
# <a name="mediacollectiongetbyalbum-method"></a><span data-ttu-id="c0e02-106">Méthode MediaCollection. getByAlbum</span><span class="sxs-lookup"><span data-stu-id="c0e02-106">MediaCollection.getByAlbum method</span></span>

<span data-ttu-id="c0e02-107">La méthode **GetByAlbum** récupère une sélection contenant les éléments multimédias de l’album spécifié.</span><span class="sxs-lookup"><span data-stu-id="c0e02-107">The **GetByAlbum** method retrieves a playlist containing the media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0e02-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0e02-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a><span data-ttu-id="c0e02-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0e02-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0e02-110">*album* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c0e02-110">*album* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0e02-111">**Chaîne** contenant le nom de l’album.</span><span class="sxs-lookup"><span data-stu-id="c0e02-111">**String** containing the name of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0e02-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0e02-112">Return value</span></span>

<span data-ttu-id="c0e02-113">Cette méthode retourne un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="c0e02-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0e02-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c0e02-114">Remarks</span></span>

<span data-ttu-id="c0e02-115">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="c0e02-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="c0e02-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c0e02-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c0e02-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="c0e02-117">Examples</span></span>

<span data-ttu-id="c0e02-118">L’exemple suivant utilise *MediaCollection*. **getByAlbum** pour récupérer une sélection d’éléments multimédias.</span><span class="sxs-lookup"><span data-stu-id="c0e02-118">The following example uses *MediaCollection*.**getByAlbum** to retrieve a playlist of media items.</span></span> <span data-ttu-id="c0e02-119">La sélection contient des éléments avec l’album spécifié par l’utilisateur dans un élément d’entrée de texte HTML nommé GetAlbum.</span><span class="sxs-lookup"><span data-stu-id="c0e02-119">The playlist contains items with the album specified by the user in an HTML TEXT input element named GetAlbum.</span></span> <span data-ttu-id="c0e02-120">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c0e02-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="c0e02-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0e02-121">Requirements</span></span>



| <span data-ttu-id="c0e02-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0e02-122">Requirement</span></span> | <span data-ttu-id="c0e02-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0e02-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e02-124">Version</span><span class="sxs-lookup"><span data-stu-id="c0e02-124">Version</span></span><br/> | <span data-ttu-id="c0e02-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c0e02-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c0e02-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c0e02-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="c0e02-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0e02-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0e02-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0e02-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0e02-129">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="c0e02-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="c0e02-130">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="c0e02-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="c0e02-131">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c0e02-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c0e02-132">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c0e02-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





