---
title: Méthode Media. getMarkerTime
description: La méthode getMarkerTime récupère l’heure du marqueur au niveau de l’index spécifié.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- méthode getMarkerTime lecteur Windows Media
- méthode getMarkerTime lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode getMarkerTime
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543901"
---
# <a name="mediagetmarkertime-method"></a><span data-ttu-id="54412-106">Méthode Media. getMarkerTime</span><span class="sxs-lookup"><span data-stu-id="54412-106">Media.getMarkerTime method</span></span>

<span data-ttu-id="54412-107">La méthode **getMarkerTime** récupère l’heure du marqueur au niveau de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="54412-107">The **getMarkerTime** method retrieves the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="54412-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54412-108">Syntax</span></span>


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="54412-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54412-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54412-110">*markerNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54412-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54412-111">**Nombre** (**long**) spécifiant l’index du marqueur.</span><span class="sxs-lookup"><span data-stu-id="54412-111">**Number** (**long**) specifying the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54412-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54412-112">Return value</span></span>

<span data-ttu-id="54412-113">Cette méthode retourne un **nombre** (**double**) qui spécifie l’emplacement du marqueur, en secondes, à partir du début du clip.</span><span class="sxs-lookup"><span data-stu-id="54412-113">This method returns a **Number** (**double**) specifying the location of the marker in seconds from the beginning of the clip.</span></span>

## <a name="remarks"></a><span data-ttu-id="54412-114">Notes</span><span class="sxs-lookup"><span data-stu-id="54412-114">Remarks</span></span>

<span data-ttu-id="54412-115">Cette méthode retourne la **valeur null** si le marqueur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="54412-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="54412-116">Certains éléments multimédias numériques ne contiennent pas de marqueurs.</span><span class="sxs-lookup"><span data-stu-id="54412-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="54412-117">Utilisez **markerCount** pour déterminer le nombre de marqueurs dans le clip actuel.</span><span class="sxs-lookup"><span data-stu-id="54412-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="54412-118">Les numéros d’index des marqueurs commencent à 1.</span><span class="sxs-lookup"><span data-stu-id="54412-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="54412-119">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="54412-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="54412-120">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="54412-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="54412-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="54412-121">Examples</span></span>

<span data-ttu-id="54412-122">L’exemple JScript suivant utilise un *média*. **getMarkerTime** pour remplir un élément textarea html nommé MTIMES avec l’emplacement de chaque marqueur.</span><span class="sxs-lookup"><span data-stu-id="54412-122">The following JScript example uses *Media*.**getMarkerTime** to fill an HTML TEXTAREA element named MTIMES with the location of each marker.</span></span> <span data-ttu-id="54412-123">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="54412-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="54412-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54412-124">Requirements</span></span>



| <span data-ttu-id="54412-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54412-125">Requirement</span></span> | <span data-ttu-id="54412-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="54412-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54412-127">Version</span><span class="sxs-lookup"><span data-stu-id="54412-127">Version</span></span><br/> | <span data-ttu-id="54412-128">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="54412-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="54412-129">DLL</span><span class="sxs-lookup"><span data-stu-id="54412-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="54412-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54412-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54412-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54412-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54412-132">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="54412-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="54412-133">**Media. getMarkerName**</span><span class="sxs-lookup"><span data-stu-id="54412-133">**Media.getMarkerName**</span></span>](media-getmarkername.md)
</dt> <dt>

[<span data-ttu-id="54412-134">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="54412-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="54412-135">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="54412-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="54412-136">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="54412-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





