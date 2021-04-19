---
title: PLAYLIST. dropDownList
description: L’attribut dropDownList spécifie ou récupère une valeur indiquant les éléments qui apparaissent dans la zone de liste déroulante pour une instance donnée de l’élément de sélection.
ms.assetid: 583041b0-25dc-4015-a3b2-37f3cfdcd496
keywords:
- Lecteur Windows Media PLAYLIST. dropDownList
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownList
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acf98dec7d50e2a3cd0b53acc07b0b8695f8461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541048"
---
# <a name="playlistdropdownlist"></a><span data-ttu-id="2cfd8-104">PLAYLIST. dropDownList</span><span class="sxs-lookup"><span data-stu-id="2cfd8-104">PLAYLIST.dropDownList</span></span>

<span data-ttu-id="2cfd8-105">L’attribut **dropDownList** spécifie ou récupère une valeur indiquant les éléments qui apparaissent dans la zone de liste déroulante pour une instance donnée de l’élément de **sélection** .</span><span class="sxs-lookup"><span data-stu-id="2cfd8-105">The **dropDownList** attribute specifies or retrieves a value indicating which elements show up in the drop-down list box for a given instance of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.dropDownList
```

## <a name="possible-values"></a><span data-ttu-id="2cfd8-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="2cfd8-106">Possible Values</span></span>

<span data-ttu-id="2cfd8-107">Cet attribut est une **chaîne** en lecture/écriture contenant l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2cfd8-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="2cfd8-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cfd8-108">Value</span></span>       | <span data-ttu-id="2cfd8-109">Description</span><span class="sxs-lookup"><span data-stu-id="2cfd8-109">Description</span></span>                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cfd8-110">showAlbums</span><span class="sxs-lookup"><span data-stu-id="2cfd8-110">showAlbums</span></span>  | <span data-ttu-id="2cfd8-111">Affiche les albums.</span><span class="sxs-lookup"><span data-stu-id="2cfd8-111">Shows albums.</span></span>                                                                                    |
| <span data-ttu-id="2cfd8-112">showAll</span><span class="sxs-lookup"><span data-stu-id="2cfd8-112">showAll</span></span>     | <span data-ttu-id="2cfd8-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="2cfd8-113">Default.</span></span> <span data-ttu-id="2cfd8-114">Affiche tous les éléments disponibles, y compris les sélections de CD, les sélections utilisateur et les présélections radio.</span><span class="sxs-lookup"><span data-stu-id="2cfd8-114">Shows all available elements including CD playlists, user playlists, and radio presets.</span></span> |
| <span data-ttu-id="2cfd8-115">showCD</span><span class="sxs-lookup"><span data-stu-id="2cfd8-115">showCD</span></span>      | <span data-ttu-id="2cfd8-116">Affiche la sélection de CD.</span><span class="sxs-lookup"><span data-stu-id="2cfd8-116">Shows the CD playlist.</span></span>                                                                           |
| <span data-ttu-id="2cfd8-117">showClips</span><span class="sxs-lookup"><span data-stu-id="2cfd8-117">showClips</span></span>   | <span data-ttu-id="2cfd8-118">Affiche tous les clips.</span><span class="sxs-lookup"><span data-stu-id="2cfd8-118">Shows all clips.</span></span>                                                                                 |
| <span data-ttu-id="2cfd8-119">showCurrent</span><span class="sxs-lookup"><span data-stu-id="2cfd8-119">showCurrent</span></span> | <span data-ttu-id="2cfd8-120">Affiche la sélection non enregistrée en cours.</span><span class="sxs-lookup"><span data-stu-id="2cfd8-120">Shows the current, unsaved playlist.</span></span>                                                             |
| <span data-ttu-id="2cfd8-121">showLibrary</span><span class="sxs-lookup"><span data-stu-id="2cfd8-121">showLibrary</span></span> | <span data-ttu-id="2cfd8-122">Affiche uniquement les sélections de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2cfd8-122">Shows only library playlists.</span></span>                                                                    |
| <span data-ttu-id="2cfd8-123">showRadio</span><span class="sxs-lookup"><span data-stu-id="2cfd8-123">showRadio</span></span>   | <span data-ttu-id="2cfd8-124">Affiche les présélections radio.</span><span class="sxs-lookup"><span data-stu-id="2cfd8-124">Shows radio presets.</span></span>                                                                             |
| <span data-ttu-id="2cfd8-125">showQueries</span><span class="sxs-lookup"><span data-stu-id="2cfd8-125">showQueries</span></span> | <span data-ttu-id="2cfd8-126">Affiche les requêtes.</span><span class="sxs-lookup"><span data-stu-id="2cfd8-126">Shows queries.</span></span>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="2cfd8-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cfd8-127">Requirements</span></span>



| <span data-ttu-id="2cfd8-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cfd8-128">Requirement</span></span> | <span data-ttu-id="2cfd8-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cfd8-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2cfd8-130">Version</span><span class="sxs-lookup"><span data-stu-id="2cfd8-130">Version</span></span><br/> | <span data-ttu-id="2cfd8-131">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="2cfd8-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2cfd8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cfd8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cfd8-133">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="2cfd8-133">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





