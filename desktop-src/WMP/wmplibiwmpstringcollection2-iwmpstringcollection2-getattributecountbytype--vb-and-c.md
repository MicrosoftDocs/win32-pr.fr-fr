---
title: Méthode IWMPStringCollection2 getAttributeCountByType
description: La méthode getAttributeCountByType retourne le nombre d’attributs associés à l’index de collection de chaînes, au nom d’attribut et à la langue spécifiés.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- méthode getAttributeCountByType lecteur Windows Media
- méthode getAttributeCountByType lecteur Windows Media, interface IWMPStringCollection2
- Interface IWMPStringCollection2 lecteur Windows Media, méthode getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bb60fdd843fb3f45b6e4e3aff444a8a915fa0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543186"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a><span data-ttu-id="58899-106">IWMPStringCollection2 :: getAttributeCountByType, méthode</span><span class="sxs-lookup"><span data-stu-id="58899-106">IWMPStringCollection2::getAttributeCountByType method</span></span>

<span data-ttu-id="58899-107">La méthode **getAttributeCountByType** retourne le nombre d’attributs associés à l’index de collection de chaînes, au nom d’attribut et à la langue spécifiés.</span><span class="sxs-lookup"><span data-stu-id="58899-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified string collection index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="58899-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58899-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="58899-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58899-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58899-110">*lCollectionIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58899-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58899-111">**System. Int32** spécifiant l’index de base zéro de l’élément de collection de chaînes à partir duquel l’attribut doit être obtenu.</span><span class="sxs-lookup"><span data-stu-id="58899-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="58899-112">*bstrType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58899-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58899-113">**System. String** qui est le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="58899-113">The **System.String** that is the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="58899-114">*bstrLanguage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58899-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58899-115">**System. String** qui est le nom de la langue.</span><span class="sxs-lookup"><span data-stu-id="58899-115">The **System.String** that is the name of the language.</span></span> <span data-ttu-id="58899-116">Si la valeur est définie sur null ou sur une chaîne de longueur nulle (""), la chaîne de paramètres régionaux active est utilisée.</span><span class="sxs-lookup"><span data-stu-id="58899-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="58899-117">Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».</span><span class="sxs-lookup"><span data-stu-id="58899-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58899-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58899-118">Return value</span></span>

<span data-ttu-id="58899-119">**System. Int32** qui est le nombre.</span><span class="sxs-lookup"><span data-stu-id="58899-119">The **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="58899-120">Notes</span><span class="sxs-lookup"><span data-stu-id="58899-120">Remarks</span></span>

<span data-ttu-id="58899-121">Cette méthode est utilisée pour découvrir le nombre d’attributs correspondant à un nom d’attribut particulier pour un élément **StringCollection** donné.</span><span class="sxs-lookup"><span data-stu-id="58899-121">This method is used to discover the number of attributes corresponding to a particular attribute name for a given **StringCollection** item.</span></span> <span data-ttu-id="58899-122">Les numéros d’index peuvent ensuite être passés au quatrième paramètre de la méthode **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="58899-122">Index numbers can then be passed to the fourth parameter of the **getItemInfoByType** method.</span></span>

<span data-ttu-id="58899-123">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="58899-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="58899-124">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="58899-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58899-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58899-125">Requirements</span></span>



| <span data-ttu-id="58899-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58899-126">Requirement</span></span> | <span data-ttu-id="58899-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="58899-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58899-128">Version</span><span class="sxs-lookup"><span data-stu-id="58899-128">Version</span></span><br/>   | <span data-ttu-id="58899-129">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="58899-129">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="58899-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="58899-130">Namespace</span></span><br/> | <span data-ttu-id="58899-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="58899-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="58899-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="58899-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="58899-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="58899-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58899-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58899-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58899-135">**Interface IWMPStringCollection2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="58899-135">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="58899-136">**IWMPStringCollection2. getItemInfoByType (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="58899-136">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





