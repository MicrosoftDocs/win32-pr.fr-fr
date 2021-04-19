---
title: StringCollection. getItemInfoByType, méthode
description: La méthode getItemInfoByType récupère la valeur correspondant à l’index, au nom, à la langue et à l’index d’attribut de StringCollection spécifiés.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- méthode getItemInfoByType lecteur Windows Media
- méthode getItemInfoByType Player Windows Media, StringCollection Class
- StringCollection, classe Windows Media Player, méthode getItemInfoByType
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523546"
---
# <a name="stringcollectiongetiteminfobytype-method"></a><span data-ttu-id="c645b-106">StringCollection. getItemInfoByType, méthode</span><span class="sxs-lookup"><span data-stu-id="c645b-106">StringCollection.getItemInfoByType method</span></span>

<span data-ttu-id="c645b-107">La méthode **getItemInfoByType** récupère la valeur correspondant à l’index, au nom, à la langue et à l’index d’attribut de **StringCollection** spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c645b-107">The **getItemInfoByType** method retrieves the value corresponding to the specified **StringCollection** index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c645b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c645b-108">Syntax</span></span>


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
)
```



## <a name="parameters"></a><span data-ttu-id="c645b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c645b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c645b-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c645b-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c645b-111">**Number** (**long**) spécifiant l’index de base zéro de l’élément **StringCollection** à partir duquel l’attribut doit être obtenu.</span><span class="sxs-lookup"><span data-stu-id="c645b-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="c645b-112">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c645b-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c645b-113">**Chaîne** contenant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="c645b-113">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="c645b-114">*langue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c645b-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c645b-115">**Chaîne** contenant le langage.</span><span class="sxs-lookup"><span data-stu-id="c645b-115">**String** containing the language.</span></span> <span data-ttu-id="c645b-116">Si la valeur est définie sur null ou sur la chaîne vide (""), la chaîne de paramètres régionaux active est utilisée.</span><span class="sxs-lookup"><span data-stu-id="c645b-116">If the value is set to null or the empty string ("") the current locale string is used.</span></span> <span data-ttu-id="c645b-117">Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».</span><span class="sxs-lookup"><span data-stu-id="c645b-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="c645b-118">*attributeIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c645b-118">*attributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c645b-119">**Nombre** (**long**) contenant l’index de base zéro de la valeur à récupérer de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="c645b-119">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c645b-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c645b-120">Return value</span></span>

<span data-ttu-id="c645b-121">Cette méthode retourne un **nombre**, une **chaîne**, un objet **MetadataPicture** ou un objet **MetadataText** comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c645b-121">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="c645b-122">Attribut</span><span class="sxs-lookup"><span data-stu-id="c645b-122">Attribute</span></span>                   | <span data-ttu-id="c645b-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c645b-123">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="c645b-124">**SyncState**</span><span class="sxs-lookup"><span data-stu-id="c645b-124">**SyncState**</span></span>               | <span data-ttu-id="c645b-125">**Number** (**unsigned long**)</span><span class="sxs-lookup"><span data-stu-id="c645b-125">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="c645b-126">**Synchronisation des WM et des paroles \_**</span><span class="sxs-lookup"><span data-stu-id="c645b-126">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="c645b-127">Objet **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="c645b-127">**MetadataText** object</span></span>        |
| <span data-ttu-id="c645b-128">**WM/image**</span><span class="sxs-lookup"><span data-stu-id="c645b-128">**WM/Picture**</span></span>              | <span data-ttu-id="c645b-129">Objet **MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="c645b-129">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="c645b-130">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="c645b-130">**WM/UserWebURL**</span></span>           | <span data-ttu-id="c645b-131">Objet **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="c645b-131">**MetadataText** object</span></span>        |
| <span data-ttu-id="c645b-132">Tous les autres attributs</span><span class="sxs-lookup"><span data-stu-id="c645b-132">All other attributes</span></span>        | <span data-ttu-id="c645b-133">String</span><span class="sxs-lookup"><span data-stu-id="c645b-133">String</span></span>                         |



 

<span data-ttu-id="c645b-134">Pour les attributs dont la valeur sous-jacente est **booléenne**, cette méthode retourne la chaîne « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="c645b-134">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="c645b-135">Notes</span><span class="sxs-lookup"><span data-stu-id="c645b-135">Remarks</span></span>

<span data-ttu-id="c645b-136">Cette méthode prend en charge des attributs avec plusieurs valeurs et des attributs avec des valeurs complexes.</span><span class="sxs-lookup"><span data-stu-id="c645b-136">This method supports attributes with multiple values, and attributes with complex values.</span></span> <span data-ttu-id="c645b-137">La méthode **getItemInfo** ne prend pas en charge les attributs avec plusieurs valeurs ou des valeurs complexes.</span><span class="sxs-lookup"><span data-stu-id="c645b-137">The **getItemInfo** method does not support attributes with multiple or complex values.</span></span>

<span data-ttu-id="c645b-138">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="c645b-138">To use this method, read access to the library is required.</span></span> <span data-ttu-id="c645b-139">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c645b-139">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c645b-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c645b-140">Requirements</span></span>



| <span data-ttu-id="c645b-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c645b-141">Requirement</span></span> | <span data-ttu-id="c645b-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="c645b-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c645b-143">Version</span><span class="sxs-lookup"><span data-stu-id="c645b-143">Version</span></span><br/> | <span data-ttu-id="c645b-144">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="c645b-144">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="c645b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c645b-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="c645b-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c645b-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c645b-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c645b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c645b-148">**Objet MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="c645b-148">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="c645b-149">**Objet MetadataText**</span><span class="sxs-lookup"><span data-stu-id="c645b-149">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="c645b-150">**StringCollection. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="c645b-150">**StringCollection.getItemInfo**</span></span>](stringcollection-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="c645b-151">**StringCollection, objet**</span><span class="sxs-lookup"><span data-stu-id="c645b-151">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





