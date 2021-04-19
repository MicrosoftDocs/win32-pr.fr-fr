---
title: PlaylistArray. Item, méthode
description: La méthode Item récupère la sélection à l’index donné.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- méthode Item lecteur Windows Media
- méthode Item lecteur Windows Media, classe PlaylistArray
- Classe PlaylistArray lecteur Windows Media, méthode Item
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6144f6e1cfda93be32060e8206a96b0da7568d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537788"
---
# <a name="playlistarrayitem-method"></a><span data-ttu-id="9bde8-106">PlaylistArray. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="9bde8-106">PlaylistArray.item method</span></span>

<span data-ttu-id="9bde8-107">La méthode **Item** récupère la sélection à l’index donné.</span><span class="sxs-lookup"><span data-stu-id="9bde8-107">The **item** method retrieves the playlist at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bde8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9bde8-108">Syntax</span></span>


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="9bde8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9bde8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bde8-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9bde8-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bde8-111">**Nombre** (**long**) contenant l’index de la sélection à récupérer.</span><span class="sxs-lookup"><span data-stu-id="9bde8-111">**Number** (**long**) containing the index of the playlist to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bde8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9bde8-112">Return value</span></span>

<span data-ttu-id="9bde8-113">Cette méthode retourne un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="9bde8-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bde8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9bde8-114">Remarks</span></span>

<span data-ttu-id="9bde8-115">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="9bde8-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="9bde8-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9bde8-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9bde8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bde8-117">Requirements</span></span>



| <span data-ttu-id="9bde8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9bde8-118">Requirement</span></span> | <span data-ttu-id="9bde8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bde8-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9bde8-120">Version</span><span class="sxs-lookup"><span data-stu-id="9bde8-120">Version</span></span><br/> | <span data-ttu-id="9bde8-121">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9bde8-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9bde8-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9bde8-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="9bde8-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bde8-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bde8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bde8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bde8-125">**Objet PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="9bde8-125">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="9bde8-126">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="9bde8-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="9bde8-127">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="9bde8-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





