---
title: Méthode Media. getAttributeCountByType
description: La méthode getAttributeCountByType récupère le nombre d’attributs associés au nom et à la langue de l’attribut spécifiés.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- méthode getAttributeCountByType lecteur Windows Media
- méthode getAttributeCountByType lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode getAttributeCountByType
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525630"
---
# <a name="mediagetattributecountbytype-method"></a><span data-ttu-id="d2fd3-106">Méthode Media. getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="d2fd3-106">Media.getAttributeCountByType method</span></span>

<span data-ttu-id="d2fd3-107">La méthode **getAttributeCountByType** récupère le nombre d’attributs associés au nom et à la langue de l’attribut spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d2fd3-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified attribute name and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2fd3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2fd3-108">Syntax</span></span>


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="d2fd3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2fd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2fd3-110">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2fd3-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2fd3-111">**Chaîne** contenant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="d2fd3-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="d2fd3-112">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d2fd3-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2fd3-113">*langue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2fd3-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2fd3-114">**Chaîne** représentant la langue.</span><span class="sxs-lookup"><span data-stu-id="d2fd3-114">**String** representing the language.</span></span> <span data-ttu-id="d2fd3-115">Si la valeur est définie sur null ou «» (chaîne vide), la chaîne de paramètres régionaux active est utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2fd3-115">If the value is set to null or "" (empty string), the current locale string is used.</span></span> <span data-ttu-id="d2fd3-116">Dans le cas contraire, la valeur doit être une chaîne valide du langage RFC 1766, par exemple « en-US ».</span><span class="sxs-lookup"><span data-stu-id="d2fd3-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2fd3-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2fd3-117">Return value</span></span>

<span data-ttu-id="d2fd3-118">Cette méthode retourne un **nombre** (**long**) contenant le nombre d’attributs.</span><span class="sxs-lookup"><span data-stu-id="d2fd3-118">This method returns a **Number** (**long**) containing the attribute count.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2fd3-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d2fd3-119">Remarks</span></span>

<span data-ttu-id="d2fd3-120">Cette méthode est utilisée pour déterminer le nombre d’attributs correspondant à un nom d’attribut particulier pour un objet **multimédia** donné.</span><span class="sxs-lookup"><span data-stu-id="d2fd3-120">This method is used to determine the number of attributes corresponding to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="d2fd3-121">Les numéros d’index peuvent ensuite être passés à la méthode **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="d2fd3-121">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="d2fd3-122">Cela est utile, par exemple, lorsqu’un élément multimédia a été catégorisé sous plusieurs genres.</span><span class="sxs-lookup"><span data-stu-id="d2fd3-122">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="d2fd3-123">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="d2fd3-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="d2fd3-124">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d2fd3-124">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="d2fd3-125">**Lecteur Windows Media 10 Mobile :** Cette propriété retourne toujours 0.</span><span class="sxs-lookup"><span data-stu-id="d2fd3-125">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2fd3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2fd3-126">Requirements</span></span>



| <span data-ttu-id="d2fd3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2fd3-127">Requirement</span></span> | <span data-ttu-id="d2fd3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2fd3-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2fd3-129">Version</span><span class="sxs-lookup"><span data-stu-id="d2fd3-129">Version</span></span><br/> | <span data-ttu-id="d2fd3-130">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d2fd3-130">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="d2fd3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d2fd3-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="d2fd3-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2fd3-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2fd3-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2fd3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2fd3-134">**MediaObject**</span><span class="sxs-lookup"><span data-stu-id="d2fd3-134">**MediaObject**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="d2fd3-135">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="d2fd3-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="d2fd3-136">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d2fd3-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="d2fd3-137">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d2fd3-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





