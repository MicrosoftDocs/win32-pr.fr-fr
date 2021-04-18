---
title: AmbientAttributes. tabStop
description: L’attribut tabStop spécifie ou récupère une valeur indiquant si le contrôle est dans l’ordre de tabulation. Vous définissez l’ordre de tabulation en plaçant le contrôle dans le script global avant ou après d’autres balises de contrôle.
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- AmbientAttributes. tabStop lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526842"
---
# <a name="ambientattributestabstop"></a><span data-ttu-id="4e588-105">AmbientAttributes. tabStop</span><span class="sxs-lookup"><span data-stu-id="4e588-105">AmbientAttributes.tabStop</span></span>

<span data-ttu-id="4e588-106">L’attribut **tabStop** spécifie ou récupère une valeur indiquant si le contrôle est dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="4e588-106">The **tabStop** attribute specifies or retrieves a value indicating whether the control is in the tabbing order.</span></span> <span data-ttu-id="4e588-107">Vous définissez l’ordre de tabulation en plaçant le contrôle dans le script global avant ou après d’autres balises de contrôle.</span><span class="sxs-lookup"><span data-stu-id="4e588-107">You set the tabbing order by placing the control in the overall script before or after other control tags.</span></span>

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a><span data-ttu-id="4e588-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="4e588-108">Possible Values</span></span>

<span data-ttu-id="4e588-109">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4e588-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="4e588-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e588-110">Value</span></span> | <span data-ttu-id="4e588-111">Description</span><span class="sxs-lookup"><span data-stu-id="4e588-111">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e588-112">true</span><span class="sxs-lookup"><span data-stu-id="4e588-112">true</span></span>  | <span data-ttu-id="4e588-113">Le contrôle se trouve dans l’ordre de tabulation (le contrôle aura un taquet de tabulation : exigence d’accessibilité).</span><span class="sxs-lookup"><span data-stu-id="4e588-113">Control is in the tabbing order (control will have a tab stop: accessibility requirement).</span></span> |
| <span data-ttu-id="4e588-114">false</span><span class="sxs-lookup"><span data-stu-id="4e588-114">false</span></span> | <span data-ttu-id="4e588-115">Le contrôle n’est pas dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="4e588-115">Control is not in the tabbing order.</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="4e588-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4e588-116">Remarks</span></span>

<span data-ttu-id="4e588-117">L’attribut **tabStop** n’est pas applicable à l’élément **Effects** .</span><span class="sxs-lookup"><span data-stu-id="4e588-117">The **tabStop** attribute is not applicable to the **EFFECTS** element.</span></span>

<span data-ttu-id="4e588-118">La valeur par défaut de cet attribut est true pour tous les éléments, à l’exception du **menu** automatique et du **texte**, dont la valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="4e588-118">The default value for this attribute is true for all elements except **AUTOMENU** and **TEXT**, which have a default value of false.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e588-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e588-119">Requirements</span></span>



| <span data-ttu-id="4e588-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e588-120">Requirement</span></span> | <span data-ttu-id="4e588-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e588-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4e588-122">Version</span><span class="sxs-lookup"><span data-stu-id="4e588-122">Version</span></span><br/> | <span data-ttu-id="4e588-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="4e588-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e588-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e588-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e588-125">**Attributs ambiants**</span><span class="sxs-lookup"><span data-stu-id="4e588-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





