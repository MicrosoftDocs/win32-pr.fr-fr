---
title: Méthode MediaCollection. getByAttribute
description: La méthode getByAttribute récupère une sélection d’éléments multimédias qui contiennent une valeur spécifiée pour un attribut spécifié.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- méthode getByAttribute lecteur Windows Media
- méthode getByAttribute lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getByAttribute
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533823127364416f8f4492c82381e682173c5c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542658"
---
# <a name="mediacollectiongetbyattribute-method"></a><span data-ttu-id="d5974-106">Méthode MediaCollection. getByAttribute</span><span class="sxs-lookup"><span data-stu-id="d5974-106">MediaCollection.getByAttribute method</span></span>

<span data-ttu-id="d5974-107">La méthode **getByAttribute** récupère une sélection d’éléments multimédias qui contiennent une valeur spécifiée pour un attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="d5974-107">The **getByAttribute** method retrieves a playlist of media items that contain a specified value for a specified attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5974-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5974-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="d5974-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5974-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5974-110">*attribut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5974-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5974-111">**Chaîne** indiquant le nom de l’attribut à rechercher.</span><span class="sxs-lookup"><span data-stu-id="d5974-111">**String** indicating the name of the attribute to search.</span></span> <span data-ttu-id="d5974-112">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d5974-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5974-113">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5974-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5974-114">**Chaîne** indiquant la valeur que l’attribut doit avoir.</span><span class="sxs-lookup"><span data-stu-id="d5974-114">**String** indicating the value that the attribute should have.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5974-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5974-115">Return value</span></span>

<span data-ttu-id="d5974-116">Cette méthode retourne un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="d5974-116">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5974-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d5974-117">Remarks</span></span>

<span data-ttu-id="d5974-118">Cette méthode peut être utilisée pour créer une requête générique pour les éléments multimédias qui correspondent à une valeur pour un attribut de la base de données.</span><span class="sxs-lookup"><span data-stu-id="d5974-118">This method can be used to create a generic query for media items that match a value for an attribute in the database.</span></span> <span data-ttu-id="d5974-119">Cela est utile dans le cas des attributs définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5974-119">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="d5974-120">Si l’attribut n’existe pas, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="d5974-120">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="d5974-121">Vous pouvez utiliser cette méthode pour récupérer tous les éléments multimédias d’un type spécifique.</span><span class="sxs-lookup"><span data-stu-id="d5974-121">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="d5974-122">Utilisez le nom d’attribut « MediaType » et l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5974-122">Use the attribute name "MediaType" and one of the following values:</span></span>



| <span data-ttu-id="d5974-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5974-123">Value</span></span>    | <span data-ttu-id="d5974-124">Description</span><span class="sxs-lookup"><span data-stu-id="d5974-124">Description</span></span>                                                |
|----------|------------------------------------------------------------|
| <span data-ttu-id="d5974-125">audio</span><span class="sxs-lookup"><span data-stu-id="d5974-125">audio</span></span>    | <span data-ttu-id="d5974-126">Musique et autres éléments audio uniquement.</span><span class="sxs-lookup"><span data-stu-id="d5974-126">Music and other audio-only items.</span></span>                          |
| <span data-ttu-id="d5974-127">playlist</span><span class="sxs-lookup"><span data-stu-id="d5974-127">playlist</span></span> | <span data-ttu-id="d5974-128">Sélections représentées en tant qu’objets **multimédias** .</span><span class="sxs-lookup"><span data-stu-id="d5974-128">Playlists represented as **Media** objects.</span></span>                |
| <span data-ttu-id="d5974-129">radio</span><span class="sxs-lookup"><span data-stu-id="d5974-129">radio</span></span>    | <span data-ttu-id="d5974-130">Éléments de station de radio.</span><span class="sxs-lookup"><span data-stu-id="d5974-130">Radio station items.</span></span> <span data-ttu-id="d5974-131">Non utilisé par le lecteur Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="d5974-131">Not used by Windows Media Player 10.</span></span>  |
| <span data-ttu-id="d5974-132">video</span><span class="sxs-lookup"><span data-stu-id="d5974-132">video</span></span>    | <span data-ttu-id="d5974-133">Éléments vidéo.</span><span class="sxs-lookup"><span data-stu-id="d5974-133">Video items.</span></span>                                               |
| <span data-ttu-id="d5974-134">photos</span><span class="sxs-lookup"><span data-stu-id="d5974-134">photo</span></span>    | <span data-ttu-id="d5974-135">Éléments de photo.</span><span class="sxs-lookup"><span data-stu-id="d5974-135">Photo items.</span></span> <span data-ttu-id="d5974-136">Requiert le lecteur Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="d5974-136">Requires Windows Media Player 10.</span></span>             |
| <span data-ttu-id="d5974-137">autre</span><span class="sxs-lookup"><span data-stu-id="d5974-137">other</span></span>    | <span data-ttu-id="d5974-138">Autres éléments, tels que les fichiers ASF ou les URL, pour la diffusion multimédia en continu.</span><span class="sxs-lookup"><span data-stu-id="d5974-138">Other items, such as ASF files or URLs to streaming media.</span></span> |



 

<span data-ttu-id="d5974-139">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="d5974-139">To use this method, read access to the library is required.</span></span> <span data-ttu-id="d5974-140">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d5974-140">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d5974-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="d5974-141">Examples</span></span>

<span data-ttu-id="d5974-142">L’exemple JScript suivant utilise *MediaCollection*. **getByAttribute** pour lire tout le contenu de la bibliothèque par l’artiste nommé triode 48.</span><span class="sxs-lookup"><span data-stu-id="d5974-142">The following JScript example uses *MediaCollection*.**getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="d5974-143">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d5974-143">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="d5974-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5974-144">Requirements</span></span>



| <span data-ttu-id="d5974-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5974-145">Requirement</span></span> | <span data-ttu-id="d5974-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5974-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5974-147">Version</span><span class="sxs-lookup"><span data-stu-id="d5974-147">Version</span></span><br/> | <span data-ttu-id="d5974-148">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d5974-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d5974-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d5974-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="d5974-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5974-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5974-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5974-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5974-152">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="d5974-152">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="d5974-153">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="d5974-153">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="d5974-154">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d5974-154">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="d5974-155">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d5974-155">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





