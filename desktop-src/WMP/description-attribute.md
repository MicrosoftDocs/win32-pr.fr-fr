---
title: Description, attribut (kit de développement logiciel (SDK) WMP)
description: L’attribut Description est une description du contenu.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Description attribute Windows Media Player
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530442"
---
# <a name="description-attribute"></a><span data-ttu-id="fa2c6-104">Description (attribut)</span><span class="sxs-lookup"><span data-stu-id="fa2c6-104">Description Attribute</span></span>

<span data-ttu-id="fa2c6-105">L’attribut **Description** est une description du contenu.</span><span class="sxs-lookup"><span data-stu-id="fa2c6-105">The **Description** attribute is a description of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="fa2c6-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="fa2c6-106">Applies To</span></span>

-   [<span data-ttu-id="fa2c6-107">Fichiers musicaux</span><span class="sxs-lookup"><span data-stu-id="fa2c6-107">Music Files</span></span>](music-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="fa2c6-108">Notes</span><span class="sxs-lookup"><span data-stu-id="fa2c6-108">Remarks</span></span>

<span data-ttu-id="fa2c6-109">Cet attribut est stocké dans des fichiers musicaux, et non dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="fa2c6-109">This attribute is stored in music files, not in the library.</span></span>

<span data-ttu-id="fa2c6-110">Cet attribut peut avoir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="fa2c6-110">This attribute may have multiple values.</span></span> <span data-ttu-id="fa2c6-111">Pour récupérer toutes les valeurs d’un attribut à valeurs multiples, vous devez utiliser le *média*. méthode **getItemInfoByType** , et non la méthode *Media*. getItemInfo.</span><span class="sxs-lookup"><span data-stu-id="fa2c6-111">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.getItemInfo method.</span></span>

<span data-ttu-id="fa2c6-112">La constante du kit de développement logiciel (SDK) du format Windows Media pour cet attribut est g \_ wszWMDescription.</span><span class="sxs-lookup"><span data-stu-id="fa2c6-112">The Windows Media Format SDK constant for this attribute is g\_wszWMDescription.</span></span>

<span data-ttu-id="fa2c6-113">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="fa2c6-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa2c6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa2c6-114">Requirements</span></span>



| <span data-ttu-id="fa2c6-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa2c6-115">Requirement</span></span> | <span data-ttu-id="fa2c6-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa2c6-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="fa2c6-117">Version</span><span class="sxs-lookup"><span data-stu-id="fa2c6-117">Version</span></span><br/> | <span data-ttu-id="fa2c6-118">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fa2c6-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa2c6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa2c6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa2c6-120">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="fa2c6-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





