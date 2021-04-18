---
title: StringCollection. getItemInfo, méthode
description: La méthode getItemInfo récupère la chaîne correspondant au nom et à l’index d’élément StringCollection spécifiés.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo Player Windows Media, StringCollection Class
- StringCollection, classe Windows Media Player, méthode getItemInfo
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533301"
---
# <a name="stringcollectiongetiteminfo-method"></a><span data-ttu-id="81c73-106">StringCollection. getItemInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="81c73-106">StringCollection.getItemInfo method</span></span>

<span data-ttu-id="81c73-107">La méthode **getItemInfo** récupère la chaîne correspondant au nom et à l’index d’élément **StringCollection** spécifiés.</span><span class="sxs-lookup"><span data-stu-id="81c73-107">The **getItemInfo** method retrieves the string corresponding to the specified **StringCollection** item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="81c73-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81c73-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="81c73-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81c73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81c73-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81c73-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81c73-111">**Number** (**long**) spécifiant l’index de base zéro de l’élément **StringCollection** à partir duquel l’attribut doit être obtenu.</span><span class="sxs-lookup"><span data-stu-id="81c73-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="81c73-112">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81c73-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81c73-113">**Chaîne** contenant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="81c73-113">**String** containing the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81c73-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81c73-114">Return value</span></span>

<span data-ttu-id="81c73-115">Cette méthode retourne une **chaîne** représentant la valeur de l’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="81c73-115">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="81c73-116">Pour les attributs dont la valeur sous-jacente est **booléenne**, elle retourne la chaîne « true » ou « false ».</span><span class="sxs-lookup"><span data-stu-id="81c73-116">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="81c73-117">Notes</span><span class="sxs-lookup"><span data-stu-id="81c73-117">Remarks</span></span>

<span data-ttu-id="81c73-118">Pour récupérer des attributs avec plusieurs valeurs et attributs avec des valeurs complexes, utilisez la méthode **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="81c73-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="81c73-119">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="81c73-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="81c73-120">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="81c73-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81c73-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81c73-121">Requirements</span></span>



| <span data-ttu-id="81c73-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81c73-122">Requirement</span></span> | <span data-ttu-id="81c73-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="81c73-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81c73-124">Version</span><span class="sxs-lookup"><span data-stu-id="81c73-124">Version</span></span><br/> | <span data-ttu-id="81c73-125">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="81c73-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="81c73-126">DLL</span><span class="sxs-lookup"><span data-stu-id="81c73-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="81c73-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81c73-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81c73-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81c73-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81c73-129">**StringCollection. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="81c73-129">**StringCollection.getItemInfoByType**</span></span>](stringcollection-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="81c73-130">**StringCollection, objet**</span><span class="sxs-lookup"><span data-stu-id="81c73-130">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





