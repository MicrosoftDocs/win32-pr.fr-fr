---
title: StringCollection. getAttributeCountByType, méthode
description: La méthode getAttributeCountByType récupère le nombre d’attributs associés à l’index d’élément StringCollection, le nom d’attribut et la langue spécifiés.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- méthode getAttributeCountByType lecteur Windows Media
- méthode getAttributeCountByType Player Windows Media, StringCollection Class
- StringCollection, classe Windows Media Player, méthode getAttributeCountByType
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525275"
---
# <a name="stringcollectiongetattributecountbytype-method"></a><span data-ttu-id="0e3e6-106">StringCollection. getAttributeCountByType, méthode</span><span class="sxs-lookup"><span data-stu-id="0e3e6-106">StringCollection.getAttributeCountByType method</span></span>

<span data-ttu-id="0e3e6-107">La méthode **getAttributeCountByType** récupère le nombre d’attributs associés à l’index d’élément **StringCollection** , le nom d’attribut et la langue spécifiés.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified **StringCollection** item index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e3e6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e3e6-108">Syntax</span></span>


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="0e3e6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e3e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e3e6-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e3e6-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e3e6-111">**Number** (**long**) spécifiant l’index de base zéro de l’élément **StringCollection** à partir duquel l’attribut doit être obtenu.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="0e3e6-112">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e3e6-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e3e6-113">**Chaîne** contenant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-113">**String** containing the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="0e3e6-114">*langue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e3e6-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e3e6-115">**Chaîne** contenant le langage.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-115">**String** containing the language.</span></span> <span data-ttu-id="0e3e6-116">Si la valeur est définie sur null ou sur la chaîne vide (""), la chaîne de paramètres régionaux active est utilisée.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-116">If the value is set to null or the empty string (""), the current locale string is used.</span></span> <span data-ttu-id="0e3e6-117">Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».</span><span class="sxs-lookup"><span data-stu-id="0e3e6-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e3e6-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e3e6-118">Return value</span></span>

<span data-ttu-id="0e3e6-119">Cette méthode retourne un **nombre** (**long**).</span><span class="sxs-lookup"><span data-stu-id="0e3e6-119">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e3e6-120">Notes</span><span class="sxs-lookup"><span data-stu-id="0e3e6-120">Remarks</span></span>

<span data-ttu-id="0e3e6-121">Cette méthode est utilisée pour déterminer le nombre d’attributs correspondant à un nom d’attribut particulier pour un élément **StringCollection** particulier.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-121">This method is used to determine the number of attributes corresponding to a particular attribute name for a particular **StringCollection** item.</span></span> <span data-ttu-id="0e3e6-122">Les numéros d’index peuvent ensuite être passés au quatrième paramètre de la méthode **StringCollection. getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="0e3e6-122">Index numbers can then be passed to the fourth parameter of the **StringCollection.getItemInfoByType** method.</span></span>

<span data-ttu-id="0e3e6-123">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="0e3e6-124">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0e3e6-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e3e6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e3e6-125">Requirements</span></span>



| <span data-ttu-id="0e3e6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e3e6-126">Requirement</span></span> | <span data-ttu-id="0e3e6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e3e6-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e3e6-128">Version</span><span class="sxs-lookup"><span data-stu-id="0e3e6-128">Version</span></span><br/> | <span data-ttu-id="0e3e6-129">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="0e3e6-129">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="0e3e6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0e3e6-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="0e3e6-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e3e6-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e3e6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e3e6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e3e6-133">**StringCollection, objet**</span><span class="sxs-lookup"><span data-stu-id="0e3e6-133">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





