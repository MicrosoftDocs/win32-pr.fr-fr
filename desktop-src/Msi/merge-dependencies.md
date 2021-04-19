---
description: La propriété dépendances en lecture seule de l’objet Merge retourne une collection d’objets de dépendance qui énumère un ensemble de dépendances non satisfaites pour la base de données actuelle.
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: Merge. Dependencies, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542351"
---
# <a name="mergedependencies-property"></a><span data-ttu-id="78324-103">Merge. Dependencies, propriété</span><span class="sxs-lookup"><span data-stu-id="78324-103">Merge.Dependencies property</span></span>

<span data-ttu-id="78324-104">La propriété **dépendances** en lecture seule de l’objet [**Merge**](merge-object.md) retourne une collection d’objets de [**dépendance**](dependency-object.md) qui énumère un ensemble de dépendances non satisfaites pour la base de données actuelle.</span><span class="sxs-lookup"><span data-stu-id="78324-104">The read-only **Dependencies** property of the [**Merge**](merge-object.md) object returns a collection of [**Dependency**](dependency-object.md) objects that enumerates a set of unsatisfied dependencies for the current database.</span></span>

<span data-ttu-id="78324-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="78324-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="78324-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78324-106">Syntax</span></span>


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a><span data-ttu-id="78324-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="78324-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="78324-108">Notes</span><span class="sxs-lookup"><span data-stu-id="78324-108">Remarks</span></span>

<span data-ttu-id="78324-109">Un module n’a pas besoin d’être ouvert pour récupérer les informations de dépendance.</span><span class="sxs-lookup"><span data-stu-id="78324-109">A module does not need to be open to retrieve dependency information.</span></span>

### <a name="c"></a><span data-ttu-id="78324-110">C++</span><span class="sxs-lookup"><span data-stu-id="78324-110">C++</span></span>

<span data-ttu-id="78324-111">Consultez la fonction [**obtenir des \_ dépendances**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) .</span><span class="sxs-lookup"><span data-stu-id="78324-111">See [**get\_Dependencies**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="78324-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78324-112">Requirements</span></span>



| <span data-ttu-id="78324-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78324-113">Requirement</span></span> | <span data-ttu-id="78324-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="78324-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78324-115">Version</span><span class="sxs-lookup"><span data-stu-id="78324-115">Version</span></span><br/> | <span data-ttu-id="78324-116">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="78324-116">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="78324-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="78324-117">Header</span></span><br/>  | <dl> <span data-ttu-id="78324-118"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="78324-118"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="78324-119">DLL</span><span class="sxs-lookup"><span data-stu-id="78324-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="78324-120"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78324-120"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
