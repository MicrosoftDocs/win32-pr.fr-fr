---
description: Définit une fonction de rappel à utiliser pendant la reconnaissance de ligne.
ms.assetid: 0b07ec80-328a-471b-b554-fa66f56a2871
title: SetLineRecoCallback fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineRecoCallback
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: b256a38d6d6ee6ecf43994c6619c369ea6ca2212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203424"
---
# <a name="setlinerecocallback-function"></a><span data-ttu-id="b0dd5-103">SetLineRecoCallback fonction)</span><span class="sxs-lookup"><span data-stu-id="b0dd5-103">SetLineRecoCallback function</span></span>

<span data-ttu-id="b0dd5-104">Définit une fonction de rappel à utiliser pendant la reconnaissance de ligne.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-104">Sets a callback function to be used during line recognition.</span></span>

<span data-ttu-id="b0dd5-105">Cette fonction d’assistance n’est pas destinée à être utilisée par le code d’application.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0dd5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0dd5-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineRecoCallback(
  _In_ INT_PTR        hDivider,
       GetLineRecoDef pfn
);
```



## <a name="parameters"></a><span data-ttu-id="b0dd5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0dd5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0dd5-108">*hDivider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0dd5-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0dd5-109">Handle de l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="b0dd5-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="b0dd5-110">*PFN*</span><span class="sxs-lookup"><span data-stu-id="b0dd5-110">*pfn*</span></span> 
</dt> <dd>

<span data-ttu-id="b0dd5-111">Pointeur vers une fonction qui est appelée lorsque la reconnaissance se produit sur le [**InkDivider**](inkdivider-class.md) passé.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-111">A pointer to a function that is called when recognition occurs on the [**InkDivider**](inkdivider-class.md) passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0dd5-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0dd5-112">Return value</span></span>

<span data-ttu-id="b0dd5-113">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-113">This function can return one of these values.</span></span>



| <span data-ttu-id="b0dd5-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b0dd5-114">Return code</span></span>                                                                                  | <span data-ttu-id="b0dd5-115">Description</span><span class="sxs-lookup"><span data-stu-id="b0dd5-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="b0dd5-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b0dd5-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b0dd5-117">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="b0dd5-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b0dd5-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b0dd5-119">Le paramètre *pDivider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0dd5-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b0dd5-120">Remarks</span></span>

<span data-ttu-id="b0dd5-121">Voici la syntaxe de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="b0dd5-121">The following is the syntax for the callback function.</span></span>

``` syntax
public delegate void GetLineRecoDef(
        int cStrokes, 
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.I4, SizeParamIndex = 0)]int [] aStrokeIds, 
        float degrees, 
        Point point, 
        [MarshalAs(UnmanagedType.BStr)] out string lineString, 
        out int cSegment, 
        out int[] strokeIdOrdered, 
        out int[] segmentStrokes,
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.BStr)] out string [] aSegmentString
    );
```

## <a name="requirements"></a><span data-ttu-id="b0dd5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0dd5-122">Requirements</span></span>



| <span data-ttu-id="b0dd5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0dd5-123">Requirement</span></span> | <span data-ttu-id="b0dd5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0dd5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0dd5-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0dd5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b0dd5-126">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0dd5-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b0dd5-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0dd5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b0dd5-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0dd5-128">None supported</span></span><br/>                                                             |
| <span data-ttu-id="b0dd5-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b0dd5-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0dd5-130"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0dd5-130"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




