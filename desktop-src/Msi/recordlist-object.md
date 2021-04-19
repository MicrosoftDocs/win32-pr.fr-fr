---
description: L’objet RecordList est une collection d’objets record. Vous devez vérifier que l’objet RecordList existe et qu’il n’est pas vide avant de référencer ses propriétés.
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: Objet RecordList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3f09887333d8ddbf83de4bea2b2e654411883e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537803"
---
# <a name="recordlist-object"></a><span data-ttu-id="758c6-104">Objet RecordList</span><span class="sxs-lookup"><span data-stu-id="758c6-104">RecordList object</span></span>

<span data-ttu-id="758c6-105">L’objet **RecordList** est une collection d’objets [**Record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="758c6-105">The **RecordList** object is a collection of [**Record**](record-object.md) objects.</span></span> <span data-ttu-id="758c6-106">Vous devez vérifier que l’objet **RecordList** existe et qu’il n’est pas vide avant de référencer ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="758c6-106">You must verify that the **RecordList** object exists and is not empty before referencing its properties.</span></span>

## <a name="members"></a><span data-ttu-id="758c6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="758c6-107">Members</span></span>

<span data-ttu-id="758c6-108">L’objet **RecordList** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="758c6-108">The **RecordList** object has these types of members:</span></span>

-   [<span data-ttu-id="758c6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="758c6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="758c6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="758c6-110">Properties</span></span>

<span data-ttu-id="758c6-111">L’objet **RecordList** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="758c6-111">The **RecordList** object has these properties.</span></span>



| <span data-ttu-id="758c6-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="758c6-112">Property</span></span>                                     | <span data-ttu-id="758c6-113">Description</span><span class="sxs-lookup"><span data-stu-id="758c6-113">Description</span></span>                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="758c6-114">**Saut**</span><span class="sxs-lookup"><span data-stu-id="758c6-114">**Count**</span></span>](recordlist-count.md)<br/> | <span data-ttu-id="758c6-115">Retourne le nombre d’éléments dans l’objet **RecordList** .</span><span class="sxs-lookup"><span data-stu-id="758c6-115">Returns the number of items in the **RecordList** object.</span></span><br/> |
| [<span data-ttu-id="758c6-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="758c6-116">**Item**</span></span>](recordlist-item.md)<br/>   | <span data-ttu-id="758c6-117">Retourne un enregistrement dans une collection d’objets **RecordList** .</span><span class="sxs-lookup"><span data-stu-id="758c6-117">Returns a record in a **RecordList** object collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="758c6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="758c6-118">Requirements</span></span>



| <span data-ttu-id="758c6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="758c6-119">Requirement</span></span> | <span data-ttu-id="758c6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="758c6-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="758c6-121">Version</span><span class="sxs-lookup"><span data-stu-id="758c6-121">Version</span></span><br/> | <span data-ttu-id="758c6-122">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="758c6-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="758c6-123">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="758c6-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="758c6-124">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="758c6-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="758c6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="758c6-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="758c6-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="758c6-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="758c6-127">IID</span><span class="sxs-lookup"><span data-stu-id="758c6-127">IID</span></span><br/>     | <span data-ttu-id="758c6-128">IID \_ IRecordList est défini en tant que 000C1096-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="758c6-128">IID\_IRecordList is defined as 000C1096-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="758c6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="758c6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="758c6-130">**Enregistrement**</span><span class="sxs-lookup"><span data-stu-id="758c6-130">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="758c6-131">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="758c6-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




