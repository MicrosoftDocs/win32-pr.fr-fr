---
description: Définit la propriété LineHeight sur l’objet InkDivider.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: SetLineHeight fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: be4045e01ac890471536d95768668b633d8f2249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520629"
---
# <a name="setlineheight-function"></a><span data-ttu-id="53058-103">SetLineHeight fonction)</span><span class="sxs-lookup"><span data-stu-id="53058-103">SetLineHeight function</span></span>

<span data-ttu-id="53058-104">Définit la propriété [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) sur l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="53058-104">Sets the [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property on the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="53058-105">Cette fonction d’assistance n’est pas destinée à être utilisée par le code d’application.</span><span class="sxs-lookup"><span data-stu-id="53058-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="53058-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53058-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a><span data-ttu-id="53058-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53058-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53058-108">*hDivider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53058-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53058-109">Handle de l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="53058-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="53058-110">*lLineHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53058-110">*lLineHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53058-111">La propriété [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) de l’objet [**InkDivider**](inkdivider-class.md) , en unités HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="53058-111">The [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property of the [**InkDivider**](inkdivider-class.md) object, in HIMETRIC units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53058-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53058-112">Return value</span></span>

<span data-ttu-id="53058-113">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="53058-113">This function can return one of these values.</span></span>



| <span data-ttu-id="53058-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="53058-114">Return code</span></span>                                                                                  | <span data-ttu-id="53058-115">Description</span><span class="sxs-lookup"><span data-stu-id="53058-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="53058-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53058-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="53058-117">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="53058-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="53058-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="53058-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="53058-119">Le paramètre *pDivider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="53058-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="53058-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53058-120">Requirements</span></span>



| <span data-ttu-id="53058-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53058-121">Requirement</span></span> | <span data-ttu-id="53058-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="53058-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53058-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53058-123">Minimum supported client</span></span><br/> | <span data-ttu-id="53058-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53058-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="53058-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53058-125">Minimum supported server</span></span><br/> | <span data-ttu-id="53058-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="53058-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="53058-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="53058-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="53058-128"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53058-128"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 
