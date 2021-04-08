---
description: Teste si l’objet InkDivider peut utiliser la classe InkRecognizerContext pour analyser des mots.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: RecognizerContextSet fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 51e75b810c2103afed2e8ac8a28706b9c9af5da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865813"
---
# <a name="recognizercontextset-function"></a><span data-ttu-id="41a4f-103">RecognizerContextSet fonction)</span><span class="sxs-lookup"><span data-stu-id="41a4f-103">RecognizerContextSet function</span></span>

<span data-ttu-id="41a4f-104">Teste si l’objet [**InkDivider**](inkdivider-class.md) peut utiliser la classe [**InkRecognizerContext**](inkrecognizercontext-class.md) pour analyser des mots.</span><span class="sxs-lookup"><span data-stu-id="41a4f-104">Tests whether the [**InkDivider**](inkdivider-class.md) object can use the [**InkRecognizerContext**](inkrecognizercontext-class.md) class to analyze words.</span></span>

<span data-ttu-id="41a4f-105">Cette fonction n’est pas destinée à être utilisée par le code d’application.</span><span class="sxs-lookup"><span data-stu-id="41a4f-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="41a4f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41a4f-106">Syntax</span></span>


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="41a4f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41a4f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41a4f-108">*hDivider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41a4f-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41a4f-109">Handle de l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="41a4f-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41a4f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41a4f-110">Return value</span></span>

<span data-ttu-id="41a4f-111">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="41a4f-111">This function can return one of these values.</span></span>



| <span data-ttu-id="41a4f-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="41a4f-112">Return code</span></span>                                                                                  | <span data-ttu-id="41a4f-113">Description</span><span class="sxs-lookup"><span data-stu-id="41a4f-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="41a4f-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="41a4f-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="41a4f-115">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="41a4f-115">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="41a4f-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="41a4f-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="41a4f-117">Le paramètre *pDivider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="41a4f-117">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="41a4f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41a4f-118">Requirements</span></span>



| <span data-ttu-id="41a4f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41a4f-119">Requirement</span></span> | <span data-ttu-id="41a4f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="41a4f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41a4f-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41a4f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="41a4f-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41a4f-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="41a4f-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41a4f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="41a4f-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="41a4f-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="41a4f-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41a4f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="41a4f-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41a4f-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




