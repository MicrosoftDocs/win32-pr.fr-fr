---
description: Type de cet élément. Lecture seule.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Item. ItemType, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518267"
---
# <a name="itemitemtype-property"></a><span data-ttu-id="ed0d7-104">Item. ItemType, propriété</span><span class="sxs-lookup"><span data-stu-id="ed0d7-104">Item.ItemType property</span></span>

<span data-ttu-id="ed0d7-105">Type de cet élément.</span><span class="sxs-lookup"><span data-stu-id="ed0d7-105">The type of this item.</span></span> <span data-ttu-id="ed0d7-106">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ed0d7-106">Read-only.</span></span>

<span data-ttu-id="ed0d7-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ed0d7-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed0d7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed0d7-108">Syntax</span></span>


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a><span data-ttu-id="ed0d7-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ed0d7-109">Property value</span></span>

<span data-ttu-id="ed0d7-110">Les valeurs suivantes sont possibles :</span><span class="sxs-lookup"><span data-stu-id="ed0d7-110">The following values are possible:</span></span>



| <span data-ttu-id="ed0d7-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed0d7-111">Value</span></span>  | <span data-ttu-id="ed0d7-112">Description</span><span class="sxs-lookup"><span data-stu-id="ed0d7-112">Description</span></span>                                     |
|--------|-------------------------------------------------|
| <span data-ttu-id="ed0d7-113">device</span><span class="sxs-lookup"><span data-stu-id="ed0d7-113">device</span></span> | <span data-ttu-id="ed0d7-114">L’élément est un périphérique matériel WIA.</span><span class="sxs-lookup"><span data-stu-id="ed0d7-114">The item is a WIA hardware device.</span></span>              |
| <span data-ttu-id="ed0d7-115">dossier</span><span class="sxs-lookup"><span data-stu-id="ed0d7-115">folder</span></span> | <span data-ttu-id="ed0d7-116">L’élément est un dossier qui contient d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="ed0d7-116">The item is a folder that contains other items.</span></span> |
| <span data-ttu-id="ed0d7-117">fichier</span><span class="sxs-lookup"><span data-stu-id="ed0d7-117">file</span></span>   | <span data-ttu-id="ed0d7-118">L’élément est un fichier image ou audio.</span><span class="sxs-lookup"><span data-stu-id="ed0d7-118">The item is an image or audio file.</span></span>             |
| <span data-ttu-id="ed0d7-119">audio</span><span class="sxs-lookup"><span data-stu-id="ed0d7-119">audio</span></span>  | <span data-ttu-id="ed0d7-120">L’élément est un clip audio.</span><span class="sxs-lookup"><span data-stu-id="ed0d7-120">The item is an audio clip.</span></span>                      |
| <span data-ttu-id="ed0d7-121">image</span><span class="sxs-lookup"><span data-stu-id="ed0d7-121">image</span></span>  | <span data-ttu-id="ed0d7-122">L’élément est une image.</span><span class="sxs-lookup"><span data-stu-id="ed0d7-122">The item is an image.</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="ed0d7-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ed0d7-123">Remarks</span></span>

<span data-ttu-id="ed0d7-124">Un élément peut avoir plusieurs types.</span><span class="sxs-lookup"><span data-stu-id="ed0d7-124">An item can have more than one type.</span></span> <span data-ttu-id="ed0d7-125">Par exemple, chaque image est de type « image » et « fichier ».</span><span class="sxs-lookup"><span data-stu-id="ed0d7-125">For example, every image is of both "image" and "file" types.</span></span> <span data-ttu-id="ed0d7-126">**ItemType** retourne une chaîne qui comprend tous les types valides pour l’élément, séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="ed0d7-126">**ItemType** returns a string that includes all valid types for the item, separated by semicolons.</span></span> <span data-ttu-id="ed0d7-127">Par exemple, « image ; fichier ».</span><span class="sxs-lookup"><span data-stu-id="ed0d7-127">For example, "image;file".</span></span> <span data-ttu-id="ed0d7-128">Il n’y a pas d’espace dans cette chaîne, et il n’y a pas de point-virgule à la fin.</span><span class="sxs-lookup"><span data-stu-id="ed0d7-128">There are no spaces in this string, and there is not a semicolon at the end.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed0d7-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed0d7-129">Requirements</span></span>



| <span data-ttu-id="ed0d7-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed0d7-130">Requirement</span></span> | <span data-ttu-id="ed0d7-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed0d7-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed0d7-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed0d7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ed0d7-133">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed0d7-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed0d7-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed0d7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ed0d7-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed0d7-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ed0d7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ed0d7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed0d7-137"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="ed0d7-137"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




