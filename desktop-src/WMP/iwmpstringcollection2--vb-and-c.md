---
title: Interface IWMPStringCollection2 (VB et C) (WMP. h)
description: Fournit des méthodes qui complètent l’interface IWMPStringCollection.
ms.assetid: be93ff47-7f76-4b5e-ad30-3094a75147c8
keywords:
- IWMPStringCollection2 (VB et C) interface Windows Media Player
- Interface IWMPStringCollection2 (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPStringCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184e1a16ea0e6b33cc5b67eaeac6b050e5cda97a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520979"
---
# <a name="iwmpstringcollection2-vb-and-c-interface"></a><span data-ttu-id="979af-105">Interface IWMPStringCollection2 (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="979af-105">IWMPStringCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="979af-106">Fournit des méthodes qui complètent l’interface **IWMPStringCollection** .</span><span class="sxs-lookup"><span data-stu-id="979af-106">Provides methods that supplement the **IWMPStringCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="979af-107">Membres</span><span class="sxs-lookup"><span data-stu-id="979af-107">Members</span></span>

<span data-ttu-id="979af-108">L’interface **IWMPStringCollection2 (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="979af-108">The **IWMPStringCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="979af-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="979af-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="979af-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="979af-110">Methods</span></span>

<span data-ttu-id="979af-111">L’interface **IWMPStringCollection2 (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="979af-111">The **IWMPStringCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="979af-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="979af-112">Method</span></span>                                                                                                                 | <span data-ttu-id="979af-113">Description</span><span class="sxs-lookup"><span data-stu-id="979af-113">Description</span></span>                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="979af-114">**getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="979af-114">**getAttributeCountByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="979af-115">Retourne le nombre d’attributs associés à l’index d’élément de collection de chaînes, au nom d’attribut et à la langue spécifiés.</span><span class="sxs-lookup"><span data-stu-id="979af-115">Returns the number of attributes associated with the specified string collection item index, attribute name, and language.</span></span><br/> |
| [<span data-ttu-id="979af-116">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="979af-116">**getItemInfo**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)                         | <span data-ttu-id="979af-117">Retourne la chaîne correspondant au nom et à l’index de l’élément de collection de chaînes spécifié.</span><span class="sxs-lookup"><span data-stu-id="979af-117">Returns the string corresponding to the specified string collection item index and name.</span></span><br/>                                   |
| [<span data-ttu-id="979af-118">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="979af-118">**getItemInfoByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="979af-119">Retourne la valeur correspondant à l’index de l’élément de collection de chaînes, au nom, à la langue et à l’index d’attributs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="979af-119">Returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span><br/>        |
| [<span data-ttu-id="979af-120">**isIdentical**</span><span class="sxs-lookup"><span data-stu-id="979af-120">**isIdentical**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-isidentical--vb-and-c.md)                         | <span data-ttu-id="979af-121">Retourne une valeur indiquant si l’objet fourni est identique à l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="979af-121">Returns a value indicating whether the supplied object is the same as the current one.</span></span><br/>                                     |



 

<span data-ttu-id="979af-122">Obtient une interface **IWMPStringCollection2** en effectuant un cast de la valeur retournée par la méthode [**IWMPMediaCollection. getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) .</span><span class="sxs-lookup"><span data-stu-id="979af-122">Get an **IWMPStringCollection2** interface by casting the value returned by the [**IWMPMediaCollection.getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="979af-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="979af-123">Requirements</span></span>



| <span data-ttu-id="979af-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="979af-124">Requirement</span></span> | <span data-ttu-id="979af-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="979af-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="979af-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="979af-126">Header</span></span><br/> | <dl> <span data-ttu-id="979af-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="979af-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="979af-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="979af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="979af-129">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="979af-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="979af-130">**Interface IWMPStringCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="979af-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





