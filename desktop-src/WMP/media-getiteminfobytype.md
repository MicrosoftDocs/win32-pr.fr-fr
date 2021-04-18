---
title: Méthode Media. getItemInfoByType
description: La méthode getItemInfoByType récupère la valeur de l’attribut correspondant au nom, à la langue et à l’index spécifiés de l’attribut.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- méthode getItemInfoByType lecteur Windows Media
- méthode getItemInfoByType lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode getItemInfoByType
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526857"
---
# <a name="mediagetiteminfobytype-method"></a><span data-ttu-id="1ec89-106">Méthode Media. getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="1ec89-106">Media.getItemInfoByType method</span></span>

<span data-ttu-id="1ec89-107">La méthode **getItemInfoByType** récupère la valeur de l’attribut correspondant au nom, à la langue et à l’index spécifiés de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="1ec89-107">The **getItemInfoByType** method retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec89-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ec89-108">Syntax</span></span>


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a><span data-ttu-id="1ec89-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ec89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec89-110">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ec89-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec89-111">**Chaîne** contenant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="1ec89-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="1ec89-112">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1ec89-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ec89-113">*langue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ec89-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec89-114">**Chaîne** représentant la langue.</span><span class="sxs-lookup"><span data-stu-id="1ec89-114">**String** representing the language.</span></span> <span data-ttu-id="1ec89-115">Si la valeur est définie sur null ou «» (chaîne vide), la chaîne de paramètres régionaux actuelle est utilisée.</span><span class="sxs-lookup"><span data-stu-id="1ec89-115">If the value is set to null or "" (empty string) the current locale string is used.</span></span> <span data-ttu-id="1ec89-116">Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».</span><span class="sxs-lookup"><span data-stu-id="1ec89-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="1ec89-117">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ec89-117">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec89-118">**Nombre** (**long**) contenant l’index de base zéro de la valeur à récupérer de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="1ec89-118">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec89-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ec89-119">Return value</span></span>

<span data-ttu-id="1ec89-120">Cette méthode retourne un **nombre**, une **chaîne**, un objet **MetadataPicture** ou un objet **MetadataText** comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1ec89-120">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="1ec89-121">Attribut</span><span class="sxs-lookup"><span data-stu-id="1ec89-121">Attribute</span></span>                   | <span data-ttu-id="1ec89-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ec89-122">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="1ec89-123">**SyncState**</span><span class="sxs-lookup"><span data-stu-id="1ec89-123">**SyncState**</span></span>               | <span data-ttu-id="1ec89-124">**Number** (**unsigned long**)</span><span class="sxs-lookup"><span data-stu-id="1ec89-124">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="1ec89-125">**Synchronisation des WM et des paroles \_**</span><span class="sxs-lookup"><span data-stu-id="1ec89-125">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="1ec89-126">Objet **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="1ec89-126">**MetadataText** object</span></span>        |
| <span data-ttu-id="1ec89-127">**WM/image**</span><span class="sxs-lookup"><span data-stu-id="1ec89-127">**WM/Picture**</span></span>              | <span data-ttu-id="1ec89-128">Objet **MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="1ec89-128">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="1ec89-129">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="1ec89-129">**WM/UserWebURL**</span></span>           | <span data-ttu-id="1ec89-130">Objet **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="1ec89-130">**MetadataText** object</span></span>        |
| <span data-ttu-id="1ec89-131">Tous les autres attributs</span><span class="sxs-lookup"><span data-stu-id="1ec89-131">All other attributes</span></span>        | <span data-ttu-id="1ec89-132">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ec89-132">**String**</span></span>                     |



 

<span data-ttu-id="1ec89-133">Pour les attributs dont la valeur sous-jacente est **booléenne**, cette méthode retourne la chaîne « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="1ec89-133">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec89-134">Notes</span><span class="sxs-lookup"><span data-stu-id="1ec89-134">Remarks</span></span>

<span data-ttu-id="1ec89-135">Cette méthode récupère les métadonnées pour un élément multimédia numérique individuel ou un élément multimédia qui fait partie d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="1ec89-135">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="1ec89-136">Cette méthode prend en charge des attributs avec plusieurs valeurs et attributs avec des valeurs complexes.</span><span class="sxs-lookup"><span data-stu-id="1ec89-136">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="1ec89-137">La méthode **getItemInfo** ne prend pas en charge les attributs avec plusieurs valeurs et attributs avec des valeurs complexes.</span><span class="sxs-lookup"><span data-stu-id="1ec89-137">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="1ec89-138">La propriété **attributeCount** contient le nombre de noms d’attribut disponibles pour un objet **multimédia** donné.</span><span class="sxs-lookup"><span data-stu-id="1ec89-138">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="1ec89-139">Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer le nom de chaque attribut disponible.</span><span class="sxs-lookup"><span data-stu-id="1ec89-139">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="1ec89-140">Les noms d’attributs individuels peuvent être passés au paramètre *Name* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="1ec89-140">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="1ec89-141">La méthode **getAttributeCountByType** retourne le nombre d’attributs qui correspondent à un nom d’attribut particulier pour un objet **multimédia** donné.</span><span class="sxs-lookup"><span data-stu-id="1ec89-141">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="1ec89-142">Les numéros d’index peuvent ensuite être passés au paramètre d' *index* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="1ec89-142">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="1ec89-143">Cela est utile lorsqu’un élément multimédia numérique a été catégorisé dans plusieurs genres, par exemple.</span><span class="sxs-lookup"><span data-stu-id="1ec89-143">This is useful when a digital media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="1ec89-144">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="1ec89-144">To use this method, read access to the library is required.</span></span> <span data-ttu-id="1ec89-145">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1ec89-145">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="1ec89-146">Cette méthode peut provoquer des erreurs.</span><span class="sxs-lookup"><span data-stu-id="1ec89-146">This method can cause errors.</span></span> <span data-ttu-id="1ec89-147">Vous devez inclure le code de gestion des erreurs lorsque vous appelez cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1ec89-147">You should include error-handling code when you call this method.</span></span> <span data-ttu-id="1ec89-148">Par exemple, dans JScript, vous pouvez implémenter la gestion des erreurs à l’aide du **bloc try... catch... finally** , structure.</span><span class="sxs-lookup"><span data-stu-id="1ec89-148">For example, in JScript you can implement error handling by using the **try...catch...finally** structure.</span></span>

<span data-ttu-id="1ec89-149">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1ec89-149">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec89-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ec89-150">Requirements</span></span>



| <span data-ttu-id="1ec89-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ec89-151">Requirement</span></span> | <span data-ttu-id="1ec89-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ec89-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec89-153">Version</span><span class="sxs-lookup"><span data-stu-id="1ec89-153">Version</span></span><br/> | <span data-ttu-id="1ec89-154">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1ec89-154">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="1ec89-155">DLL</span><span class="sxs-lookup"><span data-stu-id="1ec89-155">DLL</span></span><br/>     | <dl> <span data-ttu-id="1ec89-156"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ec89-156"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec89-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ec89-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec89-158">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="1ec89-158">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1ec89-159">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="1ec89-159">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="1ec89-160">**Media. getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="1ec89-160">**Media.getAttributeCountByType**</span></span>](media-getattributecountbytype.md)
</dt> <dt>

[<span data-ttu-id="1ec89-161">**Media. getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="1ec89-161">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="1ec89-162">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="1ec89-162">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="1ec89-163">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="1ec89-163">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="1ec89-164">**Objet MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="1ec89-164">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="1ec89-165">**Objet MetadataText**</span><span class="sxs-lookup"><span data-stu-id="1ec89-165">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="1ec89-166">**Lecture des valeurs d’attribut**</span><span class="sxs-lookup"><span data-stu-id="1ec89-166">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="1ec89-167">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="1ec89-167">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="1ec89-168">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="1ec89-168">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





