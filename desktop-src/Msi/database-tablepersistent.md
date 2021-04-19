---
description: La propriété TablePersistent de l’objet de base de données retourne l’état de persistance de la table en tant que l’un des paramètres suivants.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Propriété Database. TablePersistent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528836"
---
# <a name="databasetablepersistent-property"></a><span data-ttu-id="1124b-103">Propriété Database. TablePersistent</span><span class="sxs-lookup"><span data-stu-id="1124b-103">Database.TablePersistent property</span></span>

<span data-ttu-id="1124b-104">La propriété **TablePersistent** de l’objet [**de base de données**](database-object.md) retourne l’état de persistance de la table en tant que l’un des paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="1124b-104">The **TablePersistent** property of the [**Database**](database-object.md) object returns the persistence state of the table as one of the following parameters.</span></span>



| <span data-ttu-id="1124b-105">État de la table</span><span class="sxs-lookup"><span data-stu-id="1124b-105">Table state</span></span>               | <span data-ttu-id="1124b-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="1124b-106">Value</span></span> | <span data-ttu-id="1124b-107">Description</span><span class="sxs-lookup"><span data-stu-id="1124b-107">Description</span></span>                    |
|---------------------------|-------|--------------------------------|
| <span data-ttu-id="1124b-108">msiEvaluateConditionFalse</span><span class="sxs-lookup"><span data-stu-id="1124b-108">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="1124b-109">0</span><span class="sxs-lookup"><span data-stu-id="1124b-109">0</span></span>     | <span data-ttu-id="1124b-110">La table est temporaire.</span><span class="sxs-lookup"><span data-stu-id="1124b-110">Table is temporary.</span></span>            |
| <span data-ttu-id="1124b-111">msiEvaluateConditionTrue</span><span class="sxs-lookup"><span data-stu-id="1124b-111">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="1124b-112">1</span><span class="sxs-lookup"><span data-stu-id="1124b-112">1</span></span>     | <span data-ttu-id="1124b-113">La table est persistante.</span><span class="sxs-lookup"><span data-stu-id="1124b-113">Table is persistent.</span></span>           |
| <span data-ttu-id="1124b-114">msiEvaluateConditionNone</span><span class="sxs-lookup"><span data-stu-id="1124b-114">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="1124b-115">2</span><span class="sxs-lookup"><span data-stu-id="1124b-115">2</span></span>     | <span data-ttu-id="1124b-116">La table n’est pas dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="1124b-116">Table is not in the database.</span></span>  |
| <span data-ttu-id="1124b-117">msiEvaluateConditionError</span><span class="sxs-lookup"><span data-stu-id="1124b-117">msiEvaluateConditionError</span></span> | <span data-ttu-id="1124b-118">3</span><span class="sxs-lookup"><span data-stu-id="1124b-118">3</span></span>     | <span data-ttu-id="1124b-119">Nom de table non valide ou manquant.</span><span class="sxs-lookup"><span data-stu-id="1124b-119">Invalid or missing table name.</span></span> |



 

<span data-ttu-id="1124b-120">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1124b-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1124b-121">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1124b-121">Syntax</span></span>


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a><span data-ttu-id="1124b-122">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1124b-122">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="1124b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1124b-123">Requirements</span></span>



| <span data-ttu-id="1124b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1124b-124">Requirement</span></span> | <span data-ttu-id="1124b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1124b-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1124b-126">Version</span><span class="sxs-lookup"><span data-stu-id="1124b-126">Version</span></span><br/> | <span data-ttu-id="1124b-127">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1124b-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1124b-128">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1124b-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1124b-129">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="1124b-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1124b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1124b-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="1124b-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1124b-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1124b-132">IID</span><span class="sxs-lookup"><span data-stu-id="1124b-132">IID</span></span><br/>     | <span data-ttu-id="1124b-133">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1124b-133">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




