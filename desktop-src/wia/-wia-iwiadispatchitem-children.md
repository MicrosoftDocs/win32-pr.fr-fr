---
description: La propriété Children de l’objet Item récupère une collection d’objets Item. Les éléments de cette collection représentent des éléments qui sont des enfants directs de cet élément dans l’arborescence hiérarchique. Lecture seule.
ms.assetid: 94ad3385-9ce9-4a44-87bb-1d7170c8d45c
title: Item. Children, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Children
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 144b60f1c8e9b500d49b53dfe290565c23023220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516925"
---
# <a name="itemchildren-property"></a><span data-ttu-id="29c7d-105">Item. Children, propriété</span><span class="sxs-lookup"><span data-stu-id="29c7d-105">Item.Children property</span></span>

<span data-ttu-id="29c7d-106">La propriété **Children** de l’objet [**Item**](-wia-item.md) récupère une collection d’objets **Item** .</span><span class="sxs-lookup"><span data-stu-id="29c7d-106">The **Children** property of the [**Item**](-wia-item.md) object retrieves a collection of **Item** objects.</span></span> <span data-ttu-id="29c7d-107">Les éléments de cette collection représentent des éléments qui sont des enfants directs de cet élément dans l’arborescence hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="29c7d-107">The items in this collection represent items that are direct children of this item in the hierarchical tree.</span></span> <span data-ttu-id="29c7d-108">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="29c7d-108">Read-only.</span></span>

<span data-ttu-id="29c7d-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="29c7d-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="29c7d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29c7d-110">Syntax</span></span>


```JScript
propVal = Item.Children
```



## <a name="property-value"></a><span data-ttu-id="29c7d-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="29c7d-111">Property value</span></span>

<span data-ttu-id="29c7d-112">Variable qui reçoit les objets.</span><span class="sxs-lookup"><span data-stu-id="29c7d-112">Variable that receives the objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="29c7d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="29c7d-113">Remarks</span></span>

<span data-ttu-id="29c7d-114">Utilisez cette propriété pour naviguer dans l’arborescence hiérarchique des objets d' [**élément**](-wia-item.md) qui représentent un périphérique, les dossiers et les fichiers qui résident sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="29c7d-114">Use this property to navigate the hierarchical tree of [**Item**](-wia-item.md) objects that represent a device, the folders and the files that reside on the device.</span></span>

<span data-ttu-id="29c7d-115">La propriété **Children** est une collection d’objets [**Item**](-wia-item.md) uniquement à partir du niveau situé juste au-dessous de cet objet **Item** dans l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="29c7d-115">The **Children** property is a collection of [**Item**](-wia-item.md) objects only from the level directly beneath this **Item** object in the tree.</span></span> <span data-ttu-id="29c7d-116">Pour naviguer dans les niveaux supérieurs de l’arborescence, utilisez cette propriété de manière récursive.</span><span class="sxs-lookup"><span data-stu-id="29c7d-116">To navigate further levels down the tree, use this property recursively.</span></span>

<span data-ttu-id="29c7d-117">Si l’élément ne peut pas ou n’a pas d’éléments enfants, cette propriété retourne une collection vide.</span><span class="sxs-lookup"><span data-stu-id="29c7d-117">If the item cannot or does not have any child items, this property returns an empty collection.</span></span>

> [!Note]  
> <span data-ttu-id="29c7d-118">Cette collection est de base 0.</span><span class="sxs-lookup"><span data-stu-id="29c7d-118">This collection is 0-based.</span></span>

 

## <a name="examples"></a><span data-ttu-id="29c7d-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="29c7d-119">Examples</span></span>

<span data-ttu-id="29c7d-120">L’exemple suivant illustre l’utilisation de la propriété **Children** pour récupérer et énumérer une collection d’éléments enfants d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="29c7d-120">The following example demonstrates the use of the **Children** property to retrieve and enumerate a collection of the child items of a device.</span></span> <span data-ttu-id="29c7d-121">Si l’appareil est un appareil photo numérique, le regroupement contient généralement des éléments de dossier et d’image.</span><span class="sxs-lookup"><span data-stu-id="29c7d-121">If the device is a digital camera, the collection typically contains folder and image items.</span></span> <span data-ttu-id="29c7d-122">Si l’appareil est un scanneur, le regroupement contient généralement des éléments qui représentent des lits d’analyse.</span><span class="sxs-lookup"><span data-stu-id="29c7d-122">If the device is a scanner, the collection typically contains items that represent scanning beds.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objItemCollection
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    objItemCollection = objRootItem.Children
    For Each objItem In objItemCollection
        ' Do something with the child item
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="29c7d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29c7d-123">Requirements</span></span>



| <span data-ttu-id="29c7d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29c7d-124">Requirement</span></span> | <span data-ttu-id="29c7d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="29c7d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29c7d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29c7d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="29c7d-127">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29c7d-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29c7d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29c7d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="29c7d-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29c7d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="29c7d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="29c7d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29c7d-131"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="29c7d-131"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




