---
title: PlaylistCollection. isDeleted, méthode
description: La méthode isDeleted récupère une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- isDeleted, méthode Windows Media Player
- isDeleted, méthode lecteur Windows Media, classe PlaylistCollection
- Classe PlaylistCollection lecteur Windows Media, méthode isDeleted
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545536"
---
# <a name="playlistcollectionisdeleted-method"></a><span data-ttu-id="dbd13-106">PlaylistCollection. isDeleted, méthode</span><span class="sxs-lookup"><span data-stu-id="dbd13-106">PlaylistCollection.isDeleted method</span></span>

<span data-ttu-id="dbd13-107">La méthode **IsDeleted** récupère une valeur indiquant si la sélection spécifiée se trouve dans le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="dbd13-107">The **isDeleted** method retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbd13-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbd13-108">Syntax</span></span>


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="dbd13-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbd13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbd13-110">*sélection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dbd13-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbd13-111">Objet de la **sélection** à rechercher.</span><span class="sxs-lookup"><span data-stu-id="dbd13-111">The **Playlist** object to be searched for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbd13-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbd13-112">Return value</span></span>

<span data-ttu-id="dbd13-113">Cette méthode retourne une **valeur booléenne**.</span><span class="sxs-lookup"><span data-stu-id="dbd13-113">This method returns a **Boolean**.</span></span>

<span data-ttu-id="dbd13-114">**Windows Media Player 10 Mobile**: cette méthode retourne toujours la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="dbd13-114">**Windows Media Player 10 Mobile**: This method always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbd13-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbd13-115">Requirements</span></span>



| <span data-ttu-id="dbd13-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbd13-116">Requirement</span></span> | <span data-ttu-id="dbd13-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbd13-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbd13-118">Version</span><span class="sxs-lookup"><span data-stu-id="dbd13-118">Version</span></span><br/> | <span data-ttu-id="dbd13-119">Lecteur Windows Media version 7,0, lecteur Windows Media version 7,1 ou lecteur Windows Media pour Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dbd13-119">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="dbd13-120">Cette méthode n’est pas prise en charge pour le lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="dbd13-120">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="dbd13-121">DLL</span><span class="sxs-lookup"><span data-stu-id="dbd13-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="dbd13-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbd13-122"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="dbd13-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbd13-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbd13-124">**Objet PlaylistCollection**</span><span class="sxs-lookup"><span data-stu-id="dbd13-124">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 





