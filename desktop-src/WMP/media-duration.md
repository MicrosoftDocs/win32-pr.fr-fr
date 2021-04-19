---
title: Media. Duration
description: La propriété Duration récupère, en secondes, la durée de l’élément multimédia actuel.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media. Duration Windows Media Player
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71586f6aa37401d56a9e9537bfbea6c5af23f318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529961"
---
# <a name="mediaduration"></a><span data-ttu-id="fe549-104">Media. Duration</span><span class="sxs-lookup"><span data-stu-id="fe549-104">Media.duration</span></span>

<span data-ttu-id="fe549-105">La propriété **Duration** récupère, en secondes, la durée de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="fe549-105">The **duration** property retrieves the duration of the current media item in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe549-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe549-106">Syntax</span></span>

<span data-ttu-id="fe549-107">*lecteur*. *currentMedia*. **durée**</span><span class="sxs-lookup"><span data-stu-id="fe549-107">*player*.*currentMedia*.**duration**</span></span>

## <a name="possible-values"></a><span data-ttu-id="fe549-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="fe549-108">Possible Values</span></span>

<span data-ttu-id="fe549-109">Cette propriété est un **nombre** en lecture seule ( **double**).</span><span class="sxs-lookup"><span data-stu-id="fe549-109">This property is a read-only **Number** ( **double**).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe549-110">Notes</span><span class="sxs-lookup"><span data-stu-id="fe549-110">Remarks</span></span>

<span data-ttu-id="fe549-111">Si cette propriété est utilisée avec un élément multimédia autre que celui spécifié dans le *lecteur*. **currentMedia**, il ne peut pas contenir une valeur valide.</span><span class="sxs-lookup"><span data-stu-id="fe549-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span>

<span data-ttu-id="fe549-112">Pour récupérer la durée des fichiers qui ne sont pas dans la bibliothèque de l’utilisateur, vous devez attendre que le lecteur Windows Media ouvre le fichier. autrement dit, le OpenState actuel doit être égal à MediaOpen.</span><span class="sxs-lookup"><span data-stu-id="fe549-112">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current OpenState must equal MediaOpen.</span></span> <span data-ttu-id="fe549-113">Vous pouvez le vérifier en gérant le *lecteur*. Événement **OpenStateChange** ou en vérifiant régulièrement la valeur de *Player*. **openState**.</span><span class="sxs-lookup"><span data-stu-id="fe549-113">You can verify this by handling the *Player*.**OpenStateChange** event or by periodically checking the value of *Player*.**openState**.</span></span>

<span data-ttu-id="fe549-114">Pour les sélections, la durée de chaque élément multimédia peut être récupérée lors de l’ouverture de l’élément multimédia individuel, plutôt que lors de l’ouverture de la sélection.</span><span class="sxs-lookup"><span data-stu-id="fe549-114">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="fe549-115">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="fe549-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="fe549-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fe549-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="fe549-117">L’exemple JScript suivant utilise un *média*. **durée** d’affichage de l’heure restante dans l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="fe549-117">The following JScript example uses *Media*.**duration** to display the time remaining in the current media item.</span></span> <span data-ttu-id="fe549-118">Un élément DIV HTML nommé RemTime affiche les informations.</span><span class="sxs-lookup"><span data-stu-id="fe549-118">An HTML DIV element named RemTime displays the information.</span></span> <span data-ttu-id="fe549-119">Un minuteur HTML met à jour le texte de l’élément DIV chaque seconde.</span><span class="sxs-lookup"><span data-stu-id="fe549-119">An HTML timer updates the text in the DIV element every second.</span></span>

<span data-ttu-id="fe549-120">Le code JScript suivant démarre le minuteur :</span><span class="sxs-lookup"><span data-stu-id="fe549-120">The following JScript code starts the timer:</span></span>


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



<span data-ttu-id="fe549-121">Le code JScript suivant arrête le minuteur :</span><span class="sxs-lookup"><span data-stu-id="fe549-121">The following JScript code stops the timer:</span></span>


```JScript
window.clearInterval(idTmr);
```



<span data-ttu-id="fe549-122">Utilisez le *lecteur*. Événement **PlayStateChange** avec une instruction **switch** pour déterminer quand démarrer et arrêter le minuteur.</span><span class="sxs-lookup"><span data-stu-id="fe549-122">Use the *Player*.**PlayStateChange** event with a **switch** statement to determine when to start and stop the timer.</span></span>

<span data-ttu-id="fe549-123">Le code JScript suivant s’exécute chaque fois que la minuterie appelle la fonction de mise à jour :</span><span class="sxs-lookup"><span data-stu-id="fe549-123">The following JScript code executes each time the timer calls the update function:</span></span>


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
```



## <a name="requirements"></a><span data-ttu-id="fe549-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe549-124">Requirements</span></span>



| <span data-ttu-id="fe549-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe549-125">Requirement</span></span> | <span data-ttu-id="fe549-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe549-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe549-127">Version</span><span class="sxs-lookup"><span data-stu-id="fe549-127">Version</span></span><br/> | <span data-ttu-id="fe549-128">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="fe549-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fe549-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fe549-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="fe549-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe549-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe549-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe549-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe549-132">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="fe549-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="fe549-133">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="fe549-133">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="fe549-134">**Événement Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="fe549-134">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="fe549-135">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fe549-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="fe549-136">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="fe549-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





