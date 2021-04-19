---
title: Méthode playlist. moveItem
description: La méthode moveItem modifie l’emplacement d’un élément dans la sélection.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- méthode moveItem lecteur Windows Media
- méthode moveItem lecteur Windows Media, classe de sélection
- Classe de sélection lecteur Windows Media, méthode moveItem
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537659"
---
# <a name="playlistmoveitem-method"></a><span data-ttu-id="b3645-106">Méthode playlist. moveItem</span><span class="sxs-lookup"><span data-stu-id="b3645-106">Playlist.moveItem method</span></span>

<span data-ttu-id="b3645-107">La méthode **moveItem** modifie l’emplacement d’un élément dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="b3645-107">The **moveItem** method changes the location of an item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3645-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3645-108">Syntax</span></span>


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a><span data-ttu-id="b3645-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3645-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3645-110">*OldIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3645-110">*oldIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3645-111">**Nombre** (**long**) contenant l’ancien index.</span><span class="sxs-lookup"><span data-stu-id="b3645-111">**Number** (**long**) containing the old index.</span></span>

</dd> <dt>

<span data-ttu-id="b3645-112">*NewIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3645-112">*newIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3645-113">**Nombre** (**long**) contenant le nouvel index.</span><span class="sxs-lookup"><span data-stu-id="b3645-113">**Number** (**long**) containing the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3645-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3645-114">Return value</span></span>

<span data-ttu-id="b3645-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b3645-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3645-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b3645-116">Remarks</span></span>

<span data-ttu-id="b3645-117">Les sélections stockées dans la bibliothèque peuvent changer en dehors de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="b3645-117">Playlists stored in the library can change outside your control.</span></span> <span data-ttu-id="b3645-118">Veillez à surveiller et à gérer tous les événements appropriés liés à la sélection afin que l’ordre des éléments dans la sélection ne change pas de manière inattendue.</span><span class="sxs-lookup"><span data-stu-id="b3645-118">Be sure to monitor and handle all appropriate playlist-related events so that the order of items in the playlist does not change unexpectedly.</span></span>

<span data-ttu-id="b3645-119">Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="b3645-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="b3645-120">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b3645-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3645-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3645-121">Requirements</span></span>



| <span data-ttu-id="b3645-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3645-122">Requirement</span></span> | <span data-ttu-id="b3645-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3645-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3645-124">Version</span><span class="sxs-lookup"><span data-stu-id="b3645-124">Version</span></span><br/> | <span data-ttu-id="b3645-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b3645-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b3645-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b3645-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="b3645-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3645-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3645-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3645-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3645-129">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="b3645-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="b3645-130">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b3645-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b3645-131">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b3645-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





