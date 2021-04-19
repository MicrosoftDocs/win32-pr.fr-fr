---
title: Player. currentMedia
description: La propriété currentMedia spécifie ou récupère l’objet multimédia actuel.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Lecteur Windows Media Player. currentMedia
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea90b7be72bcb10a8ec0d3c49116f3effceb9a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520930"
---
# <a name="playercurrentmedia"></a><span data-ttu-id="26c5e-104">Player. currentMedia</span><span class="sxs-lookup"><span data-stu-id="26c5e-104">Player.currentMedia</span></span>

<span data-ttu-id="26c5e-105">La propriété **currentMedia** spécifie ou récupère l’objet multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="26c5e-105">The **currentMedia** property specifies or retrieves the current Media object.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c5e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26c5e-106">Syntax</span></span>

<span data-ttu-id="26c5e-107">*lecteur* . **currentMedia**</span><span class="sxs-lookup"><span data-stu-id="26c5e-107">*player* .**currentMedia**</span></span>

## <a name="possible-values"></a><span data-ttu-id="26c5e-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="26c5e-108">Possible Values</span></span>

<span data-ttu-id="26c5e-109">Cette propriété est un objet multimédia en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="26c5e-109">This property is a read/write Media object.</span></span>

## <a name="remarks"></a><span data-ttu-id="26c5e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="26c5e-110">Remarks</span></span>

<span data-ttu-id="26c5e-111">Si les *paramètres*. la propriété **AutoStart** a la valeur true, la lecture commence automatiquement chaque fois que vous définissez **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="26c5e-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="26c5e-112">Cette propriété prend un objet multimédia, qui peut être acquis à l’aide de la *sélection*. **élément**.</span><span class="sxs-lookup"><span data-stu-id="26c5e-112">This property takes a Media object, which can be acquired by using *Playlist*.**item**.</span></span> <span data-ttu-id="26c5e-113">Pour charger un élément **multimédia** à l’aide d’un nom de fichier, définissez la propriété URL ou utilisez **newMedia**.</span><span class="sxs-lookup"><span data-stu-id="26c5e-113">To load a **Media** item using a file name, set the URL property or use **newMedia**.</span></span>

## <a name="examples"></a><span data-ttu-id="26c5e-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="26c5e-114">Examples</span></span>

<span data-ttu-id="26c5e-115">L’exemple JScript suivant récupère le premier élément multimédia de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="26c5e-115">The following JScript example retrieves the first media item in the library.</span></span> <span data-ttu-id="26c5e-116">Il utilise ensuite **currentMedia** pour transformer l’élément multimédia récupéré en élément multimédia actuel, puis pour afficher le nom de l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="26c5e-116">It then uses **currentMedia** to make the retrieved media item the current media item, and then to display the name of the current media item.</span></span> <span data-ttu-id="26c5e-117">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="26c5e-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
```



## <a name="requirements"></a><span data-ttu-id="26c5e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26c5e-118">Requirements</span></span>



| <span data-ttu-id="26c5e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26c5e-119">Requirement</span></span> | <span data-ttu-id="26c5e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="26c5e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26c5e-121">Version</span><span class="sxs-lookup"><span data-stu-id="26c5e-121">Version</span></span><br/> | <span data-ttu-id="26c5e-122">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="26c5e-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="26c5e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="26c5e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="26c5e-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26c5e-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26c5e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26c5e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c5e-126">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="26c5e-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="26c5e-127">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="26c5e-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="26c5e-128">**Player. newMedia**</span><span class="sxs-lookup"><span data-stu-id="26c5e-128">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="26c5e-129">**Playlist. Item**</span><span class="sxs-lookup"><span data-stu-id="26c5e-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="26c5e-130">**Paramètres. démarrage automatique**</span><span class="sxs-lookup"><span data-stu-id="26c5e-130">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





