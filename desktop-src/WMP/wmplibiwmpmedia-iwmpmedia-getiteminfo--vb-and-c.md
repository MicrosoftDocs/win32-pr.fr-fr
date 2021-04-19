---
title: Méthode IWMPMedia getItemInfo
description: La méthode getItemInfo retourne la valeur de l’attribut spécifié pour l’élément multimédia.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, méthode getItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541725"
---
# <a name="iwmpmediagetiteminfo-method"></a><span data-ttu-id="2ab57-106">IWMPMedia :: getItemInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="2ab57-106">IWMPMedia::getItemInfo method</span></span>

<span data-ttu-id="2ab57-107">La méthode **getItemInfo** retourne la valeur de l’attribut spécifié pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="2ab57-107">The **getItemInfo** method returns the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab57-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ab57-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="2ab57-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ab57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ab57-110">*bstrItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ab57-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ab57-111">**System. String** qui est le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="2ab57-111">A **System.String** that is the name of the attribute.</span></span> <span data-ttu-id="2ab57-112">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2ab57-112">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ab57-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ab57-113">Return value</span></span>

<span data-ttu-id="2ab57-114">**System. String** qui est la valeur de l’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="2ab57-114">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ab57-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2ab57-115">Remarks</span></span>

<span data-ttu-id="2ab57-116">Cette méthode retourne les métadonnées pour un élément multimédia individuel ou un élément multimédia qui fait partie d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="2ab57-116">This method returns the metadata for an individual media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="2ab57-117">La propriété **attributeCount** obtient le nombre de noms d’attribut disponibles pour un élément multimédia donné.</span><span class="sxs-lookup"><span data-stu-id="2ab57-117">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="2ab57-118">Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer le nom de chaque attribut disponible.</span><span class="sxs-lookup"><span data-stu-id="2ab57-118">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="2ab57-119">Les noms d’attributs individuels peuvent être passés à **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="2ab57-119">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="2ab57-120">Pour récupérer des attributs avec plusieurs valeurs et attributs avec des valeurs complexes, utilisez la méthode **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="2ab57-120">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="2ab57-121">Si l’élément multimédia provient d’une bibliothèque qui a été récupérée en appelant [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), l’ensemble des attributs disponibles diffère de ceux qui peuvent être interrogés à partir de la bibliothèque locale récupérée en appelant [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="2ab57-121">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="2ab57-122">Par exemple, les attributs disponibles à partir de la bibliothèque locale récupéré à l’aide de **IWMPLibrary** seront un sous-ensemble des attributs disponibles à partir de la bibliothèque locale Récupérée à l’aide de **IWMPCore**.</span><span class="sxs-lookup"><span data-stu-id="2ab57-122">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **IWMPCore**.</span></span> <span data-ttu-id="2ab57-123">L’ensemble d’attributs disponibles à partir d’autres sources (bibliothèques distantes, appareils mobiles ou CDs) est défini par les autres sources.</span><span class="sxs-lookup"><span data-stu-id="2ab57-123">The set of attributes available from other sources (remote libraries, portable devices, or CDs) is defined by the other sources.</span></span>

<span data-ttu-id="2ab57-124">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2ab57-124">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="2ab57-125">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2ab57-125">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab57-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ab57-126">Requirements</span></span>



| <span data-ttu-id="2ab57-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ab57-127">Requirement</span></span> | <span data-ttu-id="2ab57-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ab57-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab57-129">Version</span><span class="sxs-lookup"><span data-stu-id="2ab57-129">Version</span></span><br/>   | <span data-ttu-id="2ab57-130">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2ab57-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2ab57-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2ab57-131">Namespace</span></span><br/> | <span data-ttu-id="2ab57-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2ab57-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2ab57-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="2ab57-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2ab57-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2ab57-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ab57-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ab57-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab57-136">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="2ab57-136">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="2ab57-137">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2ab57-137">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ab57-138">**IWMPMedia. attributeCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2ab57-138">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ab57-139">**IWMPMedia. getAttributeName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2ab57-139">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ab57-140">**IWMPMedia. setItemInfo (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2ab57-140">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ab57-141">**IWMPMedia3. getItemInfoByType (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2ab57-141">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





