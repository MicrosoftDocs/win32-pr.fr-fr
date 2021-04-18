---
title: Media. markerCount
description: La propriété markerCount récupère le nombre de marqueurs dans l’élément multimédia.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media. markerCount Windows Media Player
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522807"
---
# <a name="mediamarkercount"></a><span data-ttu-id="bbe20-104">Media. markerCount</span><span class="sxs-lookup"><span data-stu-id="bbe20-104">Media.markerCount</span></span>

<span data-ttu-id="bbe20-105">La propriété **markerCount** récupère le nombre de marqueurs dans l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="bbe20-105">The **markerCount** property retrieves the number of markers in the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe20-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbe20-106">Syntax</span></span>

<span data-ttu-id="bbe20-107">*lecteur*. *currentMedia*. **markerCount**</span><span class="sxs-lookup"><span data-stu-id="bbe20-107">*player*.*currentMedia*.**markerCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="bbe20-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="bbe20-108">Possible Values</span></span>

<span data-ttu-id="bbe20-109">Cette propriété est un **nombre** en lecture seule (**long**) qui spécifie le nombre de marqueurs dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="bbe20-109">This property is a read-only **Number** (**long**) specifying the number of markers in the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbe20-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bbe20-110">Remarks</span></span>

<span data-ttu-id="bbe20-111">Cette propriété retourne la valeur zéro si un fichier n’a pas de marqueurs, ou si l’élément multimédia n’est pas le même que le *joueur*. **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="bbe20-111">This property returns zero if a file has no markers, or if the media item is not the same as *Player*.**currentMedia**.</span></span>

<span data-ttu-id="bbe20-112">Les numéros des marqueurs commencent à 1.</span><span class="sxs-lookup"><span data-stu-id="bbe20-112">Marker numbers start at 1.</span></span>

<span data-ttu-id="bbe20-113">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="bbe20-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="bbe20-114">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="bbe20-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bbe20-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="bbe20-115">Examples</span></span>

<span data-ttu-id="bbe20-116">L’exemple JScript suivant utilise un *média*. **markerCount** pour récupérer le nombre de marqueurs dans l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="bbe20-116">The following JScript example uses *Media*.**markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="bbe20-117">Cette valeur est ensuite utilisée comme limite supérieure pour une structure de bouclage, qui itère au sein de la liste des marqueurs pour récupérer chaque nom de marqueur.</span><span class="sxs-lookup"><span data-stu-id="bbe20-117">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name.</span></span> <span data-ttu-id="bbe20-118">Un élément TEXTAREA HTML nommé MNAMES affiche les noms des marqueurs dans l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="bbe20-118">An HTML TEXTAREA element named MNAMES displays the names of the markers in the current media item.</span></span> <span data-ttu-id="bbe20-119">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="bbe20-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="bbe20-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbe20-120">Requirements</span></span>



| <span data-ttu-id="bbe20-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbe20-121">Requirement</span></span> | <span data-ttu-id="bbe20-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbe20-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe20-123">Version</span><span class="sxs-lookup"><span data-stu-id="bbe20-123">Version</span></span><br/> | <span data-ttu-id="bbe20-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bbe20-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bbe20-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bbe20-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="bbe20-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbe20-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbe20-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbe20-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe20-128">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="bbe20-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="bbe20-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="bbe20-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="bbe20-130">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bbe20-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="bbe20-131">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bbe20-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





