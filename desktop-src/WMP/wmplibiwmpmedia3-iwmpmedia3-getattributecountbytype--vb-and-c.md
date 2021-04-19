---
title: Méthode IWMPMedia3 getAttributeCountByType
description: La méthode getAttributeCountByType retourne le nombre d’attributs associés au type d’attribut spécifié.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- méthode getAttributeCountByType lecteur Windows Media
- méthode getAttributeCountByType lecteur Windows Media, interface IWMPMedia3
- Interface IWMPMedia3 lecteur Windows Media, méthode getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539537"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a><span data-ttu-id="b7123-106">IWMPMedia3 :: getAttributeCountByType, méthode</span><span class="sxs-lookup"><span data-stu-id="b7123-106">IWMPMedia3::getAttributeCountByType method</span></span>

<span data-ttu-id="b7123-107">La méthode **getAttributeCountByType** retourne le nombre d’attributs associés au type d’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7123-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified attribute type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7123-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7123-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="b7123-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7123-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7123-110">*bstrType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7123-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7123-111">**System. String** qui est le type d’attribut.</span><span class="sxs-lookup"><span data-stu-id="b7123-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="b7123-112">*bstrLanguage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7123-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7123-113">**System. String** qui est le langage.</span><span class="sxs-lookup"><span data-stu-id="b7123-113">A **System.String** that is the language.</span></span> <span data-ttu-id="b7123-114">Si la valeur est définie sur null ou sur une chaîne de longueur nulle (""), la chaîne de paramètres régionaux active est utilisée.</span><span class="sxs-lookup"><span data-stu-id="b7123-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="b7123-115">Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».</span><span class="sxs-lookup"><span data-stu-id="b7123-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7123-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7123-116">Return value</span></span>

<span data-ttu-id="b7123-117">**System. Int32** qui est le nombre d’attributs associés au type.</span><span class="sxs-lookup"><span data-stu-id="b7123-117">A **System.Int32** that is the count of attributes that are associated with the type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7123-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b7123-118">Remarks</span></span>

<span data-ttu-id="b7123-119">Cette méthode est utilisée pour découvrir le nombre d’attributs correspondant à un nom d’attribut particulier pour un élément multimédia donné.</span><span class="sxs-lookup"><span data-stu-id="b7123-119">This method is used to discover the number of attributes corresponding to a particular attribute name for a given media item.</span></span> <span data-ttu-id="b7123-120">Les numéros d’index peuvent ensuite être passés à la méthode **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="b7123-120">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="b7123-121">Cela est utile, par exemple, lorsqu’un élément multimédia a été catégorisé sous plusieurs genres.</span><span class="sxs-lookup"><span data-stu-id="b7123-121">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="b7123-122">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b7123-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="b7123-123">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b7123-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7123-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7123-124">Requirements</span></span>



| <span data-ttu-id="b7123-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7123-125">Requirement</span></span> | <span data-ttu-id="b7123-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7123-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7123-127">Version</span><span class="sxs-lookup"><span data-stu-id="b7123-127">Version</span></span><br/>   | <span data-ttu-id="b7123-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b7123-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b7123-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b7123-129">Namespace</span></span><br/> | <span data-ttu-id="b7123-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b7123-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b7123-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="b7123-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b7123-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b7123-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7123-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7123-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7123-134">**Interface IWMPMedia3 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b7123-134">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b7123-135">**IWMPMedia3. getItemInfoByType (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b7123-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





