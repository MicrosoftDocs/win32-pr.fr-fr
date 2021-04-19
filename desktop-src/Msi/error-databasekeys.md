---
description: La propriété DatabaseKeys en lecture seule de l’objet Error retourne une collection de chaînes qui contient les clés primaires de la ligne de base de données à l’origine de l’erreur. Il existe une clé par entrée dans la collection.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Erreur. DatabaseKeys, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532195"
---
# <a name="errordatabasekeys-property"></a><span data-ttu-id="53b5b-104">Error. DatabaseKeys, propriété</span><span class="sxs-lookup"><span data-stu-id="53b5b-104">Error.DatabaseKeys property</span></span>

<span data-ttu-id="53b5b-105">La propriété **DatabaseKeys** en lecture seule de l’objet [**Error**](error-object.md) retourne une collection de chaînes qui contient les clés primaires de la ligne de base de données à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="53b5b-105">The read-only **DatabaseKeys** property of the [**Error**](error-object.md) object returns a string collection that contains the primary keys of the database row causing the error.</span></span> <span data-ttu-id="53b5b-106">Il existe une clé par entrée dans la collection.</span><span class="sxs-lookup"><span data-stu-id="53b5b-106">There is one key per entry in the collection.</span></span>

<span data-ttu-id="53b5b-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="53b5b-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b5b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53b5b-108">Syntax</span></span>


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a><span data-ttu-id="53b5b-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="53b5b-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="53b5b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="53b5b-110">Remarks</span></span>

<span data-ttu-id="53b5b-111">Le client est responsable de la libération de la collection de chaînes lorsqu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="53b5b-111">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="53b5b-112">La collection est vide si les valeurs ne s’appliquent pas au type de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="53b5b-112">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="53b5b-113">Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="53b5b-113">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="53b5b-114">C++</span><span class="sxs-lookup"><span data-stu-id="53b5b-114">C++</span></span>

<span data-ttu-id="53b5b-115">Consultez la fonction [**obtenir \_ DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) .</span><span class="sxs-lookup"><span data-stu-id="53b5b-115">See [**get\_DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="53b5b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53b5b-116">Requirements</span></span>



| <span data-ttu-id="53b5b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53b5b-117">Requirement</span></span> | <span data-ttu-id="53b5b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="53b5b-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53b5b-119">Version</span><span class="sxs-lookup"><span data-stu-id="53b5b-119">Version</span></span><br/> | <span data-ttu-id="53b5b-120">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="53b5b-120">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="53b5b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="53b5b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="53b5b-122"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="53b5b-122"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="53b5b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="53b5b-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="53b5b-124"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53b5b-124"><dt>Mergemod.dll</dt></span></span> </dl> |



 

