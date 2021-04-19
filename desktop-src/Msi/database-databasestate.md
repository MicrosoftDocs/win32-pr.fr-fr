---
description: La propriété DatabaseState de l’objet de base de données est une propriété en lecture seule.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Propriété Database. DatabaseState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537436"
---
# <a name="databasedatabasestate-property"></a><span data-ttu-id="331a6-103">Propriété Database. DatabaseState</span><span class="sxs-lookup"><span data-stu-id="331a6-103">Database.DatabaseState property</span></span>

<span data-ttu-id="331a6-104">La propriété **DatabaseState** de l’objet [**de base de données**](database-object.md) est une propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="331a6-104">The **DatabaseState** property of the [**Database**](database-object.md) object is a read-only property.</span></span>

<span data-ttu-id="331a6-105">Cette propriété retourne l’état de persistance de la base de données sous la forme de l’un des paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="331a6-105">This property returns the persistence state of the database as one of the following parameters.</span></span>



| <span data-ttu-id="331a6-106">État de la base de données</span><span class="sxs-lookup"><span data-stu-id="331a6-106">Database state</span></span>        | <span data-ttu-id="331a6-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="331a6-107">Value</span></span> | <span data-ttu-id="331a6-108">Description</span><span class="sxs-lookup"><span data-stu-id="331a6-108">Description</span></span>                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="331a6-109">msiDatabaseStateRead</span><span class="sxs-lookup"><span data-stu-id="331a6-109">msiDatabaseStateRead</span></span>  | <span data-ttu-id="331a6-110">0</span><span class="sxs-lookup"><span data-stu-id="331a6-110">0</span></span>     | <span data-ttu-id="331a6-111">La base de données s’ouvre en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="331a6-111">Database opens as read-only.</span></span> <span data-ttu-id="331a6-112">Les modifications apportées aux données persistantes ne sont pas autorisées et les données temporaires ne sont pas enregistrées.</span><span class="sxs-lookup"><span data-stu-id="331a6-112">Changes to persistent data are not permitted and temporary data is not saved.</span></span> |
| <span data-ttu-id="331a6-113">msiDatabaseStateWrite</span><span class="sxs-lookup"><span data-stu-id="331a6-113">msiDatabaseStateWrite</span></span> | <span data-ttu-id="331a6-114">1</span><span class="sxs-lookup"><span data-stu-id="331a6-114">1</span></span>     | <span data-ttu-id="331a6-115">La base de données est entièrement opérationnelle pour la lecture et l’écriture.</span><span class="sxs-lookup"><span data-stu-id="331a6-115">Database is fully operational for read and write.</span></span>                                                          |



 

<span data-ttu-id="331a6-116">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="331a6-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="331a6-117">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="331a6-117">Syntax</span></span>


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a><span data-ttu-id="331a6-118">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="331a6-118">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="331a6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="331a6-119">Requirements</span></span>



| <span data-ttu-id="331a6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="331a6-120">Requirement</span></span> | <span data-ttu-id="331a6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="331a6-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="331a6-122">Version</span><span class="sxs-lookup"><span data-stu-id="331a6-122">Version</span></span><br/> | <span data-ttu-id="331a6-123">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="331a6-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="331a6-124">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="331a6-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="331a6-125">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="331a6-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="331a6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="331a6-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="331a6-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="331a6-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="331a6-128">IID</span><span class="sxs-lookup"><span data-stu-id="331a6-128">IID</span></span><br/>     | <span data-ttu-id="331a6-129">IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="331a6-129">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




