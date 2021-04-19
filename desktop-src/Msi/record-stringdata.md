---
description: La propriété StringData de l’objet record est une propriété en lecture-écriture qui transfère les données de chaîne vers ou à partir d’un champ spécifié dans l’enregistrement. Si un entier ou un objet a été stocké, sa valeur de chaîne est retournée.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Record. StringData, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530539"
---
# <a name="recordstringdata-property"></a><span data-ttu-id="feb2f-104">Record. StringData, propriété</span><span class="sxs-lookup"><span data-stu-id="feb2f-104">Record.StringData property</span></span>

<span data-ttu-id="feb2f-105">La propriété **StringData** de l’objet [**Record**](record-object.md) est une propriété en lecture-écriture qui transfère les données de chaîne vers ou à partir d’un champ spécifié dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="feb2f-105">The **StringData** property of the [**Record**](record-object.md) object is a read-write property that transfers string data in to or out of a specified field within the record.</span></span> <span data-ttu-id="feb2f-106">Si un entier ou un objet a été stocké, sa valeur de chaîne est retournée.</span><span class="sxs-lookup"><span data-stu-id="feb2f-106">If an integer or object has been stored, its string value is returned.</span></span>

<span data-ttu-id="feb2f-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="feb2f-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb2f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="feb2f-108">Syntax</span></span>


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a><span data-ttu-id="feb2f-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="feb2f-109">Property value</span></span>

<span data-ttu-id="feb2f-110">Numéro de champ obligatoire de la valeur dans l’enregistrement, de base 1.</span><span class="sxs-lookup"><span data-stu-id="feb2f-110">Required field number of the value within the record, 1-based.</span></span>

## <a name="remarks"></a><span data-ttu-id="feb2f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="feb2f-111">Remarks</span></span>

<span data-ttu-id="feb2f-112">La valeur retournée d’un champ inexistant est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="feb2f-112">The returned value of a nonexistent field is an empty string.</span></span> <span data-ttu-id="feb2f-113">Pour définir un champ de chaîne d’enregistrement sur null, utilisez un variant vide ou une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="feb2f-113">To set a record string field to null, use either an empty variant or an empty string.</span></span> <span data-ttu-id="feb2f-114">Toute tentative de stockage d’une valeur dans un champ inexistant génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="feb2f-114">Attempting to store a value in a nonexistent field causes an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb2f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="feb2f-115">Requirements</span></span>



| <span data-ttu-id="feb2f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="feb2f-116">Requirement</span></span> | <span data-ttu-id="feb2f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="feb2f-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb2f-118">Version</span><span class="sxs-lookup"><span data-stu-id="feb2f-118">Version</span></span><br/> | <span data-ttu-id="feb2f-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="feb2f-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="feb2f-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="feb2f-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="feb2f-121">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="feb2f-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="feb2f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="feb2f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="feb2f-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="feb2f-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="feb2f-124">IID</span><span class="sxs-lookup"><span data-stu-id="feb2f-124">IID</span></span><br/>     | <span data-ttu-id="feb2f-125">IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="feb2f-125">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




