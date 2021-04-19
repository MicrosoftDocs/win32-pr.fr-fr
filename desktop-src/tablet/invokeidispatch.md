---
description: Appelle la fonctionnalité d’assistance pour l’interface IDispatch.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: InvokeIDispatch fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4989e3ec23a1ffa97ba317831143ecf0920ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517921"
---
# <a name="invokeidispatch-function"></a><span data-ttu-id="480e7-103">InvokeIDispatch fonction)</span><span class="sxs-lookup"><span data-stu-id="480e7-103">InvokeIDispatch function</span></span>

<span data-ttu-id="480e7-104">Appelle la fonctionnalité d’assistance pour l’interface IDispatch.</span><span class="sxs-lookup"><span data-stu-id="480e7-104">Invokes helper functionality for the IDispatch interface.</span></span>

<span data-ttu-id="480e7-105">Cette fonction n’est pas destinée à être utilisée par le code d’application.</span><span class="sxs-lookup"><span data-stu-id="480e7-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="480e7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="480e7-106">Syntax</span></span>


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a><span data-ttu-id="480e7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="480e7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="480e7-108">*pDispatch*</span><span class="sxs-lookup"><span data-stu-id="480e7-108">*pDispatch*</span></span> 
</dt> <dd>

<span data-ttu-id="480e7-109">Instance de l’interface IDispatch.</span><span class="sxs-lookup"><span data-stu-id="480e7-109">The instance of the IDispatch interface.</span></span>

</dd> <dt>

<span data-ttu-id="480e7-110">*égal*</span><span class="sxs-lookup"><span data-stu-id="480e7-110">*dispid*</span></span> 
</dt> <dd>

<span data-ttu-id="480e7-111">Méthode, propriété ou argument à passer.</span><span class="sxs-lookup"><span data-stu-id="480e7-111">The method, property, or argument to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="480e7-112">*pDisp*</span><span class="sxs-lookup"><span data-stu-id="480e7-112">*pDisp*</span></span> 
</dt> <dd>

<span data-ttu-id="480e7-113">Paramètres à passer.</span><span class="sxs-lookup"><span data-stu-id="480e7-113">The parameters to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="480e7-114">*pVarResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="480e7-114">*pVarResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="480e7-115">Structure qui reçoit les valeurs récupérées.</span><span class="sxs-lookup"><span data-stu-id="480e7-115">A structure that receives the retrieved values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="480e7-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="480e7-116">Return value</span></span>

<span data-ttu-id="480e7-117">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="480e7-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="480e7-118">En cas d’échec, les codes de retour possibles incluent, sans s’y limiter, les valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="480e7-118">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="480e7-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="480e7-119">Return code</span></span>                                                                                  | <span data-ttu-id="480e7-120">Description</span><span class="sxs-lookup"><span data-stu-id="480e7-120">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="480e7-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="480e7-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="480e7-122">La valeur de *pDispatch* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="480e7-122">The value for *pDispatch* is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="480e7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="480e7-123">Requirements</span></span>



| <span data-ttu-id="480e7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="480e7-124">Requirement</span></span> | <span data-ttu-id="480e7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="480e7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="480e7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="480e7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="480e7-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="480e7-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="480e7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="480e7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="480e7-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="480e7-129">None supported</span></span><br/>                                                             |
| <span data-ttu-id="480e7-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="480e7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="480e7-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="480e7-131"><dt>InkObj.dll</dt></span></span> </dl> |



 

 




