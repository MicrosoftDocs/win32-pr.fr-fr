---
title: Media. durationString
description: La propriété durationString récupère une valeur de chaîne indiquant la durée de l’élément multimédia actuel au format HH MM SS.
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- Media. durationString Windows Media Player
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537828"
---
# <a name="mediadurationstring"></a><span data-ttu-id="f6edb-104">Media. durationString</span><span class="sxs-lookup"><span data-stu-id="f6edb-104">Media.durationString</span></span>

<span data-ttu-id="f6edb-105">La propriété **durationString** récupère une valeur de **chaîne** indiquant la durée de l’élément multimédia actuel au format hh : mm : SS.</span><span class="sxs-lookup"><span data-stu-id="f6edb-105">The **durationString** property retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6edb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6edb-106">Syntax</span></span>

<span data-ttu-id="f6edb-107">*lecteur*. *currentMedia*. **durationString**</span><span class="sxs-lookup"><span data-stu-id="f6edb-107">*player*.*currentMedia*.**durationString**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f6edb-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="f6edb-108">Possible Values</span></span>

<span data-ttu-id="f6edb-109">Cette propriété est une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f6edb-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6edb-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f6edb-110">Remarks</span></span>

<span data-ttu-id="f6edb-111">Si cette propriété est utilisée avec un élément multimédia autre que celui spécifié dans le *lecteur*. **currentMedia**, il ne peut pas contenir une valeur valide.</span><span class="sxs-lookup"><span data-stu-id="f6edb-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span> <span data-ttu-id="f6edb-112">Si l’élément multimédia est inférieur à une heure, la partie HH : de la valeur de retour est omise.</span><span class="sxs-lookup"><span data-stu-id="f6edb-112">If the media item is less than an hour long, the HH: portion of the return value is omitted.</span></span>

<span data-ttu-id="f6edb-113">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="f6edb-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="f6edb-114">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f6edb-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f6edb-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="f6edb-115">Examples</span></span>

<span data-ttu-id="f6edb-116">L’exemple JScript suivant utilise un *média*. **durationString** pour afficher la durée de l’élément multimédia actuel comme texte mis en forme.</span><span class="sxs-lookup"><span data-stu-id="f6edb-116">The following JScript example uses *Media*.**durationString** to display the duration of the current media item as formatted text.</span></span> <span data-ttu-id="f6edb-117">Un élément DIV HTML nommé MediaInfo affiche les informations relatives à la durée.</span><span class="sxs-lookup"><span data-stu-id="f6edb-117">An HTML DIV element named MediaInfo displays the duration information.</span></span> <span data-ttu-id="f6edb-118">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f6edb-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="f6edb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6edb-119">Requirements</span></span>



| <span data-ttu-id="f6edb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6edb-120">Requirement</span></span> | <span data-ttu-id="f6edb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6edb-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6edb-122">Version</span><span class="sxs-lookup"><span data-stu-id="f6edb-122">Version</span></span><br/> | <span data-ttu-id="f6edb-123">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f6edb-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f6edb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f6edb-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="f6edb-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6edb-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6edb-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6edb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6edb-127">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="f6edb-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="f6edb-128">**Media. Duration**</span><span class="sxs-lookup"><span data-stu-id="f6edb-128">**Media.duration**</span></span>](media-duration.md)
</dt> <dt>

[<span data-ttu-id="f6edb-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="f6edb-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="f6edb-130">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f6edb-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f6edb-131">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f6edb-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





