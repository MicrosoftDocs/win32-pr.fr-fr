---
title: Méthode IWMPMedia3 getItemInfoByType
description: La méthode getItemInfoByType retourne la valeur de l’attribut correspondant au type d’attribut et à l’index spécifiés.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- méthode getItemInfoByType lecteur Windows Media
- méthode getItemInfoByType lecteur Windows Media, interface IWMPMedia3
- Interface IWMPMedia3 lecteur Windows Media, méthode getItemInfoByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522773"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a><span data-ttu-id="92722-106">IWMPMedia3 :: getItemInfoByType, méthode</span><span class="sxs-lookup"><span data-stu-id="92722-106">IWMPMedia3::getItemInfoByType method</span></span>

<span data-ttu-id="92722-107">La méthode **getItemInfoByType** retourne la valeur de l’attribut correspondant au type d’attribut et à l’index spécifiés.</span><span class="sxs-lookup"><span data-stu-id="92722-107">The **getItemInfoByType** method returns the value of the attribute corresponding to the specified attribute type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="92722-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92722-108">Syntax</span></span>


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a><span data-ttu-id="92722-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92722-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92722-110">*bstrType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92722-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92722-111">**System. String** qui est le type d’attribut.</span><span class="sxs-lookup"><span data-stu-id="92722-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="92722-112">*bstrLanguage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92722-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92722-113">**System. String** qui est le langage.</span><span class="sxs-lookup"><span data-stu-id="92722-113">A **System.String** that is the language.</span></span> <span data-ttu-id="92722-114">Si la valeur est définie sur null ou sur une chaîne de longueur nulle (""), la chaîne de paramètres régionaux active est utilisée.</span><span class="sxs-lookup"><span data-stu-id="92722-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="92722-115">Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».</span><span class="sxs-lookup"><span data-stu-id="92722-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="92722-116">*Lindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92722-116">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92722-117">**System. Int32** qui est l’index d’attribut.</span><span class="sxs-lookup"><span data-stu-id="92722-117">A **System.Int32** that is the attribute index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92722-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92722-118">Return value</span></span>

<span data-ttu-id="92722-119">**System. Object** qui est la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="92722-119">A **System.Object** that is the value of the attribute.</span></span> <span data-ttu-id="92722-120">Le type de conversion de cet objet dépend du type de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="92722-120">The type to cast this object to depends on the type of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="92722-121">Notes</span><span class="sxs-lookup"><span data-stu-id="92722-121">Remarks</span></span>

<span data-ttu-id="92722-122">Cette méthode retourne les métadonnées pour un élément multimédia numérique individuel ou un élément multimédia qui fait partie d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="92722-122">This method returns the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="92722-123">Cette méthode prend en charge des attributs avec plusieurs valeurs et attributs avec des valeurs complexes.</span><span class="sxs-lookup"><span data-stu-id="92722-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="92722-124">La méthode **getItemInfo** ne prend pas en charge les attributs avec plusieurs valeurs et attributs avec des valeurs complexes.</span><span class="sxs-lookup"><span data-stu-id="92722-124">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="92722-125">La propriété **attributeCount** obtient le nombre de noms d’attribut disponibles pour un élément multimédia donné.</span><span class="sxs-lookup"><span data-stu-id="92722-125">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="92722-126">Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer le nom de chaque attribut disponible.</span><span class="sxs-lookup"><span data-stu-id="92722-126">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="92722-127">Les noms d’attributs individuels peuvent être passés au paramètre *Name* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="92722-127">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="92722-128">La méthode **getAttributeCountByType** retourne le nombre d’attributs qui correspondent à un nom d’attribut particulier pour un élément multimédia donné.</span><span class="sxs-lookup"><span data-stu-id="92722-128">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given media item.</span></span> <span data-ttu-id="92722-129">Les numéros d’index peuvent ensuite être passés au paramètre d' *index* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="92722-129">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="92722-130">Cela est utile lorsqu’un élément multimédia a été catégorisé dans plusieurs genres, par exemple.</span><span class="sxs-lookup"><span data-stu-id="92722-130">This is useful when a media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="92722-131">Si l’élément multimédia provient d’une bibliothèque qui a été récupérée en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), l’ensemble des attributs disponibles diffère de ceux qui peuvent être interrogés à partir de la bibliothèque locale récupérée en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="92722-131">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="92722-132">Par exemple, les attributs disponibles à partir de la bibliothèque locale récupéré à l’aide de **IWMPLibrary** seront un sous-ensemble des attributs disponibles à partir de la bibliothèque locale Récupérée à l’aide de **AxWindowsMediaPlayer**.</span><span class="sxs-lookup"><span data-stu-id="92722-132">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **AxWindowsMediaPlayer**.</span></span> <span data-ttu-id="92722-133">L’ensemble d’attributs disponibles à partir d’autres sources (bibliothèques distantes, périphériques portables ou CDs) est défini par les autres sources.</span><span class="sxs-lookup"><span data-stu-id="92722-133">The set of attributes available from other sources (remote libraries, portable devices, or CDs is defined by the other sources.</span></span>

<span data-ttu-id="92722-134">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="92722-134">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="92722-135">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="92722-135">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92722-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92722-136">Requirements</span></span>



| <span data-ttu-id="92722-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92722-137">Requirement</span></span> | <span data-ttu-id="92722-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="92722-138">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92722-139">Version</span><span class="sxs-lookup"><span data-stu-id="92722-139">Version</span></span><br/>   | <span data-ttu-id="92722-140">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="92722-140">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="92722-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="92722-141">Namespace</span></span><br/> | <span data-ttu-id="92722-142">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="92722-142">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="92722-143">Assembly</span><span class="sxs-lookup"><span data-stu-id="92722-143">Assembly</span></span><br/>  | <dl> <span data-ttu-id="92722-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="92722-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92722-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92722-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92722-146">**Interface IWMPMedia3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="92722-146">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="92722-147">**IWMPMedia. attributeCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="92722-147">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="92722-148">**IWMPMedia. getAttributeName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="92722-148">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="92722-149">**IWMPMedia. getItemInfo (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="92722-149">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="92722-150">**IWMPMedia3. getAttributeCountByType (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="92722-150">**IWMPMedia3.getAttributeCountByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





