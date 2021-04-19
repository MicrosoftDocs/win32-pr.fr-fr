---
title: Méthode Media. getAttributeName
description: La méthode getAttributeName récupère le nom de l’attribut correspondant à l’index spécifié.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- méthode getAttributeName lecteur Windows Media
- méthode getAttributeName lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode getAttributeName
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7134b68837a7a5d1b765c64320ae68c56c6fc56
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523528"
---
# <a name="mediagetattributename-method"></a><span data-ttu-id="e02f2-106">Méthode Media. getAttributeName</span><span class="sxs-lookup"><span data-stu-id="e02f2-106">Media.getAttributeName method</span></span>

<span data-ttu-id="e02f2-107">La méthode **getAttributeName** récupère le nom de l’attribut correspondant à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="e02f2-107">The **getAttributeName** method retrieves the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e02f2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e02f2-108">Syntax</span></span>


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="e02f2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e02f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e02f2-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e02f2-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e02f2-111">**Nombre** (**long**) contenant l’index de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e02f2-111">**Number** (**long**) containing the index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e02f2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e02f2-112">Return value</span></span>

<span data-ttu-id="e02f2-113">Cette méthode retourne une **chaîne** spécifiant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="e02f2-113">This method returns a **String** specifying the name of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="e02f2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e02f2-114">Remarks</span></span>

<span data-ttu-id="e02f2-115">Le nom d’attribut retourné peut être utilisé conjointement avec **getItemInfo** pour récupérer la valeur d’un attribut nommé spécifique.</span><span class="sxs-lookup"><span data-stu-id="e02f2-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="e02f2-116">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="e02f2-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e02f2-117">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e02f2-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="e02f2-118">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e02f2-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="e02f2-119">**Lecteur Windows Media 10 Mobile :** Les attributs d’un élément multimédia sont disponibles uniquement lors de la lecture, sauf s’ils sont récupérés à partir de l’élément via la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="e02f2-119">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="e02f2-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="e02f2-120">Examples</span></span>

<span data-ttu-id="e02f2-121">L’exemple JScript suivant utilise un *média*. **getAttributeName** pour remplir une zone de texte html nommée myText avec l’index et le nom de chaque attribut de l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="e02f2-121">The following JScript example uses *Media*.**getAttributeName** to fill an HTML text area named myText with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="e02f2-122">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="e02f2-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="e02f2-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e02f2-123">Requirements</span></span>



| <span data-ttu-id="e02f2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e02f2-124">Requirement</span></span> | <span data-ttu-id="e02f2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e02f2-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e02f2-126">Version</span><span class="sxs-lookup"><span data-stu-id="e02f2-126">Version</span></span><br/> | <span data-ttu-id="e02f2-127">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e02f2-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e02f2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e02f2-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="e02f2-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e02f2-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e02f2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e02f2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e02f2-131">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="e02f2-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="e02f2-132">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="e02f2-132">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="e02f2-133">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="e02f2-133">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="e02f2-134">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e02f2-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e02f2-135">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e02f2-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





