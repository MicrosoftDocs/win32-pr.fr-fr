---
title: Cdrom. playlist
description: La propriété playlist récupère un objet playlist représentant les pistes sur le CD-ROM actuellement dans le lecteur de CD ou les entrées de titre au niveau de la racine pour le DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Lecteur Windows Media cdrom. playlist
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512163"
---
# <a name="cdromplaylist"></a><span data-ttu-id="63e59-104">Cdrom. playlist</span><span class="sxs-lookup"><span data-stu-id="63e59-104">Cdrom.playlist</span></span>

<span data-ttu-id="63e59-105">La propriété **playlist** récupère un objet **playlist** représentant les pistes sur le CD-ROM actuellement dans le lecteur de CD ou les entrées de titre au niveau de la racine pour le DVD.</span><span class="sxs-lookup"><span data-stu-id="63e59-105">The **playlist** property retrieves a **Playlist** object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a><span data-ttu-id="63e59-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="63e59-106">Possible Values</span></span>

<span data-ttu-id="63e59-107">Cette propriété est un objet de **sélection** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="63e59-107">This property is a read-only **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="63e59-108">Notes</span><span class="sxs-lookup"><span data-stu-id="63e59-108">Remarks</span></span>

<span data-ttu-id="63e59-109">En règle générale, les DVD sont organisés en titres.</span><span class="sxs-lookup"><span data-stu-id="63e59-109">Typically, DVDs are organized into titles.</span></span> <span data-ttu-id="63e59-110">Chaque titre contient un ou plusieurs chapitres.</span><span class="sxs-lookup"><span data-stu-id="63e59-110">Each title contains one or more chapters.</span></span> <span data-ttu-id="63e59-111">Chaque DVD étant créé différemment, la façon dont les titres et les chapitres sont utilisés est celle de l’auteur du contenu.</span><span class="sxs-lookup"><span data-stu-id="63e59-111">Each DVD is authored differently, so how titles and chapters are used is up to the content author.</span></span>

<span data-ttu-id="63e59-112">Pour le DVD, cette méthode récupère une sélection qui contient comme premier élément un objet **multimédia** qui représente le support DVD.</span><span class="sxs-lookup"><span data-stu-id="63e59-112">For DVD, this method retrieves a playlist that contains as the first item a **Media** object that represents the DVD media.</span></span> <span data-ttu-id="63e59-113">La lecture de l’élément entraîne la lecture du DVD à partir du début s’il s’agit de la première lecture après l’insertion d’un nouveau DVD, ou la reprise de la lecture si le DVD est le même que le dernier DVD affiché.</span><span class="sxs-lookup"><span data-stu-id="63e59-113">Playing the item results in the DVD playing from the beginning if it is the first play after inserting a new DVD, or resuming playback if the DVD is the same as the last DVD viewed.</span></span> <span data-ttu-id="63e59-114">La définition de cet élément en tant qu’élément actuel pendant la lecture entraîne la lecture du DVD à partir du début.</span><span class="sxs-lookup"><span data-stu-id="63e59-114">Setting this item as the current one during playback results in the DVD playing from the beginning.</span></span>

<span data-ttu-id="63e59-115">Les éléments supplémentaires (objets **multimédias** ) de la sélection sont des titres de DVD représentés par des sélections imbriquées.</span><span class="sxs-lookup"><span data-stu-id="63e59-115">Additional items (**Media** objects) in the playlist are DVD titles that are represented by nested playlists.</span></span> <span data-ttu-id="63e59-116">Lorsque vous spécifiez des *contrôles*. **CurrentItem** pour correspondre à l’un de ces éléments de sélection imbriqués, le lecteur Windows Media définit automatiquement la sélection imbriquée en tant que *lecteur*. **currentPlaylist** après le début de la lecture du chapitre.</span><span class="sxs-lookup"><span data-stu-id="63e59-116">When you specify *Controls*.**currentItem** to equal one of these nested playlist items, Windows Media Player automatically sets the nested playlist as *Player*.**currentPlaylist** after chapter playback begins.</span></span> <span data-ttu-id="63e59-117">Vous pouvez ensuite utiliser les propriétés, méthodes et événements de l’objet **currentPlaylist** pour travailler avec des chapitres DVD, qui sont également des éléments de sélection.</span><span class="sxs-lookup"><span data-stu-id="63e59-117">You can then use the **currentPlaylist** object properties, methods, and events to work with DVD chapters, which are also playlist items.</span></span>

<span data-ttu-id="63e59-118">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="63e59-118">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="63e59-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="63e59-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="63e59-120">**Lecteur Windows Media 10 Mobile :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="63e59-120">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="63e59-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="63e59-121">Examples</span></span>

<span data-ttu-id="63e59-122">L’exemple suivant utilise *cdrom*. **pour remplir un élément de texte** html, nommé myText, avec les titres du CD audio actuellement présent dans le premier lecteur de CD.</span><span class="sxs-lookup"><span data-stu-id="63e59-122">The following example uses *Cdrom*.**playlist** to fill an HTML text element, named myText, with the titles of the audio CD currently in the first CD drive.</span></span> <span data-ttu-id="63e59-123">Utilisez *CdromCollection*. **nombre** pour déterminer le nombre de lecteurs de CD disponibles.</span><span class="sxs-lookup"><span data-stu-id="63e59-123">Use *CdromCollection*.**count** to determine the number of available CD drives.</span></span> <span data-ttu-id="63e59-124">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="63e59-124">The **Player** object was created with ID = "Player".</span></span>


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a><span data-ttu-id="63e59-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63e59-125">Requirements</span></span>



| <span data-ttu-id="63e59-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63e59-126">Requirement</span></span> | <span data-ttu-id="63e59-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="63e59-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63e59-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63e59-128">Minimum supported client</span></span><br/> | <span data-ttu-id="63e59-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63e59-129">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="63e59-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63e59-130">Minimum supported server</span></span><br/> | <span data-ttu-id="63e59-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63e59-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="63e59-132">Version</span><span class="sxs-lookup"><span data-stu-id="63e59-132">Version</span></span><br/>                  | <span data-ttu-id="63e59-133">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="63e59-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="63e59-134">DLL</span><span class="sxs-lookup"><span data-stu-id="63e59-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e59-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63e59-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e59-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63e59-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e59-137">**Objet cdrom**</span><span class="sxs-lookup"><span data-stu-id="63e59-137">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="63e59-138">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="63e59-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="63e59-139">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="63e59-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





