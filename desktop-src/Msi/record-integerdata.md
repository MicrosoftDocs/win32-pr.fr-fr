---
description: Il s’agit de la propriété IntegerData de l’objet record. Cette propriété en lecture-écriture transfère les données de type entier 32 bits dans vers ou à partir d’un champ spécifié dans l’enregistrement. Si une valeur de champ ne peut pas être convertie en un entier, msiDatabaseNullInteger est retourné.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Record. IntegerData, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526107"
---
# <a name="recordintegerdata-property"></a><span data-ttu-id="5afa9-105">Record. IntegerData, propriété</span><span class="sxs-lookup"><span data-stu-id="5afa9-105">Record.IntegerData property</span></span>

<span data-ttu-id="5afa9-106">Il s’agit de la propriété **IntegerData** de l’objet [**Record**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5afa9-106">This is the **IntegerData** property of the [**Record**](record-object.md) object.</span></span> <span data-ttu-id="5afa9-107">Cette propriété en lecture-écriture transfère les données de type entier 32 bits dans vers ou à partir d’un champ spécifié dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5afa9-107">This read-write property transfers 32-bit integer data in to or out of a specified field within the record.</span></span> <span data-ttu-id="5afa9-108">Si une valeur de champ ne peut pas être convertie en un entier, msiDatabaseNullInteger est retourné.</span><span class="sxs-lookup"><span data-stu-id="5afa9-108">If a field value cannot be converted to an integer, msiDatabaseNullInteger is returned.</span></span>

<span data-ttu-id="5afa9-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5afa9-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5afa9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5afa9-110">Syntax</span></span>


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="5afa9-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5afa9-111">Property value</span></span>

<span data-ttu-id="5afa9-112">Numéro de champ obligatoire de la valeur dans l’enregistrement, de base 1.</span><span class="sxs-lookup"><span data-stu-id="5afa9-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="5afa9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5afa9-113">Remarks</span></span>

<span data-ttu-id="5afa9-114">Pour définir un champ d’entier d’enregistrement sur null, utilisez msiDatabaseNullInteger.</span><span class="sxs-lookup"><span data-stu-id="5afa9-114">To set a record integer field to null, use msiDatabaseNullInteger.</span></span> <span data-ttu-id="5afa9-115">La valeur retournée d’un champ inexistant est msiDatabaseNullInteger.</span><span class="sxs-lookup"><span data-stu-id="5afa9-115">The returned value of a nonexistent field is msiDatabaseNullInteger.</span></span> <span data-ttu-id="5afa9-116">Toute tentative de stockage d’une valeur dans un champ inexistant génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="5afa9-116">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5afa9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5afa9-117">Requirements</span></span>



| <span data-ttu-id="5afa9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5afa9-118">Requirement</span></span> | <span data-ttu-id="5afa9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5afa9-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5afa9-120">Version</span><span class="sxs-lookup"><span data-stu-id="5afa9-120">Version</span></span><br/> | <span data-ttu-id="5afa9-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5afa9-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5afa9-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5afa9-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5afa9-123">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="5afa9-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5afa9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5afa9-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="5afa9-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5afa9-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5afa9-126">IID</span><span class="sxs-lookup"><span data-stu-id="5afa9-126">IID</span></span><br/>     | <span data-ttu-id="5afa9-127">IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5afa9-127">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




