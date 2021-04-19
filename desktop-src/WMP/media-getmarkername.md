---
title: Méthode Media. getMarkerName
description: La méthode getMarkerName récupère le nom du marqueur à l’index spécifié.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- méthode getMarkerName lecteur Windows Media
- méthode getMarkerName lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode getMarkerName
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533452"
---
# <a name="mediagetmarkername-method"></a><span data-ttu-id="35c1e-106">Méthode Media. getMarkerName</span><span class="sxs-lookup"><span data-stu-id="35c1e-106">Media.getMarkerName method</span></span>

<span data-ttu-id="35c1e-107">La méthode **getMarkerName** récupère le nom du marqueur à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="35c1e-107">The **getMarkerName** method retrieves the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c1e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35c1e-108">Syntax</span></span>


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="35c1e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35c1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35c1e-110">*markerNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35c1e-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35c1e-111">**Nombre** (**long**) spécifiant un index de marqueur.</span><span class="sxs-lookup"><span data-stu-id="35c1e-111">**Number** (**long**) specifying a marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35c1e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35c1e-112">Return value</span></span>

<span data-ttu-id="35c1e-113">Cette méthode retourne une **chaîne**.</span><span class="sxs-lookup"><span data-stu-id="35c1e-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="35c1e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="35c1e-114">Remarks</span></span>

<span data-ttu-id="35c1e-115">Cette méthode retourne la **valeur null** si le marqueur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="35c1e-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="35c1e-116">Certains éléments multimédias numériques ne contiennent pas de marqueurs.</span><span class="sxs-lookup"><span data-stu-id="35c1e-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="35c1e-117">Utilisez **markerCount** pour déterminer le nombre de marqueurs dans le clip actuel.</span><span class="sxs-lookup"><span data-stu-id="35c1e-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="35c1e-118">Les numéros d’index des marqueurs commencent à 1.</span><span class="sxs-lookup"><span data-stu-id="35c1e-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="35c1e-119">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="35c1e-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="35c1e-120">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="35c1e-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="35c1e-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="35c1e-121">Examples</span></span>

<span data-ttu-id="35c1e-122">L’exemple JScript suivant utilise un *média*. **getMarkerName** pour remplir un élément textarea html nommé MNAMES avec les noms des marqueurs dans l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="35c1e-122">The following JScript example uses *Media*.**getMarkerName** to fill an HTML TEXTAREA element named MNAMES with the names of the markers in the current media item.</span></span> <span data-ttu-id="35c1e-123">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="35c1e-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="35c1e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35c1e-124">Requirements</span></span>



| <span data-ttu-id="35c1e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35c1e-125">Requirement</span></span> | <span data-ttu-id="35c1e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="35c1e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35c1e-127">Version</span><span class="sxs-lookup"><span data-stu-id="35c1e-127">Version</span></span><br/> | <span data-ttu-id="35c1e-128">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="35c1e-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="35c1e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="35c1e-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="35c1e-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35c1e-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35c1e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35c1e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c1e-132">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="35c1e-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="35c1e-133">**Media. getMarkerTime**</span><span class="sxs-lookup"><span data-stu-id="35c1e-133">**Media.getMarkerTime**</span></span>](media-getmarkertime.md)
</dt> <dt>

[<span data-ttu-id="35c1e-134">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="35c1e-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="35c1e-135">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="35c1e-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="35c1e-136">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="35c1e-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





