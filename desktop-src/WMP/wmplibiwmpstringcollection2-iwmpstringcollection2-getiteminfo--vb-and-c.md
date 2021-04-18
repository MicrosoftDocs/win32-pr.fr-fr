---
title: Méthode IWMPStringCollection2 getItemInfo
description: La méthode getItemInfo retourne la chaîne correspondant à l’index et au nom d’élément de collection de chaînes spécifiés.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo lecteur Windows Media, interface IWMPStringCollection2
- Interface IWMPStringCollection2 lecteur Windows Media, méthode getItemInfo
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4741c4a3ba74b03038974d8b66bc42c23830ebb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540637"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a><span data-ttu-id="53372-106">IWMPStringCollection2 :: getItemInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="53372-106">IWMPStringCollection2::getItemInfo method</span></span>

<span data-ttu-id="53372-107">La méthode **getItemInfo** retourne la chaîne correspondant à l’index et au nom d’élément de collection de chaînes spécifiés.</span><span class="sxs-lookup"><span data-stu-id="53372-107">The **getItemInfo** method returns the string corresponding to the specified string collection item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="53372-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53372-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="53372-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53372-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53372-110">*lCollectionIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53372-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53372-111">**System. Int32** spécifiant l’index de base zéro de l’élément de collection de chaînes à partir duquel l’attribut doit être obtenu.</span><span class="sxs-lookup"><span data-stu-id="53372-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="53372-112">*bstrItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53372-112">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53372-113">**System. String** qui est le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="53372-113">The **System.String** that is the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53372-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53372-114">Return value</span></span>

<span data-ttu-id="53372-115">**System. String** qui est le nom de l’élément de collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="53372-115">The **System.String** that is the name of the string collection item.</span></span> <span data-ttu-id="53372-116">Pour les attributs dont la valeur sous-jacente est **System. Boolean**, la chaîne « true » ou « false » est retournée.</span><span class="sxs-lookup"><span data-stu-id="53372-116">For attributes whose underlying value is **System.Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="53372-117">Notes</span><span class="sxs-lookup"><span data-stu-id="53372-117">Remarks</span></span>

<span data-ttu-id="53372-118">Pour récupérer des attributs avec plusieurs valeurs et attributs avec des valeurs complexes, utilisez la méthode **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="53372-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="53372-119">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="53372-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="53372-120">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="53372-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53372-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53372-121">Requirements</span></span>



| <span data-ttu-id="53372-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53372-122">Requirement</span></span> | <span data-ttu-id="53372-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="53372-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53372-124">Version</span><span class="sxs-lookup"><span data-stu-id="53372-124">Version</span></span><br/>   | <span data-ttu-id="53372-125">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="53372-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="53372-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="53372-126">Namespace</span></span><br/> | <span data-ttu-id="53372-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="53372-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="53372-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="53372-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="53372-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="53372-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53372-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53372-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53372-131">**Interface IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="53372-131">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="53372-132">**IWMPStringCollection2. getItemInfoByType (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="53372-132">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





