---
title: Controls. playItem, méthode
description: La méthode playItem lit l’élément multimédia spécifié. | Controls. playItem, méthode
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- méthode playItem lecteur Windows Media
- méthode playItem lecteur Windows Media, classe de contrôles
- Classe Controls lecteur Windows Media, méthode playItem
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535345"
---
# <a name="controlsplayitem-method"></a><span data-ttu-id="7a292-107">Controls. playItem, méthode</span><span class="sxs-lookup"><span data-stu-id="7a292-107">Controls.playItem method</span></span>

<span data-ttu-id="7a292-108">La méthode **playItem** lit l’élément multimédia spécifié.</span><span class="sxs-lookup"><span data-stu-id="7a292-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a292-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a292-109">Syntax</span></span>


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a><span data-ttu-id="7a292-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a292-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a292-111">*theMediaItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a292-111">*theMediaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a292-112">Objet **multimédia** à lire.</span><span class="sxs-lookup"><span data-stu-id="7a292-112">**Media** object to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a292-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a292-113">Return value</span></span>

<span data-ttu-id="7a292-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7a292-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a292-115">Notes</span><span class="sxs-lookup"><span data-stu-id="7a292-115">Remarks</span></span>

<span data-ttu-id="7a292-116">L’élément multimédia est chargé et lu automatiquement, quelle que soit la valeur des *paramètres*. propriété **AutoStart** .</span><span class="sxs-lookup"><span data-stu-id="7a292-116">The media item will be loaded and played automatically, regardless of the value of the *Settings*.**autoStart** property.</span></span> <span data-ttu-id="7a292-117">Pour charger un élément sans le lancer automatiquement, définissez *paramètres*. **démarrage automatique** sur false et attribution d’une valeur à *Player*. **URL**, après laquelle la **lecture** peut être appelée pour démarrer la lecture de l’élément.</span><span class="sxs-lookup"><span data-stu-id="7a292-117">To load an item without playing it automatically, set *Settings*.**autoStart** to false and assign a value to *Player*.**URL**, after which **play** can be called to start playing the item.</span></span>

<span data-ttu-id="7a292-118">Remarque</span><span class="sxs-lookup"><span data-stu-id="7a292-118">Note</span></span>

<span data-ttu-id="7a292-119">**playItem** fonctionne uniquement avec les éléments dans *currentPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="7a292-119">**playItem** works only with items in *currentPlaylist*.</span></span> <span data-ttu-id="7a292-120">L’appel de **playItem** avec une référence à un élément multimédia enregistré n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7a292-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="7a292-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="7a292-121">Examples</span></span>

<span data-ttu-id="7a292-122">L’exemple JScript suivant utilise **playItem** pour lire un élément multimédia à partir de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="7a292-122">The following JScript example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="7a292-123">L’élément à lire est choisi en fonction de sa position dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="7a292-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="7a292-124">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="7a292-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a><span data-ttu-id="7a292-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a292-125">Requirements</span></span>



| <span data-ttu-id="7a292-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a292-126">Requirement</span></span> | <span data-ttu-id="7a292-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a292-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a292-128">Version</span><span class="sxs-lookup"><span data-stu-id="7a292-128">Version</span></span><br/> | <span data-ttu-id="7a292-129">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7a292-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7a292-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7a292-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="7a292-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a292-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a292-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a292-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a292-133">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="7a292-133">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="7a292-134">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="7a292-134">**Playlist.item**</span></span>](playlist-item.md)
</dt> </dl>

 

 





