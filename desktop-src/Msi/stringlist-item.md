---
description: La propriété Item est une propriété en lecture seule qui retourne une chaîne dans la collection d’objets StringList.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: StringList. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541423"
---
# <a name="stringlistitem-property"></a><span data-ttu-id="ea8cd-103">StringList. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="ea8cd-103">StringList.Item property</span></span>

<span data-ttu-id="ea8cd-104">La propriété **Item** est une propriété en lecture seule qui retourne une chaîne dans la collection d' [**objets StringList**](stringlist-object.md) .</span><span class="sxs-lookup"><span data-stu-id="ea8cd-104">The **Item** property is a read-only property that returns a string in the [**StringList Object**](stringlist-object.md) collection.</span></span>

<span data-ttu-id="ea8cd-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8cd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea8cd-106">Syntax</span></span>


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a><span data-ttu-id="ea8cd-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ea8cd-107">Property value</span></span>

<span data-ttu-id="ea8cd-108">Numéro d’index de l’élément avec la collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="ea8cd-109">Ce paramètre est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea8cd-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ea8cd-110">Remarks</span></span>

<span data-ttu-id="ea8cd-111">Le client doit vérifier que l' [**objet StringList**](stringlist-object.md) existe et n’est pas vide avant de référencer la propriété **Item** .</span><span class="sxs-lookup"><span data-stu-id="ea8cd-111">The client must verify that the [**StringList Object**](stringlist-object.md) exists and is not empty before referencing the **Item** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8cd-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea8cd-112">Requirements</span></span>



| <span data-ttu-id="ea8cd-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea8cd-113">Requirement</span></span> | <span data-ttu-id="ea8cd-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea8cd-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8cd-115">Version</span><span class="sxs-lookup"><span data-stu-id="ea8cd-115">Version</span></span><br/> | <span data-ttu-id="ea8cd-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ea8cd-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ea8cd-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ea8cd-118">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="ea8cd-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="ea8cd-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ea8cd-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="ea8cd-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cd-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="ea8cd-121">IID</span><span class="sxs-lookup"><span data-stu-id="ea8cd-121">IID</span></span><br/>     | <span data-ttu-id="ea8cd-122">IID \_ IStringList est défini en tant que 000C1095-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ea8cd-122">IID\_IStringList is defined as 000C1095-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




