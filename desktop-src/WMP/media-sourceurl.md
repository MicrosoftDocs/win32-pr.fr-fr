---
title: Media. sourceURL
description: La propriété sourceURL récupère l’URL de l’élément multimédia.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media. sourceURL Windows Media Player
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c32d594cd1c3b590001eedfd09e9a8c8eb21240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540569"
---
# <a name="mediasourceurl"></a><span data-ttu-id="9dcb4-104">Media. sourceURL</span><span class="sxs-lookup"><span data-stu-id="9dcb4-104">Media.sourceURL</span></span>

<span data-ttu-id="9dcb4-105">La propriété **sourceURL** récupère l’URL de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-105">The **sourceURL** property retrieves the URL of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dcb4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9dcb4-106">Syntax</span></span>

<span data-ttu-id="9dcb4-107">*lecteur*. *currentMedia*. sourceURL</span><span class="sxs-lookup"><span data-stu-id="9dcb4-107">*player*.*currentMedia*.sourceURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="9dcb4-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9dcb4-108">Possible Values</span></span>

<span data-ttu-id="9dcb4-109">Cette propriété est une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-109">This property is a read-only **String**.</span></span>

## <a name="examples"></a><span data-ttu-id="9dcb4-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="9dcb4-110">Examples</span></span>

<span data-ttu-id="9dcb4-111">L’exemple JScript suivant utilise un *média*. **sourceURL** pour récupérer l’URL du premier élément multimédia dans l’exemple de sélection ; l’URL de l’élément multimédia est ensuite affectée à la propriété **URL** de l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-111">The following JScript example uses *Media*.**sourceURL** to retrieve the URL of the first media item in the sample playlist; the URL of the media item is then assigned to the player object **URL** property.</span></span> <span data-ttu-id="9dcb4-112">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9dcb4-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="9dcb4-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dcb4-113">Requirements</span></span>



| <span data-ttu-id="9dcb4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9dcb4-114">Requirement</span></span> | <span data-ttu-id="9dcb4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dcb4-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9dcb4-116">Version</span><span class="sxs-lookup"><span data-stu-id="9dcb4-116">Version</span></span><br/> | <span data-ttu-id="9dcb4-117">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9dcb4-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9dcb4-118">DLL</span><span class="sxs-lookup"><span data-stu-id="9dcb4-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="9dcb4-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dcb4-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dcb4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dcb4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dcb4-121">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="9dcb4-121">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





