---
description: La propriété ModuleTable en lecture seule retourne le nom de la table dans le module à l’origine de l’erreur.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Erreur. ModuleTable, propriété (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 063898419596fc852d073bf83ce7504a7691a10e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544424"
---
# <a name="errormoduletable-property"></a><span data-ttu-id="4e904-103">Error. ModuleTable, propriété</span><span class="sxs-lookup"><span data-stu-id="4e904-103">Error.ModuleTable property</span></span>

<span data-ttu-id="4e904-104">La propriété **ModuleTable** en lecture seule retourne le nom de la table dans le module à l’origine de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4e904-104">The read-only **ModuleTable** Property returns the name of the table in the module that caused the error.</span></span>

<span data-ttu-id="4e904-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4e904-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e904-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e904-106">Syntax</span></span>


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a><span data-ttu-id="4e904-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4e904-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="4e904-108">Notes</span><span class="sxs-lookup"><span data-stu-id="4e904-108">Remarks</span></span>

<span data-ttu-id="4e904-109">La collection est vide si les valeurs ne s’appliquent pas au type de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4e904-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="4e904-110">Vous pouvez déterminer le type d’erreur en appelant la propriété [**type**](error-type.md) de l’objet [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="4e904-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="4e904-111">C++</span><span class="sxs-lookup"><span data-stu-id="4e904-111">C++</span></span>

<span data-ttu-id="4e904-112">Consultez la fonction [**obtenir \_ ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) .</span><span class="sxs-lookup"><span data-stu-id="4e904-112">See [**get\_ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e904-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e904-113">Requirements</span></span>



| <span data-ttu-id="4e904-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e904-114">Requirement</span></span> | <span data-ttu-id="4e904-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e904-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e904-116">Version</span><span class="sxs-lookup"><span data-stu-id="4e904-116">Version</span></span><br/> | <span data-ttu-id="4e904-117">Mergemod.dll 1,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4e904-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="4e904-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e904-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4e904-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e904-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e904-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4e904-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="4e904-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e904-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

