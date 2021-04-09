---
description: Supprime un objet InkDivider et libère les ressources associées.
ms.assetid: adf772e0-2829-4410-83c4-45a24bf3a848
title: DeleteInkDivider fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteInkDivider
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 8338d179b0bd57232463c794feca96885ee006fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867734"
---
# <a name="deleteinkdivider-function"></a><span data-ttu-id="2e7fe-103">DeleteInkDivider fonction)</span><span class="sxs-lookup"><span data-stu-id="2e7fe-103">DeleteInkDivider function</span></span>

<span data-ttu-id="2e7fe-104">Supprime un objet [**InkDivider**](inkdivider-class.md) et libère les ressources associées.</span><span class="sxs-lookup"><span data-stu-id="2e7fe-104">Deletes an [**InkDivider**](inkdivider-class.md) object and releases associated resources.</span></span>

<span data-ttu-id="2e7fe-105">Cette fonction n’est pas destinée à être utilisée par le code d’application.</span><span class="sxs-lookup"><span data-stu-id="2e7fe-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7fe-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e7fe-106">Syntax</span></span>


```C++
HRESULT WINAPI DeleteInkDivider(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="2e7fe-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e7fe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e7fe-108">*hDivider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e7fe-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e7fe-109">Handle de l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="2e7fe-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e7fe-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e7fe-110">Return value</span></span>

<span data-ttu-id="2e7fe-111">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2e7fe-111">This function can return one of these values.</span></span>



| <span data-ttu-id="2e7fe-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2e7fe-112">Return code</span></span>                                                                                  | <span data-ttu-id="2e7fe-113">Description</span><span class="sxs-lookup"><span data-stu-id="2e7fe-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="2e7fe-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2e7fe-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2e7fe-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="2e7fe-115">The method succeeded.</span></span><br/>                |
| <dl> <span data-ttu-id="2e7fe-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2e7fe-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2e7fe-117">Le paramètre *hDivider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2e7fe-117">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2e7fe-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e7fe-118">Requirements</span></span>



| <span data-ttu-id="2e7fe-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e7fe-119">Requirement</span></span> | <span data-ttu-id="2e7fe-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e7fe-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e7fe-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e7fe-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e7fe-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e7fe-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="2e7fe-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e7fe-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e7fe-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e7fe-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="2e7fe-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2e7fe-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e7fe-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e7fe-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




