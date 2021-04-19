---
title: IWMPPlaylist insertItem, méthode
description: La méthode insertItem insère un élément multimédia à un emplacement spécifié dans une sélection.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- méthode insertItem Windows Media Player
- méthode insertItem lecteur Windows Media, interface IWMPPlaylist
- IWMPPlaylist interface Windows Media Player, insertItem, méthode
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ef167a5f3931f34d4cd6fb91b3d044affb9484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525575"
---
# <a name="iwmpplaylistinsertitem-method"></a><span data-ttu-id="48fc5-106">IWMPPlaylist :: insertItem, méthode</span><span class="sxs-lookup"><span data-stu-id="48fc5-106">IWMPPlaylist::insertItem method</span></span>

<span data-ttu-id="48fc5-107">La méthode **InsertItem** insère un élément multimédia à un emplacement spécifié dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="48fc5-107">The **insertItem** method inserts a media item at a specified location in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="48fc5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48fc5-108">Syntax</span></span>


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a><span data-ttu-id="48fc5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48fc5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48fc5-110">*Lindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="48fc5-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48fc5-111">**System. Int32** qui est l’index de base zéro au niveau duquel l’élément multimédia est inséré dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="48fc5-111">A **System.Int32** that is the zero-based index at which the media item will be inserted in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="48fc5-112">*pIWMPMedia* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="48fc5-112">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48fc5-113">Interface **wmplib. IWMPMedia** qui représente l’élément multimédia à insérer.</span><span class="sxs-lookup"><span data-stu-id="48fc5-113">A **WMPLib.IWMPMedia** interface that represents the media item to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48fc5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48fc5-114">Return value</span></span>

<span data-ttu-id="48fc5-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="48fc5-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48fc5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="48fc5-116">Remarks</span></span>

<span data-ttu-id="48fc5-117">Tous les éléments multimédias après l’élément inséré auront leurs index augmentés d’une unité.</span><span class="sxs-lookup"><span data-stu-id="48fc5-117">All media items after the inserted item will have their indexes increased by one.</span></span>

<span data-ttu-id="48fc5-118">Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="48fc5-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="48fc5-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="48fc5-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48fc5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48fc5-120">Requirements</span></span>



| <span data-ttu-id="48fc5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48fc5-121">Requirement</span></span> | <span data-ttu-id="48fc5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="48fc5-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48fc5-123">Version</span><span class="sxs-lookup"><span data-stu-id="48fc5-123">Version</span></span><br/>   | <span data-ttu-id="48fc5-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="48fc5-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="48fc5-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="48fc5-125">Namespace</span></span><br/> | <span data-ttu-id="48fc5-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="48fc5-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="48fc5-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="48fc5-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="48fc5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="48fc5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48fc5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48fc5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48fc5-130">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="48fc5-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="48fc5-131">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="48fc5-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="48fc5-132">**IWMPPlaylist. removeItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="48fc5-132">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





