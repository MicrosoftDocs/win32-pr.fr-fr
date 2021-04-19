---
title: IWMPPlaylist. attributeName (VB et C)
description: La propriété attributeName (la \_ méthode obtenir AttributeName dans C \) obtient le nom d’un attribut playlist spécifié par un index.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- IWMPPlaylist. attributeName (VB et C) lecteur Windows Media
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529660"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a><span data-ttu-id="98e41-104">IWMPPlaylist. attributeName (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="98e41-104">IWMPPlaylist.attributeName (VB and C#)</span></span>

<span data-ttu-id="98e41-105">La propriété **AttributeName** (la méthode **obtenir \_ AttributeName** en C#) obtient le nom d’un attribut playlist spécifié par un index.</span><span class="sxs-lookup"><span data-stu-id="98e41-105">The **attributeName** property (the **get\_attributeName** method in C#) gets the name of a playlist attribute specified by an index.</span></span>


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a><span data-ttu-id="98e41-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98e41-106">Parameters</span></span>

<span data-ttu-id="98e41-107">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="98e41-107">*lIndex*</span></span>

<span data-ttu-id="98e41-108">**System. Int32** qui est l’index de l’attribut playlist.</span><span class="sxs-lookup"><span data-stu-id="98e41-108">A **System.Int32** that is the index of the playlist attribute.</span></span>

## <a name="return-value"></a><span data-ttu-id="98e41-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="98e41-109">Return Value</span></span>

<span data-ttu-id="98e41-110">**System. String** qui est le nom de l’attribut playlist.</span><span class="sxs-lookup"><span data-stu-id="98e41-110">A **System.String** that is the name of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e41-111">Notes</span><span class="sxs-lookup"><span data-stu-id="98e41-111">Remarks</span></span>

<span data-ttu-id="98e41-112">**IWMPPlaylist. AttributeName** est une propriété en lecture seule dans Visual Basic qui accepte un paramètre, tandis que en C#, elle est appelée méthode **IWMPPlaylist. obtenir \_ AttributeName** .</span><span class="sxs-lookup"><span data-stu-id="98e41-112">**IWMPPlaylist.attributeName** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_attributeName** method.</span></span>

<span data-ttu-id="98e41-113">Le nombre d’attributs associés à une sélection est retourné par la propriété **IWMPPlaylist. attributeCount** .</span><span class="sxs-lookup"><span data-stu-id="98e41-113">The number of attributes associated with a playlist is returned by the **IWMPPlaylist.attributeCount** property.</span></span>

<span data-ttu-id="98e41-114">Le nom retourné par cette propriété peut être fourni aux méthodes **setItemInfo** ou **getItemInfo** pour spécifier ou récupérer une valeur pour l’attribut nommé.</span><span class="sxs-lookup"><span data-stu-id="98e41-114">The name returned by this property can be supplied to the **setItemInfo** or **getItemInfo** methods to specify or retrieve a value for the named attribute.</span></span>

<span data-ttu-id="98e41-115">Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="98e41-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="98e41-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="98e41-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="98e41-117">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence des attributs](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="98e41-117">For more information about attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="98e41-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="98e41-118">Examples</span></span>

<span data-ttu-id="98e41-119">Consultez la propriété [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) pour obtenir un exemple de code qui utilise cette propriété.</span><span class="sxs-lookup"><span data-stu-id="98e41-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e41-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98e41-120">Requirements</span></span>



| <span data-ttu-id="98e41-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98e41-121">Requirement</span></span> | <span data-ttu-id="98e41-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="98e41-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e41-123">Version</span><span class="sxs-lookup"><span data-stu-id="98e41-123">Version</span></span><br/>   | <span data-ttu-id="98e41-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="98e41-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="98e41-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="98e41-125">Namespace</span></span><br/> | <span data-ttu-id="98e41-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="98e41-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="98e41-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="98e41-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="98e41-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="98e41-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e41-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98e41-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e41-130">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="98e41-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98e41-131">**IWMPPlaylist. attributeCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="98e41-131">**IWMPPlaylist.attributeCount (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98e41-132">**IWMPPlaylist. getItemInfo (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="98e41-132">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98e41-133">**IWMPPlaylist. setItemInfo (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="98e41-133">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





