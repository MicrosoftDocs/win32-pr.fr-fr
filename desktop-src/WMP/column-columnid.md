---
title: COLUMN. columnID
description: L’attribut columnID spécifie ou récupère un ID de colonne dans le contrôle PLAYLIST.
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- COLUMN. columnID Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535002"
---
# <a name="columncolumnid"></a><span data-ttu-id="d3076-104">COLUMN. columnID</span><span class="sxs-lookup"><span data-stu-id="d3076-104">COLUMN.columnID</span></span>

<span data-ttu-id="d3076-105">L’attribut **ColumnID** spécifie ou récupère un ID de colonne dans le contrôle **playlist** .</span><span class="sxs-lookup"><span data-stu-id="d3076-105">The **columnID** attribute specifies or retrieves a column ID in the **PLAYLIST** control.</span></span>

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a><span data-ttu-id="d3076-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d3076-106">Possible Values</span></span>

<span data-ttu-id="d3076-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d3076-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3076-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d3076-108">Remarks</span></span>

<span data-ttu-id="d3076-109">Les valeurs **ColumnID** sont identiques à celles utilisées avec la méthode **getItemInfo** sur un objet **Media** .</span><span class="sxs-lookup"><span data-stu-id="d3076-109">The **columnID** values are the same values used with the **getItemInfo** method on a **Media** object.</span></span> <span data-ttu-id="d3076-110">Une liste peut être obtenue à l’aide du *média*. propriété **attributeCount** pour déterminer le nombre d’attributs disponibles pour un objet **multimédia** donné.</span><span class="sxs-lookup"><span data-stu-id="d3076-110">A list can be obtained by using the *Media*.**attributeCount** property to determine the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="d3076-111">Les numéros d’index peuvent ensuite être utilisés avec le *média*. méthode **getAttributeName** pour déterminer les noms des attributs, qui peuvent à leur tour être passés au *média*. **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="d3076-111">Index numbers can then be used with the *Media*.**getAttributeName** method to determine the names of the attributes, which can in turn be passed to *Media*.**getItemInfo**.</span></span> <span data-ttu-id="d3076-112">La propriété **ColumnID** ne peut être définie que sur ces valeurs, à l’exception de certaines valeurs qui ne peuvent pas être retournées par le *support*. **getAttributeName**.</span><span class="sxs-lookup"><span data-stu-id="d3076-112">The **columnID** property can only be set to these values, with the exception of some values that may not be returned by *Media*.**getAttributeName**.</span></span> <span data-ttu-id="d3076-113">Ces valeurs sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d3076-113">These values are listed below.</span></span>



| <span data-ttu-id="d3076-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3076-114">Value</span></span>     | <span data-ttu-id="d3076-115">Description</span><span class="sxs-lookup"><span data-stu-id="d3076-115">Description</span></span>                                                                        |
|-----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3076-116">name</span><span class="sxs-lookup"><span data-stu-id="d3076-116">name</span></span>      | <span data-ttu-id="d3076-117">Affiche le nom de l’objet **multimédia** .</span><span class="sxs-lookup"><span data-stu-id="d3076-117">Displays the name of the **Media** object.</span></span>                                         |
| <span data-ttu-id="d3076-118">duration</span><span class="sxs-lookup"><span data-stu-id="d3076-118">duration</span></span>  | <span data-ttu-id="d3076-119">Affiche la durée de l’objet **multimédia** .</span><span class="sxs-lookup"><span data-stu-id="d3076-119">Displays the duration of the **Media** object.</span></span>                                     |
| <span data-ttu-id="d3076-120">sourceURL</span><span class="sxs-lookup"><span data-stu-id="d3076-120">sourceURL</span></span> | <span data-ttu-id="d3076-121">Affiche l’URL de l’objet **multimédia** .</span><span class="sxs-lookup"><span data-stu-id="d3076-121">Displays the URL of the **Media** object.</span></span>                                          |
| <span data-ttu-id="d3076-122">status</span><span class="sxs-lookup"><span data-stu-id="d3076-122">status</span></span>    | <span data-ttu-id="d3076-123">Affiche l’état de la copie des fichiers.</span><span class="sxs-lookup"><span data-stu-id="d3076-123">Displays the status of copying files.</span></span>                                              |
| <span data-ttu-id="d3076-124">est</span><span class="sxs-lookup"><span data-stu-id="d3076-124">size</span></span>      | <span data-ttu-id="d3076-125">Affiche la taille du fichier représenté par l’objet **multimédia** .</span><span class="sxs-lookup"><span data-stu-id="d3076-125">Displays the size of the file that the **Media** object represents.</span></span>                |
| <span data-ttu-id="d3076-126">extension</span><span class="sxs-lookup"><span data-stu-id="d3076-126">extension</span></span> | <span data-ttu-id="d3076-127">Affiche l’extension de nom de fichier du fichier que l’objet **multimédia** représente.</span><span class="sxs-lookup"><span data-stu-id="d3076-127">Displays the file name extension of the file that the **Media** object represents.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d3076-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3076-128">Requirements</span></span>



| <span data-ttu-id="d3076-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3076-129">Requirement</span></span> | <span data-ttu-id="d3076-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3076-130">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="d3076-131">Version</span><span class="sxs-lookup"><span data-stu-id="d3076-131">Version</span></span><br/> | <span data-ttu-id="d3076-132">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d3076-132">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3076-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3076-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3076-134">**Élément COLUMN**</span><span class="sxs-lookup"><span data-stu-id="d3076-134">**COLUMN Element**</span></span>](column-element.md)
</dt> <dt>

[<span data-ttu-id="d3076-135">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="d3076-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="d3076-136">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="d3076-136">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="d3076-137">**Media. getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="d3076-137">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="d3076-138">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="d3076-138">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> </dl>

 

 





