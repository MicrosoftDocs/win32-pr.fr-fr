---
title: Méthode Media. getItemInfoByAtom
description: La méthode getItemInfoByAtom récupère la valeur de l’attribut avec le numéro d’index spécifié.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- méthode getItemInfoByAtom lecteur Windows Media
- méthode getItemInfoByAtom lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode getItemInfoByAtom
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530003"
---
# <a name="mediagetiteminfobyatom-method"></a><span data-ttu-id="3eafc-106">Méthode Media. getItemInfoByAtom</span><span class="sxs-lookup"><span data-stu-id="3eafc-106">Media.getItemInfoByAtom method</span></span>

<span data-ttu-id="3eafc-107">La méthode **getItemInfoByAtom** récupère la valeur de l’attribut avec le numéro d’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="3eafc-107">The **getItemInfoByAtom** method retrieves the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eafc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3eafc-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="3eafc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3eafc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eafc-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3eafc-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eafc-111">**Nombre** (**long**) spécifiant l’index auquel un attribut donné réside dans le jeu d’attributs disponibles.</span><span class="sxs-lookup"><span data-stu-id="3eafc-111">**Number** (**long**) specifying the index at which a given attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eafc-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3eafc-112">Return value</span></span>

<span data-ttu-id="3eafc-113">Cette méthode retourne une **chaîne** représentant la valeur de l’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="3eafc-113">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="3eafc-114">Pour les attributs dont la valeur sous-jacente est **booléenne**, elle retourne la chaîne « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="3eafc-114">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="3eafc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3eafc-115">Remarks</span></span>

<span data-ttu-id="3eafc-116">Cette méthode peut être utilisée pour récupérer des métadonnées pour un élément multimédia numérique spécifique à l’aide d’un numéro d’index d’attribut.</span><span class="sxs-lookup"><span data-stu-id="3eafc-116">This method can be used to retrieve metadata for a specific digital media item by using an attribute index number.</span></span> <span data-ttu-id="3eafc-117">La propriété **attributeCount** peut être utilisée pour déterminer le nombre d’attributs disponibles pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="3eafc-117">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="3eafc-118">La méthode **getMediaAtom** de l’objet **MediaCollection** peut également être utilisée pour récupérer l’index d’un attribut particulier.</span><span class="sxs-lookup"><span data-stu-id="3eafc-118">The **getMediaAtom** method of the **MediaCollection** object can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="3eafc-119">Cette technique est généralement plus efficace que les méthodes **getItemInfo** ou **getItemInfoByType** lorsque vous utilisez des sélections volumineuses.</span><span class="sxs-lookup"><span data-stu-id="3eafc-119">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="3eafc-120">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="3eafc-120">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3eafc-121">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3eafc-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="3eafc-122">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3eafc-122">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="3eafc-123">**Lecteur Windows Media 10 Mobile :** Les attributs d’un élément multimédia sont disponibles uniquement lors de la lecture, sauf s’ils sont récupérés à partir de l’élément via la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="3eafc-123">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eafc-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3eafc-124">Requirements</span></span>



| <span data-ttu-id="3eafc-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3eafc-125">Requirement</span></span> | <span data-ttu-id="3eafc-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3eafc-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3eafc-127">Version</span><span class="sxs-lookup"><span data-stu-id="3eafc-127">Version</span></span><br/> | <span data-ttu-id="3eafc-128">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3eafc-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3eafc-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3eafc-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="3eafc-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3eafc-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eafc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eafc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eafc-132">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="3eafc-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="3eafc-133">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="3eafc-133">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="3eafc-134">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="3eafc-134">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="3eafc-135">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="3eafc-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="3eafc-136">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="3eafc-136">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="3eafc-137">**MediaCollection.getMediaAtom**</span><span class="sxs-lookup"><span data-stu-id="3eafc-137">**MediaCollection.getMediaAtom**</span></span>](mediacollection-getmediaatom.md)
</dt> <dt>

[<span data-ttu-id="3eafc-138">**Lecture des valeurs d’attribut**</span><span class="sxs-lookup"><span data-stu-id="3eafc-138">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="3eafc-139">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3eafc-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3eafc-140">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3eafc-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





