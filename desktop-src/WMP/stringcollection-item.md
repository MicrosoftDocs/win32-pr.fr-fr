---
title: StringCollection. Item, méthode
description: La méthode Item récupère la chaîne à l’index spécifié.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- méthode Item lecteur Windows Media
- méthode Item lecteur Windows Media, StringCollection, classe
- StringCollection, classe Windows Media Player, méthode Item
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542434"
---
# <a name="stringcollectionitem-method"></a><span data-ttu-id="16df8-106">StringCollection. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="16df8-106">StringCollection.item method</span></span>

<span data-ttu-id="16df8-107">La méthode **Item** récupère la chaîne à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="16df8-107">The **item** method retrieves the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="16df8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16df8-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="16df8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16df8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16df8-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16df8-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16df8-111">**Nombre** (**long**) contenant l’index.</span><span class="sxs-lookup"><span data-stu-id="16df8-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16df8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16df8-112">Return value</span></span>

<span data-ttu-id="16df8-113">Cette méthode retourne une **chaîne**.</span><span class="sxs-lookup"><span data-stu-id="16df8-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="16df8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="16df8-114">Remarks</span></span>

<span data-ttu-id="16df8-115">L’objet **StringCollection** est utilisé pour récupérer l’ensemble de valeurs disponibles pour un attribut.</span><span class="sxs-lookup"><span data-stu-id="16df8-115">The **StringCollection** object is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="16df8-116">Par exemple, *MediaCollection*. la méthode **getAttributeStringCollection** peut être utilisée pour récupérer un objet **StringCollection** représentant toutes les valeurs de l’attribut genre dans le type de média audio.</span><span class="sxs-lookup"><span data-stu-id="16df8-116">For example, the *MediaCollection*.**getAttributeStringCollection** method can be used to retrieve a **StringCollection** object representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="16df8-117">La propriété **Item** peut ensuite être utilisée pour itérer au sein de toutes les valeurs possibles de l’attribut genre.</span><span class="sxs-lookup"><span data-stu-id="16df8-117">The **item** property can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="16df8-118">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="16df8-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="16df8-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="16df8-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16df8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16df8-120">Requirements</span></span>



| <span data-ttu-id="16df8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16df8-121">Requirement</span></span> | <span data-ttu-id="16df8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="16df8-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16df8-123">Version</span><span class="sxs-lookup"><span data-stu-id="16df8-123">Version</span></span><br/> | <span data-ttu-id="16df8-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="16df8-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="16df8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="16df8-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="16df8-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16df8-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16df8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16df8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16df8-128">**MediaCollection.getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="16df8-128">**MediaCollection.getAttributeStringCollection**</span></span>](mediacollection-getattributestringcollection.md)
</dt> <dt>

[<span data-ttu-id="16df8-129">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="16df8-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="16df8-130">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="16df8-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="16df8-131">**StringCollection, objet**</span><span class="sxs-lookup"><span data-stu-id="16df8-131">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





