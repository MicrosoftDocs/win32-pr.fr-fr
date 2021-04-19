---
title: Méthode Media. isReadOnlyItem
description: La méthode isReadOnlyItem retourne une valeur indiquant si l’attribut spécifié de l’élément multimédia peut être modifié.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- méthode isReadOnlyItem lecteur Windows Media
- méthode isReadOnlyItem lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode isReadOnlyItem
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ac5bb8d445c3ba6418be4ee5c0c5e7a96f507d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536450"
---
# <a name="mediaisreadonlyitem-method"></a><span data-ttu-id="d5d79-106">Méthode Media. isReadOnlyItem</span><span class="sxs-lookup"><span data-stu-id="d5d79-106">Media.isReadOnlyItem method</span></span>

<span data-ttu-id="d5d79-107">La méthode **isReadOnlyItem** retourne une valeur indiquant si l’attribut spécifié de l’élément multimédia peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="d5d79-107">The **isReadOnlyItem** method returns a value indicating whether the specified attribute of the media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d79-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5d79-108">Syntax</span></span>


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="d5d79-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5d79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5d79-110">*attribut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5d79-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5d79-111">**Chaîne** indiquant le nom de l’attribut à tester.</span><span class="sxs-lookup"><span data-stu-id="d5d79-111">**String** indicating the name of the attribute to test.</span></span> <span data-ttu-id="d5d79-112">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d5d79-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5d79-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5d79-113">Return value</span></span>

<span data-ttu-id="d5d79-114">Cette méthode retourne une **valeur booléenne**.</span><span class="sxs-lookup"><span data-stu-id="d5d79-114">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5d79-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d5d79-115">Remarks</span></span>

<span data-ttu-id="d5d79-116">Si un attribut est en lecture seule, il ne peut pas être défini à l’aide de la méthode **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="d5d79-116">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="d5d79-117">Notez que cette méthode peut retourner des valeurs différentes pour un attribut particulier lorsqu’elle est utilisée avec différentes versions du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d5d79-117">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="d5d79-118">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="d5d79-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="d5d79-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d5d79-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="d5d79-120">**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours **true**.</span><span class="sxs-lookup"><span data-stu-id="d5d79-120">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="d5d79-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="d5d79-121">Examples</span></span>

<span data-ttu-id="d5d79-122">L’exemple JScript suivant utilise un *média*. **isReadOnlyItem** pour remplir un élément textarea html nommé rwText avec des informations sur l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="d5d79-122">The following JScript example uses *Media*.**isReadOnlyItem** to fill an HTML TEXTAREA element named rwText with information about the current media item.</span></span> <span data-ttu-id="d5d79-123">Le code génère chaque attribut de l’élément multimédia en cours, ainsi que le texte indiquant si l’attribut est en lecture seule ou en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d5d79-123">The code outputs each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="d5d79-124">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d5d79-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="d5d79-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5d79-125">Requirements</span></span>



| <span data-ttu-id="d5d79-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5d79-126">Requirement</span></span> | <span data-ttu-id="d5d79-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5d79-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d79-128">Version</span><span class="sxs-lookup"><span data-stu-id="d5d79-128">Version</span></span><br/> | <span data-ttu-id="d5d79-129">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d5d79-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d5d79-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d5d79-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="d5d79-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5d79-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d79-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5d79-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d79-133">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="d5d79-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="d5d79-134">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="d5d79-134">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="d5d79-135">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d5d79-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="d5d79-136">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d5d79-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





