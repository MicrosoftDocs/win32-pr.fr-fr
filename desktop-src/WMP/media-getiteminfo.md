---
title: Méthode Media. getItemInfo
description: La méthode getItemInfo récupère la valeur de l’attribut spécifié pour l’élément multimédia actuel.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode getItemInfo
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e7348e73e3550ed668f6694ccfe9ed615215b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535380"
---
# <a name="mediagetiteminfo-method"></a><span data-ttu-id="60829-106">Méthode Media. getItemInfo</span><span class="sxs-lookup"><span data-stu-id="60829-106">Media.getItemInfo method</span></span>

<span data-ttu-id="60829-107">La méthode **getItemInfo** récupère la valeur de l’attribut spécifié pour l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="60829-107">The **getItemInfo** method retrieves the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="60829-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60829-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="60829-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60829-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60829-110">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60829-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60829-111">**Chaîne** contenant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="60829-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="60829-112">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="60829-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60829-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60829-113">Return value</span></span>

<span data-ttu-id="60829-114">Cette méthode retourne une **chaîne** représentant la valeur de l’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="60829-114">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="60829-115">Pour les attributs dont la valeur sous-jacente est **booléenne**, elle retourne la chaîne « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="60829-115">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="60829-116">Notes</span><span class="sxs-lookup"><span data-stu-id="60829-116">Remarks</span></span>

<span data-ttu-id="60829-117">Cette méthode récupère les métadonnées pour un élément multimédia numérique individuel ou un élément multimédia qui fait partie d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="60829-117">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="60829-118">La propriété **attributeCount** contient le nombre de noms d’attribut disponibles pour un objet **multimédia** donné.</span><span class="sxs-lookup"><span data-stu-id="60829-118">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="60829-119">Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer le nom de chaque attribut disponible.</span><span class="sxs-lookup"><span data-stu-id="60829-119">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="60829-120">Les noms d’attributs individuels peuvent être passés à **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="60829-120">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="60829-121">Pour récupérer des attributs avec plusieurs valeurs et attributs avec des valeurs complexes, utilisez la méthode **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="60829-121">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="60829-122">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="60829-122">To use this method, read access to the library is required.</span></span> <span data-ttu-id="60829-123">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="60829-123">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="60829-124">Pour partager les bibliothèques Windows Media via UPnP, le lecteur Windows Media crée un service d’annuaire de contenu (CDS) qui est exposé sur UPnP.</span><span class="sxs-lookup"><span data-stu-id="60829-124">To share the Windows media libraries over UPnP, Windows Media Player creates a content directory service (CDS) that is exposed over UPnP.</span></span> <span data-ttu-id="60829-125">Les autres appareils peuvent alors parcourir les bibliothèques et y accéder.</span><span class="sxs-lookup"><span data-stu-id="60829-125">Other devices can then navigate and browse the libraries.</span></span>

<span data-ttu-id="60829-126">Dans Windows 7, une application peut utiliser les attributs [**TrackingID**](trackingid-attribute.md) et [**MediaType**](mediatype-attribute.md) du lecteur Windows Media pour créer l’ID d’objet de chaque élément dans les CDs.</span><span class="sxs-lookup"><span data-stu-id="60829-126">In Windows 7, an application can use the Windows Media Player [**TrackingID**](trackingid-attribute.md) and [**MediaType**](mediatype-attribute.md) attributes to construct the object ID of each item in the CDS.</span></span> <span data-ttu-id="60829-127">Notez que cette construction peut changer dans les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="60829-127">Note that this construction might change in future versions of Windows.</span></span> <span data-ttu-id="60829-128">L’application passe chacune de ces chaînes d’attributs dans le paramètre *Name* dans un appel à **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="60829-128">The application passes each of these attribute strings in the *name* parameter in a call to **getItemInfo**.</span></span> <span data-ttu-id="60829-129">**getItemInfo** retourne la valeur de chaque attribut de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="60829-129">**getItemInfo** returns the value for each attribute in the return value.</span></span> <span data-ttu-id="60829-130">L’application utilise ensuite la syntaxe suivante pour construire chaque ID d’objet :</span><span class="sxs-lookup"><span data-stu-id="60829-130">The application then uses the following syntax to construct each object ID:</span></span>

<span data-ttu-id="60829-131">*TrackingID*. 0. *MediaTypeID*</span><span class="sxs-lookup"><span data-stu-id="60829-131">*TrackingID*.0.*MediaTypeID*</span></span>

<span data-ttu-id="60829-132">La signification de cette syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="60829-132">This syntax has the following meaning:</span></span>

-   <span data-ttu-id="60829-133">*TrackingID* est la chaîne stockée dans l’attribut [**TrackingID**](trackingid-attribute.md) du lecteur Windows Media de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="60829-133">*TrackingID* is the string that is stored in the Windows Media Player [**TrackingID**](trackingid-attribute.md) attribute of the media item.</span></span>
-   <span data-ttu-id="60829-134">*MediaTypeID* dépend de la valeur de l’attribut [**MediaType**](mediatype-attribute.md) , comme indiqué dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="60829-134">*MediaTypeID* depends on the value of the [**MediaType**](mediatype-attribute.md) attribute, as shown in the following table:</span></span>

    | <span data-ttu-id="60829-135">MediaType (attribut)</span><span class="sxs-lookup"><span data-stu-id="60829-135">MediaType attribute</span></span>                      | <span data-ttu-id="60829-136">MediaTypeID</span><span class="sxs-lookup"><span data-stu-id="60829-136">MediaTypeID</span></span> |
    |------------------------------------------|-------------|
    | [<span data-ttu-id="60829-137">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="60829-137">Audio Items</span></span>](audio-item-attributes.md) | <span data-ttu-id="60829-138">4</span><span class="sxs-lookup"><span data-stu-id="60829-138">4</span></span>           |
    | [<span data-ttu-id="60829-139">Éléments de photo</span><span class="sxs-lookup"><span data-stu-id="60829-139">Photo Items</span></span>](photo-item-attributes.md) | <span data-ttu-id="60829-140">B</span><span class="sxs-lookup"><span data-stu-id="60829-140">B</span></span>           |
    | [<span data-ttu-id="60829-141">Éléments vidéo</span><span class="sxs-lookup"><span data-stu-id="60829-141">Video Items</span></span>](video-item-attributes.md) | <span data-ttu-id="60829-142">8</span><span class="sxs-lookup"><span data-stu-id="60829-142">8</span></span>           |

    

     

<span data-ttu-id="60829-143">**Lecteur Windows Media 10 Mobile :** Les attributs d’un élément multimédia sont disponibles uniquement lors de la lecture, sauf s’ils sont récupérés à partir de l’élément via la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="60829-143">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="60829-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60829-144">Requirements</span></span>



| <span data-ttu-id="60829-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60829-145">Requirement</span></span> | <span data-ttu-id="60829-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="60829-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60829-147">Version</span><span class="sxs-lookup"><span data-stu-id="60829-147">Version</span></span><br/> | <span data-ttu-id="60829-148">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="60829-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="60829-149">DLL</span><span class="sxs-lookup"><span data-stu-id="60829-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="60829-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60829-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60829-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60829-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60829-152">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="60829-152">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="60829-153">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="60829-153">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="60829-154">**Media. getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="60829-154">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="60829-155">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="60829-155">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="60829-156">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="60829-156">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="60829-157">**Lecture des valeurs d’attribut**</span><span class="sxs-lookup"><span data-stu-id="60829-157">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="60829-158">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="60829-158">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="60829-159">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="60829-159">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





