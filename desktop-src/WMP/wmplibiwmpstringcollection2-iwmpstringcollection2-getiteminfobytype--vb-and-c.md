---
title: Méthode IWMPStringCollection2 getItemInfobyType
description: La méthode getItemInfoByType retourne la valeur correspondant à l’index de l’élément de collection de chaînes, au nom, à la langue et à l’index d’attributs spécifiés.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- méthode getItemInfobyType lecteur Windows Media
- méthode getItemInfobyType lecteur Windows Media, interface IWMPStringCollection2
- Interface IWMPStringCollection2 lecteur Windows Media, méthode getItemInfobyType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541457"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a><span data-ttu-id="fcf18-106">IWMPStringCollection2 :: getItemInfobyType, méthode</span><span class="sxs-lookup"><span data-stu-id="fcf18-106">IWMPStringCollection2::getItemInfobyType method</span></span>

<span data-ttu-id="fcf18-107">La méthode **getItemInfoByType** retourne la valeur correspondant à l’index de l’élément de collection de chaînes, au nom, à la langue et à l’index d’attributs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fcf18-107">The **getItemInfoByType** method returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcf18-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcf18-108">Syntax</span></span>


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a><span data-ttu-id="fcf18-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcf18-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcf18-110">*lCollectionIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcf18-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf18-111">**System. Int32** qui est l’index de base zéro de l’élément de collection de chaînes à partir duquel l’attribut doit être obtenu.</span><span class="sxs-lookup"><span data-stu-id="fcf18-111">The **System.Int32** that is the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="fcf18-112">*bstrType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcf18-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf18-113">**System. String** qui est le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="fcf18-113">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="fcf18-114">*bstrLanguage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcf18-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf18-115">**System. String** qui indique la langue.</span><span class="sxs-lookup"><span data-stu-id="fcf18-115">The **System.String** that indicates the language.</span></span> <span data-ttu-id="fcf18-116">Si la valeur est définie sur null ou sur une chaîne de longueur nulle (""), la chaîne de paramètres régionaux active est utilisée.</span><span class="sxs-lookup"><span data-stu-id="fcf18-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="fcf18-117">Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».</span><span class="sxs-lookup"><span data-stu-id="fcf18-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="fcf18-118">*lAttributeIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fcf18-118">*lAttributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcf18-119">**System. Int32** qui correspond à l’index de base zéro de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="fcf18-119">A **System.Int32** that is the zero-based index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcf18-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fcf18-120">Return value</span></span>

<span data-ttu-id="fcf18-121">**System. Object** qui est l’élément de collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="fcf18-121">A **System.Object** that is the string collection item.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcf18-122">Notes</span><span class="sxs-lookup"><span data-stu-id="fcf18-122">Remarks</span></span>

<span data-ttu-id="fcf18-123">Cette méthode prend en charge des attributs avec plusieurs valeurs et attributs avec des valeurs complexes.</span><span class="sxs-lookup"><span data-stu-id="fcf18-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="fcf18-124">La méthode **getItemInfo** ne prend pas en charge les attributs avec plusieurs valeurs ou attributs avec des valeurs complexes.</span><span class="sxs-lookup"><span data-stu-id="fcf18-124">The **getItemInfo** method does not support attributes with multiple values or attributes with complex values.</span></span>

<span data-ttu-id="fcf18-125">En passant la valeur « ChildList » dans le paramètre *bstrType* , vous pouvez récupérer une nouvelle collection de chaînes qui contient les enfants de l’un des éléments de la collection de chaînes parente.</span><span class="sxs-lookup"><span data-stu-id="fcf18-125">By passing the value "ChildList" in the *bstrType* parameter, you can retrieve a new string collection that contains the children of one of the items in the parent string collection.</span></span> <span data-ttu-id="fcf18-126">Par exemple, si la collection parente contient une liste de AlbumIDs, vous pouvez utiliser cette méthode pour obtenir une collection de chaînes enfant qui contient toutes les pistes de l’un des albums.</span><span class="sxs-lookup"><span data-stu-id="fcf18-126">For instance, if the parent collection contains a list of AlbumIDs, you can use this method to obtain a child string collection that contains all the tracks for one of the albums.</span></span> <span data-ttu-id="fcf18-127">Cette approche est plus rapide et plus efficace que l’appel de la méthode **IWMPMediaCollection2. getStringCollectionByQuery** à deux reprises. une fois pour obtenir une collection de AlbumIDs et une deuxième fois pour obtenir une collection de pistes pour un AlbumID particulier.</span><span class="sxs-lookup"><span data-stu-id="fcf18-127">This approach is faster and more efficient than calling the **IWMPMediaCollection2.getStringCollectionByQuery** method twice; once to get a collection of AlbumIDs, and a second time to get a collection of tracks for a particular AlbumID.</span></span> <span data-ttu-id="fcf18-128">Pour utiliser ChildList de la manière décrite ci-dessus, la collection de chaînes parent doit être obtenue à partir d’une collection de médias via **IWMPLibraryServices**, et non à l’aide de la propriété **AxWindowsMediaPlayer. mediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="fcf18-128">To use ChildList in the way just described, the parent string collection must be obtained from a media collection through **IWMPLibraryServices**, and not by using the **AxWindowsMediaPlayer.mediaCollection** property.</span></span>

<span data-ttu-id="fcf18-129">Lorsque vous utilisez ChildList, transmettez la valeur « ChildList » dans le paramètre *bstrType* et la valeur 0 dans le paramètre *lAttributeIndex* .</span><span class="sxs-lookup"><span data-stu-id="fcf18-129">When using ChildList, pass the value "ChildList" in the *bstrType* parameter, and the value 0 in the *lAttributeIndex* parameter.</span></span> <span data-ttu-id="fcf18-130">Vous pouvez ensuite effectuer un cast de l’objet qui est retourné à une interface **IWMPStringCollection2** pour accéder à la liste enfant.</span><span class="sxs-lookup"><span data-stu-id="fcf18-130">You can then cast the object that is returned to an **IWMPStringCollection2** interface to access the child list.</span></span>

<span data-ttu-id="fcf18-131">Pour utiliser cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="fcf18-131">To use this method, you must have read access to the library.</span></span> <span data-ttu-id="fcf18-132">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fcf18-132">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcf18-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcf18-133">Requirements</span></span>



| <span data-ttu-id="fcf18-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcf18-134">Requirement</span></span> | <span data-ttu-id="fcf18-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcf18-135">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf18-136">Version</span><span class="sxs-lookup"><span data-stu-id="fcf18-136">Version</span></span><br/>   | <span data-ttu-id="fcf18-137">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="fcf18-137">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="fcf18-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fcf18-138">Namespace</span></span><br/> | <span data-ttu-id="fcf18-139">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fcf18-139">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fcf18-140">Assembly</span><span class="sxs-lookup"><span data-stu-id="fcf18-140">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fcf18-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fcf18-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcf18-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcf18-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcf18-143">**Attribut AlbumID**</span><span class="sxs-lookup"><span data-stu-id="fcf18-143">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="fcf18-144">**Interface IWMPLibraryServices (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fcf18-144">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fcf18-145">**IWMPMediaCollection2. getStringCollectionByQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fcf18-145">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fcf18-146">**Interface IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="fcf18-146">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fcf18-147">**IWMPStringCollection2. getItemInfo (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="fcf18-147">**IWMPStringCollection2.getItemInfo (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





