---
title: Media. attributeCount
description: La propriété attributeCount récupère le nombre d’attributs qui peuvent être interrogés et/ou définis pour l’élément multimédia.
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- Media. attributeCount Windows Media Player
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4979f670cdd6a79b1b309bc3eceff5a2798223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521678"
---
# <a name="mediaattributecount"></a><span data-ttu-id="976f6-104">Media. attributeCount</span><span class="sxs-lookup"><span data-stu-id="976f6-104">Media.attributeCount</span></span>

<span data-ttu-id="976f6-105">La propriété **attributeCount** récupère le nombre d’attributs qui peuvent être interrogés et/ou définis pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="976f6-105">The **attributeCount** property retrieves the number of attributes that can be queried and/or set for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="976f6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="976f6-106">Syntax</span></span>

<span data-ttu-id="976f6-107">*lecteur*. *currentMedia*. **attributeCount**</span><span class="sxs-lookup"><span data-stu-id="976f6-107">*player*.*currentMedia*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="976f6-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="976f6-108">Possible Values</span></span>

<span data-ttu-id="976f6-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="976f6-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="976f6-110">Notes</span><span class="sxs-lookup"><span data-stu-id="976f6-110">Remarks</span></span>

<span data-ttu-id="976f6-111">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="976f6-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="976f6-112">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="976f6-112">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="976f6-113">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="976f6-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="976f6-114">**Lecteur Windows Media 10 Mobile :** Les attributs d’un élément multimédia sont disponibles uniquement lors de la lecture, sauf s’ils sont récupérés à partir de l’élément via la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="976f6-114">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="976f6-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="976f6-115">Examples</span></span>

<span data-ttu-id="976f6-116">L’exemple JScript suivant utilise un *média*. **attributeCount** pour déterminer le nombre d’attributs disponibles dans l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="976f6-116">The following JScript example uses *Media*.**attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="976f6-117">Le code utilise cette valeur pour imprimer une liste de noms d’attributs et de valeurs dans une zone de texte HTML, nommée myText.</span><span class="sxs-lookup"><span data-stu-id="976f6-117">The code uses that value to print a list of attribute names and values in an HTML text area, named myText.</span></span> <span data-ttu-id="976f6-118">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="976f6-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="976f6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="976f6-119">Requirements</span></span>



| <span data-ttu-id="976f6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="976f6-120">Requirement</span></span> | <span data-ttu-id="976f6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="976f6-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="976f6-122">Version</span><span class="sxs-lookup"><span data-stu-id="976f6-122">Version</span></span><br/> | <span data-ttu-id="976f6-123">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="976f6-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="976f6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="976f6-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="976f6-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="976f6-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="976f6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="976f6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="976f6-127">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="976f6-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="976f6-128">**Media. getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="976f6-128">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="976f6-129">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="976f6-129">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="976f6-130">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="976f6-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="976f6-131">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="976f6-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





