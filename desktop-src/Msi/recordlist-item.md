---
description: La propriété Item est une propriété en lecture seule qui retourne un enregistrement dans une collection d’objets RecordList.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: RecordList. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523644"
---
# <a name="recordlistitem-property"></a><span data-ttu-id="9b30a-103">RecordList. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="9b30a-103">RecordList.Item property</span></span>

<span data-ttu-id="9b30a-104">La propriété **Item** est une propriété en lecture seule qui retourne un enregistrement dans une collection d’objets [**RecordList**](recordlist-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9b30a-104">The **Item** property is a read-only property that returns a record in a [**RecordList**](recordlist-object.md) Object collection.</span></span>

<span data-ttu-id="9b30a-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9b30a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b30a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b30a-106">Syntax</span></span>


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a><span data-ttu-id="9b30a-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9b30a-107">Property value</span></span>

<span data-ttu-id="9b30a-108">Numéro d’index de l’élément avec la collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="9b30a-108">Index number of the item with the collection of strings.</span></span> <span data-ttu-id="9b30a-109">L’index est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9b30a-109">Index is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b30a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9b30a-110">Remarks</span></span>

<span data-ttu-id="9b30a-111">Le client doit vérifier que l’objet [**RecordList**](recordlist-object.md) existe et n’est pas vide avant de référencer la propriété Item.</span><span class="sxs-lookup"><span data-stu-id="9b30a-111">The client must verify that the [**RecordList**](recordlist-object.md) object exists and is not empty before referencing the Item property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b30a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b30a-112">Requirements</span></span>



| <span data-ttu-id="9b30a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b30a-113">Requirement</span></span> | <span data-ttu-id="9b30a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b30a-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b30a-115">Version</span><span class="sxs-lookup"><span data-stu-id="9b30a-115">Version</span></span><br/> | <span data-ttu-id="9b30a-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9b30a-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9b30a-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9b30a-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9b30a-118">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="9b30a-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9b30a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9b30a-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="9b30a-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b30a-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9b30a-121">IID</span><span class="sxs-lookup"><span data-stu-id="9b30a-121">IID</span></span><br/>     | <span data-ttu-id="9b30a-122">IID \_ IRecordList est défini en tant que 000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9b30a-122">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



 

 




