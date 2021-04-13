---
title: StringCollection, objet
description: L’objet StringCollection fournit un moyen de manipuler une collection de chaînes.
ms.assetid: bd4f82e7-1a6a-47c5-b019-7aff520e621a
keywords:
- Objet StringCollection lecteur Windows Media
topic_type:
- apiref
api_name:
- StringCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d1872bec7e00e87ada845f7518608ea4149f137
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313249"
---
# <a name="stringcollection-object"></a><span data-ttu-id="55040-104">StringCollection, objet</span><span class="sxs-lookup"><span data-stu-id="55040-104">StringCollection Object</span></span>

<span data-ttu-id="55040-105">L’objet **StringCollection** fournit un moyen de manipuler une collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="55040-105">The **StringCollection** object provides a way to manipulate a collection of strings.</span></span>

<span data-ttu-id="55040-106">L’objet **StringCollection** prend en charge la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="55040-106">The **StringCollection** object supports the following property.</span></span>



| <span data-ttu-id="55040-107">Propriété</span><span class="sxs-lookup"><span data-stu-id="55040-107">Property</span></span>                            | <span data-ttu-id="55040-108">Description</span><span class="sxs-lookup"><span data-stu-id="55040-108">Description</span></span>                                             |
|-------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="55040-109">count</span><span class="sxs-lookup"><span data-stu-id="55040-109">count</span></span>](stringcollection-count.md) | <span data-ttu-id="55040-110">Récupère le nombre d’éléments dans la collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="55040-110">Retrieves the number of items in the string collection.</span></span> |



 

<span data-ttu-id="55040-111">L’objet **StringCollection** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="55040-111">The **StringCollection** object supports the following methods.</span></span>



| <span data-ttu-id="55040-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="55040-112">Method</span></span>                                                                  | <span data-ttu-id="55040-113">Description</span><span class="sxs-lookup"><span data-stu-id="55040-113">Description</span></span>                                                                                                                     |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55040-114">getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="55040-114">getAttributeCountByType</span></span>](stringcollection-getattributecountbytype.md) | <span data-ttu-id="55040-115">Récupère le nombre d’attributs associés à l’index d’élément **StringCollection** , le nom d’attribut et la langue spécifiés.</span><span class="sxs-lookup"><span data-stu-id="55040-115">Retrieves the number of attributes associated with the specified **StringCollection** item index, attribute name, and language.</span></span> |
| [<span data-ttu-id="55040-116">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="55040-116">getItemInfo</span></span>](stringcollection-getiteminfo.md)                         | <span data-ttu-id="55040-117">Récupère la chaîne correspondant au nom et à l’index d’élément **StringCollection** spécifiés.</span><span class="sxs-lookup"><span data-stu-id="55040-117">Retrieves the string corresponding to the specified **StringCollection** item index and name.</span></span>                                   |
| [<span data-ttu-id="55040-118">getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="55040-118">getItemInfoByType</span></span>](stringcollection-getiteminfobytype.md)             | <span data-ttu-id="55040-119">Récupère la chaîne correspondant à l’index d’élément **StringCollection** , au nom, à la langue et à l’index d’attribut spécifiés.</span><span class="sxs-lookup"><span data-stu-id="55040-119">Retrieves the string corresponding to the specified **StringCollection** item index, name, language, and attribute index.</span></span>       |
| [<span data-ttu-id="55040-120">isIdentical</span><span class="sxs-lookup"><span data-stu-id="55040-120">isIdentical</span></span>](stringcollection-isidentical.md)                         | <span data-ttu-id="55040-121">Récupère une valeur indiquant si l’objet fourni est identique à l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="55040-121">Retrieves a value indicating whether the supplied object is the same as the current one.</span></span>                                        |
| [<span data-ttu-id="55040-122">item</span><span class="sxs-lookup"><span data-stu-id="55040-122">item</span></span>](stringcollection-item.md)                                       | <span data-ttu-id="55040-123">Récupère la chaîne à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="55040-123">Retrieves the string at the specified index.</span></span>                                                                                    |



 

<span data-ttu-id="55040-124">L’objet **StringCollection** est accessible par le biais de la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="55040-124">The **StringCollection** object is accessed through the following method.</span></span>



| <span data-ttu-id="55040-125">Object</span><span class="sxs-lookup"><span data-stu-id="55040-125">Object</span></span>                                        | <span data-ttu-id="55040-126">Méthode</span><span class="sxs-lookup"><span data-stu-id="55040-126">Method</span></span>                                                                           |
|-----------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="55040-127">MediaCollection</span><span class="sxs-lookup"><span data-stu-id="55040-127">MediaCollection</span></span>](mediacollection-object.md) | [<span data-ttu-id="55040-128">getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="55040-128">getAttributeStringCollection</span></span>](mediacollection-getattributestringcollection.md) |



 

<span data-ttu-id="55040-129">À des fins d’illustration, *joueur*. *mediaCollection*. **getAttributeStringCollection**(*attribute*, *MediaType*) est utilisé dans les sections de syntaxe de référence.</span><span class="sxs-lookup"><span data-stu-id="55040-129">For purposes of illustration, *player*.*mediaCollection*.**getAttributeStringCollection**(*attribute*, *mediaType*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="55040-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55040-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55040-131">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="55040-131">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




