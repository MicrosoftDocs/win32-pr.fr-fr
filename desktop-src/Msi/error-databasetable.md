---
description: La propriété DatabaseTable en lecture seule de l’objet Error retourne le nom de la table dans la base de données qui a provoqué l’erreur.
ms.assetid: 38ff45ca-4bd6-43f3-88ad-db4077daeb77
title: Erreur. DatabaseTable, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseTable
- IMsmError.get_DatabaseTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8d7be883597d30059f6c949a800fe9803563c2b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537352"
---
# <a name="errordatabasetable-property"></a><span data-ttu-id="629dd-103">Error. DatabaseTable, propriété</span><span class="sxs-lookup"><span data-stu-id="629dd-103">Error.DatabaseTable property</span></span>

<span data-ttu-id="629dd-104">La propriété **DatabaseTable** en lecture seule de l’objet [**Error**](error-object.md) retourne le nom de la table dans la base de données qui a provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="629dd-104">The read-only **DatabaseTable** property of the [**Error**](error-object.md) object returns the name of the table in the database that caused the error.</span></span>

<span data-ttu-id="629dd-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="629dd-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="629dd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="629dd-106">Syntax</span></span>


```JScript
propVal = Error.DatabaseTable
```



## <a name="property-value"></a><span data-ttu-id="629dd-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="629dd-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="629dd-108">Notes</span><span class="sxs-lookup"><span data-stu-id="629dd-108">Remarks</span></span>

<span data-ttu-id="629dd-109">La collection est vide si les valeurs ne s’appliquent pas au type de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="629dd-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="629dd-110">Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="629dd-110">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="629dd-111">C++</span><span class="sxs-lookup"><span data-stu-id="629dd-111">C++</span></span>

<span data-ttu-id="629dd-112">Consultez la fonction [**obtenir \_ DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) .</span><span class="sxs-lookup"><span data-stu-id="629dd-112">See [**get\_DatabaseTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasetable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="629dd-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="629dd-113">Requirements</span></span>



| <span data-ttu-id="629dd-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="629dd-114">Requirement</span></span> | <span data-ttu-id="629dd-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="629dd-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="629dd-116">Version</span><span class="sxs-lookup"><span data-stu-id="629dd-116">Version</span></span><br/> | <span data-ttu-id="629dd-117">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="629dd-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="629dd-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="629dd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="629dd-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="629dd-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="629dd-120">DLL</span><span class="sxs-lookup"><span data-stu-id="629dd-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="629dd-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="629dd-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

