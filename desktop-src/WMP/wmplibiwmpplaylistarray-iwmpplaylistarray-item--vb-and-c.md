---
title: Méthode d’élément IWMPPlaylistArray
description: La méthode Item retourne une interface IWMPPlaylist représentant la sélection à l’index spécifié.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Méthode Item lecteur Windows Media
- Méthode Item lecteur Windows Media, interface IWMPPlaylistArray
- Interface IWMPPlaylistArray lecteur Windows Media, méthode d’élément
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660e919ef51bbb9584971f25bdf92296d331de23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539945"
---
# <a name="iwmpplaylistarrayitem-method"></a><span data-ttu-id="a4905-106">IWMPPlaylistArray :: Item, méthode</span><span class="sxs-lookup"><span data-stu-id="a4905-106">IWMPPlaylistArray::Item method</span></span>

<span data-ttu-id="a4905-107">La méthode **Item** retourne une interface **IWMPPlaylist** représentant la sélection à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="a4905-107">The **Item** method returns an **IWMPPlaylist** interface representing the playlist at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4905-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4905-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a><span data-ttu-id="a4905-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4905-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4905-110">*Lindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4905-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4905-111">**System. Int32** contenant l’index qui identifie la sélection que la méthode doit récupérer.</span><span class="sxs-lookup"><span data-stu-id="a4905-111">A **System.Int32** containing the index that identifies the playlist that the method should retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4905-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4905-112">Return value</span></span>

<span data-ttu-id="a4905-113">Interface **wmplib. IWMPPlaylist** pour la sélection récupérée.</span><span class="sxs-lookup"><span data-stu-id="a4905-113">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4905-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a4905-114">Remarks</span></span>

<span data-ttu-id="a4905-115">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="a4905-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="a4905-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a4905-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4905-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4905-117">Requirements</span></span>



| <span data-ttu-id="a4905-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4905-118">Requirement</span></span> | <span data-ttu-id="a4905-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4905-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4905-120">Version</span><span class="sxs-lookup"><span data-stu-id="a4905-120">Version</span></span><br/>   | <span data-ttu-id="a4905-121">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a4905-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="a4905-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a4905-122">Namespace</span></span><br/> | <span data-ttu-id="a4905-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a4905-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a4905-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="a4905-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a4905-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a4905-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4905-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4905-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4905-127">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a4905-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4905-128">**Interface IWMPPlaylistArray (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="a4905-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





