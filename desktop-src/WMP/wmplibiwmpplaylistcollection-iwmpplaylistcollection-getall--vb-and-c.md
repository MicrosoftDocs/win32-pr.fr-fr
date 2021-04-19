---
title: IWMPPlaylistCollection getAll, méthode
description: La méthode getAll retourne une interface IWMPPlaylistArray qui fournit l’accès à toutes les playlists de la bibliothèque.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- méthode getAll lecteur Windows Media
- méthode getAll lecteur Windows Media, interface IWMPPlaylistCollection
- IWMPPlaylistCollection interface Windows Media Player, getAll, méthode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4260f5c960650cf6c04a1dd8b39d887f711fb8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539944"
---
# <a name="iwmpplaylistcollectiongetall-method"></a><span data-ttu-id="8459f-106">IWMPPlaylistCollection :: getAll, méthode</span><span class="sxs-lookup"><span data-stu-id="8459f-106">IWMPPlaylistCollection::getAll method</span></span>

<span data-ttu-id="8459f-107">La méthode **GetAll** retourne une interface **IWMPPlaylistArray** qui fournit l’accès à toutes les playlists de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="8459f-107">The **getAll** method returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="8459f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8459f-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="8459f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8459f-109">Parameters</span></span>

<span data-ttu-id="8459f-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8459f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8459f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8459f-111">Return value</span></span>

<span data-ttu-id="8459f-112">Interface **wmplib. IWMPPlaylistArray** pour le tableau de sélections récupéré.</span><span class="sxs-lookup"><span data-stu-id="8459f-112">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="8459f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8459f-113">Remarks</span></span>

<span data-ttu-id="8459f-114">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="8459f-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="8459f-115">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8459f-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8459f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8459f-116">Requirements</span></span>



| <span data-ttu-id="8459f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8459f-117">Requirement</span></span> | <span data-ttu-id="8459f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8459f-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8459f-119">Version</span><span class="sxs-lookup"><span data-stu-id="8459f-119">Version</span></span><br/>   | <span data-ttu-id="8459f-120">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8459f-120">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="8459f-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8459f-121">Namespace</span></span><br/> | <span data-ttu-id="8459f-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8459f-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8459f-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="8459f-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8459f-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8459f-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8459f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8459f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8459f-126">**Interface IWMPPlaylistArray (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8459f-126">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8459f-127">**Interface IWMPPlaylistCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8459f-127">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





