---
title: MediaCollection. Add, méthode
description: La méthode Add ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque. | MediaCollection. Add, méthode
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Ajouter une méthode lecteur Windows Media
- Add, méthode lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode Add
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525541"
---
# <a name="mediacollectionadd-method"></a><span data-ttu-id="8a8cb-107">MediaCollection. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="8a8cb-107">MediaCollection.add method</span></span>

<span data-ttu-id="8a8cb-108">La méthode **Add** ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="8a8cb-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a8cb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a8cb-109">Syntax</span></span>


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a><span data-ttu-id="8a8cb-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a8cb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a8cb-111">*chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a8cb-111">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a8cb-112">**Chaîne** contenant le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="8a8cb-112">**String** containing the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a8cb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a8cb-113">Return value</span></span>

<span data-ttu-id="8a8cb-114">Cette méthode retourne un objet **multimédia** .</span><span class="sxs-lookup"><span data-stu-id="8a8cb-114">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a8cb-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8a8cb-115">Remarks</span></span>

<span data-ttu-id="8a8cb-116">Cette méthode charge un élément multimédia existant ou une sélection dans la bibliothèque, en fonction d’un chemin d’accès à un fichier.</span><span class="sxs-lookup"><span data-stu-id="8a8cb-116">This method loads an existing media item or playlist into the library, given a path to a file.</span></span> <span data-ttu-id="8a8cb-117">Cette méthode ne déplace pas ou ne modifie pas le fichier.</span><span class="sxs-lookup"><span data-stu-id="8a8cb-117">This method does not move or change the file.</span></span> <span data-ttu-id="8a8cb-118">Cette méthode échoue si le chemin d’accès local n’est pas valide, mais que la validité des fichiers multimédias numériques n’est pas vérifiée avant leur ajout à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="8a8cb-118">This method fails if given an invalid local path, but digital media files are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="8a8cb-119">Cette méthode accepte à la fois les fichiers de sélection statique et automatique.</span><span class="sxs-lookup"><span data-stu-id="8a8cb-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="8a8cb-120">*PlaylistCollection*. la méthode **importPlaylist** peut également être utilisée pour ajouter une sélection statique à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="8a8cb-120">The *PlaylistCollection*.**importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="8a8cb-121">Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="8a8cb-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="8a8cb-122">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8a8cb-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8a8cb-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="8a8cb-123">Examples</span></span>

<span data-ttu-id="8a8cb-124">L’exemple Microsoft JScript suivant ajoute trois objets multimédias à la collection de supports du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8a8cb-124">The following Microsoft JScript example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="8a8cb-125">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="8a8cb-125">The **Player** object was created with ID="Player".</span></span>


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a><span data-ttu-id="8a8cb-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a8cb-126">Requirements</span></span>



| <span data-ttu-id="8a8cb-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a8cb-127">Requirement</span></span> | <span data-ttu-id="8a8cb-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a8cb-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8cb-129">Version</span><span class="sxs-lookup"><span data-stu-id="8a8cb-129">Version</span></span><br/> | <span data-ttu-id="8a8cb-130">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8a8cb-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8a8cb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8a8cb-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="8a8cb-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a8cb-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a8cb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a8cb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8cb-134">**Gestion des sélections**</span><span class="sxs-lookup"><span data-stu-id="8a8cb-134">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="8a8cb-135">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="8a8cb-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="8a8cb-136">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="8a8cb-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="8a8cb-137">**MediaCollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="8a8cb-137">**MediaCollection.remove**</span></span>](mediacollection-remove.md)
</dt> <dt>

[<span data-ttu-id="8a8cb-138">**PlaylistCollection.importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="8a8cb-138">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="8a8cb-139">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="8a8cb-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="8a8cb-140">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="8a8cb-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





