---
title: Propriété Count IWMPPlaylist
description: La propriété Count obtient le nombre d’éléments multimédias dans une sélection.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- propriété Count Windows Media Player
- propriété Count lecteur Windows Media, interface IWMPPlaylist
- IWMPPlaylist interface Windows Media Player, propriété Count
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d988fefc436b65652d2b0765320ca289417c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541355"
---
# <a name="iwmpplaylistcount-property"></a><span data-ttu-id="318af-106">IWMPPlaylist :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="318af-106">IWMPPlaylist::count property</span></span>

<span data-ttu-id="318af-107">La propriété **Count** obtient le nombre d’éléments multimédias dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="318af-107">The **count** property gets the number of media items in a playlist.</span></span>

<span data-ttu-id="318af-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="318af-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="318af-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="318af-109">Syntax</span></span>


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="318af-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="318af-110">Property value</span></span>

<span data-ttu-id="318af-111">**System. Int32** qui correspond au nombre d’éléments multimédias dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="318af-111">A **System.Int32** that is the number of media items in the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="318af-112">Notes</span><span class="sxs-lookup"><span data-stu-id="318af-112">Remarks</span></span>

<span data-ttu-id="318af-113">Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="318af-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="318af-114">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="318af-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="318af-115">Consultez la propriété [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) pour obtenir un exemple de code qui utilise cette propriété.</span><span class="sxs-lookup"><span data-stu-id="318af-115">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="318af-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="318af-116">Requirements</span></span>



| <span data-ttu-id="318af-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="318af-117">Requirement</span></span> | <span data-ttu-id="318af-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="318af-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="318af-119">Version</span><span class="sxs-lookup"><span data-stu-id="318af-119">Version</span></span><br/>   | <span data-ttu-id="318af-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="318af-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="318af-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="318af-121">Namespace</span></span><br/> | <span data-ttu-id="318af-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="318af-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="318af-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="318af-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="318af-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="318af-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="318af-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="318af-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="318af-126">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="318af-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





