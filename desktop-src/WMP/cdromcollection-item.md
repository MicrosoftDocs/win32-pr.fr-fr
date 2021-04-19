---
title: CdromCollection. Item, méthode
description: La méthode Item récupère l’objet cdrom à l’index donné.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- méthode Item lecteur Windows Media
- méthode Item lecteur Windows Media, classe CdromCollection
- Classe CdromCollection lecteur Windows Media, méthode Item
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521758"
---
# <a name="cdromcollectionitem-method"></a><span data-ttu-id="387f7-106">CdromCollection. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="387f7-106">CdromCollection.item method</span></span>

<span data-ttu-id="387f7-107">La méthode **Item** récupère l’objet **cdrom** à l’index donné.</span><span class="sxs-lookup"><span data-stu-id="387f7-107">The **item** method retrieves the **Cdrom** object at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="387f7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="387f7-108">Syntax</span></span>


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="387f7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="387f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="387f7-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="387f7-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="387f7-111">**Nombre** (**long**) contenant l’index.</span><span class="sxs-lookup"><span data-stu-id="387f7-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="387f7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="387f7-112">Return value</span></span>

<span data-ttu-id="387f7-113">Cette méthode retourne un objet **cdrom** .</span><span class="sxs-lookup"><span data-stu-id="387f7-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="387f7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="387f7-114">Remarks</span></span>

<span data-ttu-id="387f7-115">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="387f7-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="387f7-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="387f7-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="387f7-117">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="387f7-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="387f7-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="387f7-118">Examples</span></span>

<span data-ttu-id="387f7-119">L’exemple JScript suivant utilise *CdromCollection*. **élément** pour imprimer le nom de la sélection à partir de chaque CD disponible sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="387f7-119">The following JScript example uses *CdromCollection*.**item** to print the playlist name from each CD available on the computer.</span></span> <span data-ttu-id="387f7-120">Si le lecteur contient réellement du contenu DVD, Windows XP ou version ultérieure est requis.</span><span class="sxs-lookup"><span data-stu-id="387f7-120">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="387f7-121">Un élément TextArea HTML a été créé avec ID = "Playlists".</span><span class="sxs-lookup"><span data-stu-id="387f7-121">An HTML TextArea element was created with ID = "playlists".</span></span> <span data-ttu-id="387f7-122">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="387f7-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="387f7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="387f7-123">Requirements</span></span>



| <span data-ttu-id="387f7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="387f7-124">Requirement</span></span> | <span data-ttu-id="387f7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="387f7-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="387f7-126">Version</span><span class="sxs-lookup"><span data-stu-id="387f7-126">Version</span></span><br/> | <span data-ttu-id="387f7-127">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="387f7-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="387f7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="387f7-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="387f7-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="387f7-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="387f7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="387f7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="387f7-131">**Cdrom. driveSpecifier**</span><span class="sxs-lookup"><span data-stu-id="387f7-131">**Cdrom.driveSpecifier**</span></span>](cdrom-drivespecifier.md)
</dt> <dt>

[<span data-ttu-id="387f7-132">**Objet CdromCollection**</span><span class="sxs-lookup"><span data-stu-id="387f7-132">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="387f7-133">**CdromCollection. Count**</span><span class="sxs-lookup"><span data-stu-id="387f7-133">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="387f7-134">**Playlist.name**</span><span class="sxs-lookup"><span data-stu-id="387f7-134">**Playlist.name**</span></span>](playlist-name.md)
</dt> <dt>

[<span data-ttu-id="387f7-135">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="387f7-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="387f7-136">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="387f7-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





