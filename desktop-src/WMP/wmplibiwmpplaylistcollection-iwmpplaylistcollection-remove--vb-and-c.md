---
title: IWMPPlaylistCollection méthode Remove
description: La méthode Remove supprime une sélection de la bibliothèque. | IWMPPlaylistCollection méthode Remove
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- Méthode Remove Windows Media Player
- Remove, méthode lecteur Windows Media, interface IWMPPlaylistCollection
- Interface IWMPPlaylistCollection lecteur Windows Media, méthode Remove
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99fbaa2f60c769599bd6173b8e38f4d99e9f42d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525677"
---
# <a name="iwmpplaylistcollectionremove-method"></a><span data-ttu-id="baccd-107">IWMPPlaylistCollection :: Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="baccd-107">IWMPPlaylistCollection::remove method</span></span>

<span data-ttu-id="baccd-108">La méthode **Remove** supprime une sélection de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="baccd-108">The **remove** method removes a playlist from the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="baccd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="baccd-109">Syntax</span></span>


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="baccd-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="baccd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baccd-111">*pItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="baccd-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baccd-112">Une interface **wmplib. IWMPPlaylist** pour la sélection que cette méthode supprimera.</span><span class="sxs-lookup"><span data-stu-id="baccd-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baccd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="baccd-113">Return value</span></span>

<span data-ttu-id="baccd-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="baccd-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="baccd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="baccd-115">Remarks</span></span>

<span data-ttu-id="baccd-116">Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="baccd-116">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="baccd-117">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="baccd-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="baccd-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="baccd-118">Requirements</span></span>



| <span data-ttu-id="baccd-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="baccd-119">Requirement</span></span> | <span data-ttu-id="baccd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="baccd-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baccd-121">Version</span><span class="sxs-lookup"><span data-stu-id="baccd-121">Version</span></span><br/>   | <span data-ttu-id="baccd-122">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="baccd-122">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="baccd-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="baccd-123">Namespace</span></span><br/> | <span data-ttu-id="baccd-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="baccd-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="baccd-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="baccd-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="baccd-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="baccd-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baccd-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baccd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baccd-128">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="baccd-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="baccd-129">**Interface IWMPPlaylistCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="baccd-129">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





