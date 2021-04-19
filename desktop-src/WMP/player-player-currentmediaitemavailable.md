---
title: Événement Player. CurrentMediaItemAvailable
description: L’événement CurrentMediaItemAvailable se produit lorsqu’un élément de métadonnées graphiques de l’élément multimédia actuel devient disponible. | Événement Player. CurrentMediaItemAvailable
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Événement CurrentMediaItemAvailable lecteur Windows Media
- Événement CurrentMediaItemAvailable lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement CurrentMediaItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523964"
---
# <a name="playercurrentmediaitemavailable-event"></a><span data-ttu-id="17888-107">Événement Player. CurrentMediaItemAvailable</span><span class="sxs-lookup"><span data-stu-id="17888-107">Player.CurrentMediaItemAvailable event</span></span>

<span data-ttu-id="17888-108">L’événement **CurrentMediaItemAvailable** se produit lorsqu’un élément de métadonnées graphiques de l’élément multimédia actuel devient disponible.</span><span class="sxs-lookup"><span data-stu-id="17888-108">The **CurrentMediaItemAvailable** event occurs when a graphic metadata item in the current media item becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="17888-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17888-109">Syntax</span></span>


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="17888-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17888-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17888-111">*bstrItemName*</span><span class="sxs-lookup"><span data-stu-id="17888-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="17888-112">**Chaîne** contenant le nom de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="17888-112">**String** containing the name of the current media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17888-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17888-113">Return value</span></span>

<span data-ttu-id="17888-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="17888-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17888-115">Notes</span><span class="sxs-lookup"><span data-stu-id="17888-115">Remarks</span></span>

<span data-ttu-id="17888-116">Dans la mesure où la lecture peut commencer avant le téléchargement complet d’un élément multimédia, les graphiques de métadonnées contenus dans l’élément multimédia (par exemple, les jaquettes de la couverture de l’album) peuvent ne pas être disponibles au début de la lecture.</span><span class="sxs-lookup"><span data-stu-id="17888-116">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="17888-117">Cet événement vous avertit à la fin du téléchargement d’un élément de graphique de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="17888-117">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="17888-118">Vous pouvez ensuite récupérer l’objet **Media** en passant la valeur de *bstrItemName* à *MediaCollection*. méthode **GetByName** , après laquelle vous pouvez accéder à l’élément de graphique de métadonnées à l’aide d’un *média*. **getItemInfoByType** et en spécifiant **WM/image** comme nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="17888-118">You can then retrieve the **Media** object by passing the value of *bstrItemName* to the *MediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *Media*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

<span data-ttu-id="17888-119">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="17888-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="17888-120">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="17888-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="17888-121">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="17888-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="17888-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17888-122">Requirements</span></span>



| <span data-ttu-id="17888-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17888-123">Requirement</span></span> | <span data-ttu-id="17888-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="17888-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17888-125">Version</span><span class="sxs-lookup"><span data-stu-id="17888-125">Version</span></span><br/> | <span data-ttu-id="17888-126">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="17888-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="17888-127">DLL</span><span class="sxs-lookup"><span data-stu-id="17888-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="17888-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17888-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17888-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17888-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17888-130">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="17888-130">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="17888-131">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="17888-131">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="17888-132">**MediaCollection.getByName**</span><span class="sxs-lookup"><span data-stu-id="17888-132">**MediaCollection.getByName**</span></span>](mediacollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="17888-133">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="17888-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





