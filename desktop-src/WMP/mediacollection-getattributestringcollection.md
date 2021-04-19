---
title: Méthode MediaCollection. getAttributeStringCollection
description: La méthode getAttributeStringCollection récupère un objet StringCollection représentant l’ensemble de toutes les valeurs d’un attribut spécifié dans un type de média spécifié.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- méthode getAttributeStringCollection lecteur Windows Media
- méthode getAttributeStringCollection lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getAttributeStringCollection
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539969"
---
# <a name="mediacollectiongetattributestringcollection-method"></a><span data-ttu-id="ab186-106">Méthode MediaCollection. getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="ab186-106">MediaCollection.getAttributeStringCollection method</span></span>

<span data-ttu-id="ab186-107">La méthode **getAttributeStringCollection** récupère un objet **StringCollection** représentant l’ensemble de toutes les valeurs d’un attribut spécifié dans un type de média spécifié.</span><span class="sxs-lookup"><span data-stu-id="ab186-107">The **getAttributeStringCollection** method retrieves a **StringCollection** object representing the set of all values for a specified attribute within a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab186-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab186-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="ab186-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab186-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab186-110">*attribut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab186-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab186-111">**Chaîne** spécifiant l’attribut.</span><span class="sxs-lookup"><span data-stu-id="ab186-111">**String** specifying the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ab186-112">*MediaType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab186-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab186-113">**Chaîne** représentant le type de média.</span><span class="sxs-lookup"><span data-stu-id="ab186-113">**String** representing the media type.</span></span> <span data-ttu-id="ab186-114">Contient l’une des valeurs suivantes : « audio », « Video », « playlist » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="ab186-114">Contains one of the following values: "Audio", "Video", "Playlist", or "Other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab186-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab186-115">Return value</span></span>

<span data-ttu-id="ab186-116">Cette méthode retourne un objet **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="ab186-116">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab186-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ab186-117">Remarks</span></span>

<span data-ttu-id="ab186-118">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="ab186-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="ab186-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ab186-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ab186-120">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la section [référence des attributs](attribute-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ab186-120">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md) section.</span></span>

## <a name="examples"></a><span data-ttu-id="ab186-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="ab186-121">Examples</span></span>

<span data-ttu-id="ab186-122">L’exemple JScript suivant utilise *MediaCollection*. **getAttributeStringCollection** pour afficher une liste de valeurs qui correspondent à un attribut particulier pour les éléments audio de la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="ab186-122">The following JScript example uses *MediaCollection*.**getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="ab186-123">Un élément SELECT HTML, créé avec ID = "attribute", permet à l’utilisateur de sélectionner un attribut, tel qu’un artiste, un genre ou un album.</span><span class="sxs-lookup"><span data-stu-id="ab186-123">An HTML SELECT element, created with ID = "Attribute", allows the user to select an attribute, such as Artist, Genre, or Album.</span></span> <span data-ttu-id="ab186-124">Un élément TEXTAREA HTML, créé avec ID = "AttributeVals", affiche le résultat.</span><span class="sxs-lookup"><span data-stu-id="ab186-124">An HTML TEXTAREA element, created with ID = "AttributeVals", displays the result.</span></span> <span data-ttu-id="ab186-125">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ab186-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="ab186-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab186-126">Requirements</span></span>



| <span data-ttu-id="ab186-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab186-127">Requirement</span></span> | <span data-ttu-id="ab186-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab186-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab186-129">Version</span><span class="sxs-lookup"><span data-stu-id="ab186-129">Version</span></span><br/> | <span data-ttu-id="ab186-130">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ab186-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ab186-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ab186-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="ab186-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab186-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab186-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab186-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab186-134">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="ab186-134">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="ab186-135">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ab186-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ab186-136">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ab186-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ab186-137">**StringCollection, objet**</span><span class="sxs-lookup"><span data-stu-id="ab186-137">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





