---
title: Méthode Media. setItemInfo
description: La méthode setItemInfo définit la valeur de l’attribut spécifié pour l’élément multimédia actuel.
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- méthode setItemInfo lecteur Windows Media
- méthode setItemInfo lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode setItemInfo
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535297"
---
# <a name="mediasetiteminfo-method"></a><span data-ttu-id="1f1b1-106">Méthode Media. setItemInfo</span><span class="sxs-lookup"><span data-stu-id="1f1b1-106">Media.setItemInfo method</span></span>

<span data-ttu-id="1f1b1-107">La méthode **setItemInfo** définit la valeur de l’attribut spécifié pour l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-107">The **setItemInfo** method sets the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f1b1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f1b1-108">Syntax</span></span>


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="1f1b1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f1b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f1b1-110">*attribut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f1b1-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f1b1-111">**Chaîne** contenant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-111">**String** containing the attribute name.</span></span> <span data-ttu-id="1f1b1-112">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f1b1-113">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1f1b1-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f1b1-114">**Chaîne** contenant la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-114">**String** containing the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f1b1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f1b1-115">Return value</span></span>

<span data-ttu-id="1f1b1-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f1b1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1f1b1-117">Remarks</span></span>

<span data-ttu-id="1f1b1-118">La propriété **attributeCount** contient le nombre d’attributs disponibles pour un objet **multimédia** donné.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-118">The **attributeCount** property contains the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="1f1b1-119">Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer les noms des attributs intégrés qui peuvent être utilisés avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-119">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="1f1b1-120">Avant d’utiliser cette méthode, utilisez la méthode **isReadOnlyItem** pour déterminer si un attribut particulier peut être défini.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-120">Before using this method, use the **isReadOnlyItem** method to determine whether a particular attribute can be set.</span></span>

<span data-ttu-id="1f1b1-121">Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="1f1b1-122">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1f1b1-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="1f1b1-123">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="1f1b1-123">**Note**</span></span>

<span data-ttu-id="1f1b1-124">Si vous incorporez le contrôle du lecteur Windows Media dans votre application, les attributs de fichier que vous modifiez ne seront pas écrits dans le fichier multimédia numérique tant que l’utilisateur n’aura pas exécuté le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-124">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="1f1b1-125">Si vous utilisez le contrôle dans une application distante écrite en C++, les attributs de fichier que vous modifiez seront écrits dans le fichier multimédia numérique peu après que vous avez apporté les modifications.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-125">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="1f1b1-126">Dans les deux cas, les modifications sont immédiatement disponibles pour votre code via la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-126">In either case, the changes are immediately available to your code through the library.</span></span>

<span data-ttu-id="1f1b1-127">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-127">**Windows Media Player 10 Mobile:** This method is not implemented.</span></span>

## <a name="examples"></a><span data-ttu-id="1f1b1-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="1f1b1-128">Examples</span></span>

<span data-ttu-id="1f1b1-129">L’exemple JScript suivant utilise un *média*. **setItemInfo** pour modifier la valeur de l’attribut genre pour l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-129">The following JScript example uses *Media*.**setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="1f1b1-130">Un élément d’entrée de texte HTML nommé genText permet à l’utilisateur d’entrer une chaîne de texte, qui est ensuite utilisée pour modifier les informations d’attribut.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-130">An HTML TEXT input element named genText allows the user to enter a text string, which is then used to change the attribute information.</span></span> <span data-ttu-id="1f1b1-131">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="1f1b1-131">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

```



## <a name="requirements"></a><span data-ttu-id="1f1b1-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f1b1-132">Requirements</span></span>



| <span data-ttu-id="1f1b1-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f1b1-133">Requirement</span></span> | <span data-ttu-id="1f1b1-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f1b1-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1b1-135">Version</span><span class="sxs-lookup"><span data-stu-id="1f1b1-135">Version</span></span><br/> | <span data-ttu-id="1f1b1-136">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1f1b1-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1f1b1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1f1b1-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="1f1b1-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f1b1-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f1b1-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f1b1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1b1-140">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="1f1b1-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1f1b1-141">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="1f1b1-141">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="1f1b1-142">**Media. isReadOnlyItem**</span><span class="sxs-lookup"><span data-stu-id="1f1b1-142">**Media.isReadOnlyItem**</span></span>](media-isreadonlyitem.md)
</dt> <dt>

[<span data-ttu-id="1f1b1-143">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="1f1b1-143">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="1f1b1-144">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="1f1b1-144">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





