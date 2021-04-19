---
title: Méthode d’élément IWMPStringCollection
description: La méthode Item retourne la chaîne à l’index spécifié.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Méthode Item lecteur Windows Media
- Méthode Item lecteur Windows Media, interface IWMPStringCollection
- Interface IWMPStringCollection lecteur Windows Media, méthode d’élément
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69bdc63448699a595238b9907f4b1253209ad06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537088"
---
# <a name="iwmpstringcollectionitem-method"></a><span data-ttu-id="c9cd5-106">IWMPStringCollection :: Item, méthode</span><span class="sxs-lookup"><span data-stu-id="c9cd5-106">IWMPStringCollection::Item method</span></span>

<span data-ttu-id="c9cd5-107">La méthode **Item** retourne la chaîne à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="c9cd5-107">The **Item** method returns the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9cd5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9cd5-108">Syntax</span></span>


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="c9cd5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9cd5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9cd5-110">*Lindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9cd5-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9cd5-111">**System. Int32** qui est l’index.</span><span class="sxs-lookup"><span data-stu-id="c9cd5-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9cd5-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9cd5-112">Return value</span></span>

<span data-ttu-id="c9cd5-113">**System. String** qui est la chaîne à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="c9cd5-113">A **System.String** that is the string at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9cd5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c9cd5-114">Remarks</span></span>

<span data-ttu-id="c9cd5-115">L’interface **IWMPStringCollection** est utilisée pour récupérer l’ensemble de valeurs disponibles pour un attribut.</span><span class="sxs-lookup"><span data-stu-id="c9cd5-115">The **IWMPStringCollection** interface is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="c9cd5-116">Par exemple, la méthode **IWMPMediaCollection. getAttributeStringCollection** peut être utilisée pour récupérer une interface **IWMPStringCollection** représentant toutes les valeurs de l’attribut genre dans le type de média audio.</span><span class="sxs-lookup"><span data-stu-id="c9cd5-116">For example, the **IWMPMediaCollection.getAttributeStringCollection** method can be used to retrieve an **IWMPStringCollection** interface representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="c9cd5-117">La méthode **Item** peut ensuite être utilisée pour itérer au sein de toutes les valeurs possibles de l’attribut genre.</span><span class="sxs-lookup"><span data-stu-id="c9cd5-117">The **Item** method can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="c9cd5-118">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="c9cd5-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="c9cd5-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c9cd5-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9cd5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9cd5-120">Requirements</span></span>



| <span data-ttu-id="c9cd5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9cd5-121">Requirement</span></span> | <span data-ttu-id="c9cd5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9cd5-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9cd5-123">Version</span><span class="sxs-lookup"><span data-stu-id="c9cd5-123">Version</span></span><br/>   | <span data-ttu-id="c9cd5-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c9cd5-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c9cd5-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c9cd5-125">Namespace</span></span><br/> | <span data-ttu-id="c9cd5-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c9cd5-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c9cd5-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="c9cd5-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c9cd5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c9cd5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9cd5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9cd5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9cd5-130">**IWMPMediaCollection. getAttributeStringCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c9cd5-130">**IWMPMediaCollection.getAttributeStringCollection (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9cd5-131">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c9cd5-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9cd5-132">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c9cd5-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9cd5-133">**Interface IWMPStringCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c9cd5-133">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





