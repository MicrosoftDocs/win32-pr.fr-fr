---
description: La propriété des erreurs en lecture seule de l’objet Merge retourne une collection d’objets Error qui est le jeu actuel d’erreurs.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Merge. Errors, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9f07bdbba9fecf48001aed1fbcd42e02abb5c5c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532619"
---
# <a name="mergeerrors-property"></a><span data-ttu-id="1194d-103">Merge. Errors, propriété</span><span class="sxs-lookup"><span data-stu-id="1194d-103">Merge.Errors property</span></span>

<span data-ttu-id="1194d-104">La propriété des **Erreurs** en lecture seule de l’objet [**Merge**](merge-object.md) retourne une collection d’objets [**Error**](error-object.md) qui est le jeu actuel d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="1194d-104">The read-only **Errors** property of the [**Merge**](merge-object.md) object returns a collection of [**Error**](error-object.md) objects that is the current set of errors.</span></span>

<span data-ttu-id="1194d-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1194d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1194d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1194d-106">Syntax</span></span>


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a><span data-ttu-id="1194d-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1194d-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="1194d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1194d-108">Remarks</span></span>

<span data-ttu-id="1194d-109">La récupération est non destructrice.</span><span class="sxs-lookup"><span data-stu-id="1194d-109">The retrieval is non-destructive.</span></span> <span data-ttu-id="1194d-110">Plusieurs instances de la collection d’erreurs peuvent être récupérées en appelant à plusieurs reprises cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1194d-110">Multiple instances of the error collection may be retrieved by repeatedly calling this method.</span></span>

### <a name="c"></a><span data-ttu-id="1194d-111">C++</span><span class="sxs-lookup"><span data-stu-id="1194d-111">C++</span></span>

<span data-ttu-id="1194d-112">Consultez la fonction [**obtenir des \_ Erreurs**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) .</span><span class="sxs-lookup"><span data-stu-id="1194d-112">See [**get\_Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1194d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1194d-113">Requirements</span></span>



| <span data-ttu-id="1194d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1194d-114">Requirement</span></span> | <span data-ttu-id="1194d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1194d-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1194d-116">Version</span><span class="sxs-lookup"><span data-stu-id="1194d-116">Version</span></span><br/> | <span data-ttu-id="1194d-117">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1194d-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="1194d-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1194d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1194d-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="1194d-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="1194d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1194d-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="1194d-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1194d-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
