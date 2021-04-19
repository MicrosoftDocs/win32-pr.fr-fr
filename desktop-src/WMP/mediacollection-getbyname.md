---
title: Méthode MediaCollection. getByName
description: La méthode getByName récupère une sélection des éléments multimédias portant le nom spécifié.
ms.assetid: f9395a4f-06d6-438b-b7c5-7a063abdf59f
keywords:
- méthode getByName lecteur Windows Media
- méthode getByName lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getByName
topic_type:
- apiref
api_name:
- MediaCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a3fc6e34b508fa094f79d2fbbd1d44ab712789
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541327"
---
# <a name="mediacollectiongetbyname-method"></a><span data-ttu-id="34cf0-106">Méthode MediaCollection. getByName</span><span class="sxs-lookup"><span data-stu-id="34cf0-106">MediaCollection.getByName method</span></span>

<span data-ttu-id="34cf0-107">La méthode **GetByName** récupère une sélection des éléments multimédias portant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="34cf0-107">The **getByName** method retrieves a playlist of the media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="34cf0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34cf0-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="34cf0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34cf0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34cf0-110">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34cf0-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34cf0-111">**Chaîne** contenant le nom.</span><span class="sxs-lookup"><span data-stu-id="34cf0-111">**String** containing the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34cf0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34cf0-112">Return value</span></span>

<span data-ttu-id="34cf0-113">Cette méthode retourne un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="34cf0-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="34cf0-114">Notes</span><span class="sxs-lookup"><span data-stu-id="34cf0-114">Remarks</span></span>

<span data-ttu-id="34cf0-115">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="34cf0-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="34cf0-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="34cf0-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="34cf0-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="34cf0-117">Examples</span></span>

<span data-ttu-id="34cf0-118">L’exemple JScript suivant utilise *MediaCollection*. **GetByName** pour récupérer trois éléments de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="34cf0-118">The following JScript example uses *MediaCollection*.**getByName** to retrieve three items from the library.</span></span> <span data-ttu-id="34cf0-119">Chaque élément est ensuite ajouté à la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="34cf0-119">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="34cf0-120">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="34cf0-120">The **Player** object was created with ID="Player".</span></span>


```JScript
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get a playlist object that contains an Internet URL.
var One = Player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");
 
// Get a playlist object that contains a file on a network server.
var Two = Player.mediaCollection.getByName("Jeanne");

// Get a playlist object that contains a file on a local drive.
var Three = Player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use Playlist.item with
// an index of zero to reference that item.
Player.currentPlaylist.appendItem(One.item(0));
Player.currentPlaylist.appendItem(Two.item(0));
Player.currentPlaylist.appendItem(Three.item(0));

```



## <a name="requirements"></a><span data-ttu-id="34cf0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34cf0-121">Requirements</span></span>



| <span data-ttu-id="34cf0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34cf0-122">Requirement</span></span> | <span data-ttu-id="34cf0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="34cf0-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34cf0-124">Version</span><span class="sxs-lookup"><span data-stu-id="34cf0-124">Version</span></span><br/> | <span data-ttu-id="34cf0-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="34cf0-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="34cf0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="34cf0-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="34cf0-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34cf0-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34cf0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34cf0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34cf0-129">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="34cf0-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="34cf0-130">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="34cf0-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="34cf0-131">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="34cf0-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="34cf0-132">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="34cf0-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





