---
title: Controls. currentMarker
description: La propriété currentMarker spécifie ou récupère le numéro de marqueur actuel.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Controls. currentMarker Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544465"
---
# <a name="controlscurrentmarker"></a><span data-ttu-id="6bb38-104">Controls. currentMarker</span><span class="sxs-lookup"><span data-stu-id="6bb38-104">Controls.currentMarker</span></span>

<span data-ttu-id="6bb38-105">La propriété **currentMarker** spécifie ou récupère le numéro de marqueur actuel.</span><span class="sxs-lookup"><span data-stu-id="6bb38-105">The **currentMarker** property specifies or retrieves the current marker number.</span></span>

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a><span data-ttu-id="6bb38-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="6bb38-106">Possible Values</span></span>

<span data-ttu-id="6bb38-107">Cette propriété est un **nombre** en lecture/écriture (**long**) avec une valeur par défaut de zéro.</span><span class="sxs-lookup"><span data-stu-id="6bb38-107">This property is a read/write **Number** (**long**) with a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb38-108">Notes</span><span class="sxs-lookup"><span data-stu-id="6bb38-108">Remarks</span></span>

<span data-ttu-id="6bb38-109">La définition de **currentMarker** entraîne le démarrage de la lecture à partir du marqueur spécifié.</span><span class="sxs-lookup"><span data-stu-id="6bb38-109">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="6bb38-110">Avant de tenter de définir **currentMarker**, déterminez si un fichier a des marqueurs et combien il a à l’aide de **markerCount**.</span><span class="sxs-lookup"><span data-stu-id="6bb38-110">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **markerCount**.</span></span> <span data-ttu-id="6bb38-111">Si un fichier n’a pas de marqueur, la définition de **currentMarker** sur n’importe quelle valeur, sauf zéro, génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="6bb38-111">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="6bb38-112">Si vous définissez **currentMarker** sur un nombre supérieur à **markerCount** , une erreur est également générée.</span><span class="sxs-lookup"><span data-stu-id="6bb38-112">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="6bb38-113">La propriété **currentMarker** retourne toujours le marqueur actuel ou le dernier marqueur, ce qui signifie que la position de fichier réelle peut être soit au marqueur actuel, soit avant le marqueur suivant.</span><span class="sxs-lookup"><span data-stu-id="6bb38-113">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="6bb38-114">Les marqueurs sont numérotés à partir de 1. par conséquent, si un fichier a des marqueurs, vous pouvez affecter la valeur zéro à **currentMarker** pour changer la position du fichier.</span><span class="sxs-lookup"><span data-stu-id="6bb38-114">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="6bb38-115">Jusqu’à ce que l’élément multimédia actuel soit défini (à l’aide de *Player*.**URL** ou *lecteur*. **currentMedia**), **currentMarker** retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="6bb38-115">Until the current media item is set (using *Player*.**URL** or *Player*.**currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="6bb38-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="6bb38-116">Examples</span></span>

<span data-ttu-id="6bb38-117">L’exemple JScript suivant utilise **currentMarker** pour démarrer la lecture vidéo à partir du marqueur qui correspond à la propriété **SelectedIndex** d’un élément Select HTML.</span><span class="sxs-lookup"><span data-stu-id="6bb38-117">The following JScript example uses **currentMarker** to start video playback from the marker that corresponds to the **selectedIndex** property of an HTML SELECT element.</span></span> <span data-ttu-id="6bb38-118">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6bb38-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="6bb38-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bb38-119">Requirements</span></span>



| <span data-ttu-id="6bb38-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bb38-120">Requirement</span></span> | <span data-ttu-id="6bb38-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bb38-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb38-122">Version</span><span class="sxs-lookup"><span data-stu-id="6bb38-122">Version</span></span><br/> | <span data-ttu-id="6bb38-123">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6bb38-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6bb38-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6bb38-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="6bb38-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bb38-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb38-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bb38-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb38-127">**Controls (objet)**</span><span class="sxs-lookup"><span data-stu-id="6bb38-127">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="6bb38-128">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="6bb38-128">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="6bb38-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="6bb38-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="6bb38-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="6bb38-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





