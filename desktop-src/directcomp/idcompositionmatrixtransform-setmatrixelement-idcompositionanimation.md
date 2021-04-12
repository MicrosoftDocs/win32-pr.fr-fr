---
title: IDCompositionMatrixTransform SetMatrixElement (int, int, IDCompositionAnimation), méthode
description: Anime la valeur d’un élément de la matrice de cette transformation 2D.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Méthode SetMatrixElement DirectComposition
- SetMatrixElement, méthode DirectComposition, IDCompositionMatrixTransform, interface
- IDCompositionMatrixTransform interface DirectComposition, méthode SetMatrixElement
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382389"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a><span data-ttu-id="20415-106">IDCompositionMatrixTransform :: SetMatrixElement (int, int, IDCompositionAnimation \* ), méthode</span><span class="sxs-lookup"><span data-stu-id="20415-106">IDCompositionMatrixTransform::SetMatrixElement(int, int, IDCompositionAnimation\*) method</span></span>

<span data-ttu-id="20415-107">Anime la valeur d’un élément de la matrice de cette transformation 2D.</span><span class="sxs-lookup"><span data-stu-id="20415-107">Animates the value of one element of the matrix of this 2D transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="20415-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20415-108">Syntax</span></span>


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a><span data-ttu-id="20415-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20415-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20415-110">*ligne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20415-110">*row* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20415-111">Index de ligne de l’élément à modifier.</span><span class="sxs-lookup"><span data-stu-id="20415-111">The row index of the element to change.</span></span> <span data-ttu-id="20415-112">Cette valeur doit être comprise entre 0 et 2 inclus.</span><span class="sxs-lookup"><span data-stu-id="20415-112">This value must be between 0 and 2, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="20415-113">*colonne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20415-113">*column* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20415-114">Index de colonne de l’élément à modifier.</span><span class="sxs-lookup"><span data-stu-id="20415-114">The column index of the element to change.</span></span> <span data-ttu-id="20415-115">Cette valeur doit être comprise entre 0 et 1, inclus.</span><span class="sxs-lookup"><span data-stu-id="20415-115">This value must be between 0 and 1, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="20415-116">*animation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20415-116">*animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20415-117">Animation qui représente la façon dont la valeur de l’élément spécifié change au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="20415-117">An animation that represents how the value of the specified element changes over time.</span></span> <span data-ttu-id="20415-118">Ce paramètre ne doit pas avoir la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="20415-118">This parameter must not be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20415-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20415-119">Return value</span></span>

<span data-ttu-id="20415-120">Si la fonction est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20415-120">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="20415-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="20415-121">Otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="20415-122">Pour obtenir la liste des codes d’erreur, consultez [codes d’erreur DirectComposition](directcomposition-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="20415-122">See [DirectComposition Error Codes](directcomposition-error-codes.md) for a list of error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="20415-123">Notes</span><span class="sxs-lookup"><span data-stu-id="20415-123">Remarks</span></span>

<span data-ttu-id="20415-124">Cette méthode effectue une copie de l’animation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="20415-124">This method makes a copy of the specified animation.</span></span> <span data-ttu-id="20415-125">Si l’objet référencé par le paramètre d' *animation* est modifié après l’appel de cette méthode, la modification n’affecte pas l’élément à moins que cette méthode ne soit appelée à nouveau.</span><span class="sxs-lookup"><span data-stu-id="20415-125">If the object referenced by the *animation* parameter is changed after calling this method, the change does not affect the element unless this method is called again.</span></span> <span data-ttu-id="20415-126">Si l’élément a été précédemment animé, l’appel de cette méthode remplace l’animation précédente par la nouvelle animation.</span><span class="sxs-lookup"><span data-stu-id="20415-126">If the element was previously animated, calling this method replaces the previous animation with the new animation.</span></span>

<span data-ttu-id="20415-127">Cette méthode échoue si l' *animation* est un pointeur non valide ou si elle n’a pas été créée par la même interface [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) que la transformation affectée.</span><span class="sxs-lookup"><span data-stu-id="20415-127">This method fails if *animation* is an invalid pointer or if it was not created by the same [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) interface as the affected transform.</span></span> <span data-ttu-id="20415-128">L’interface ne peut pas être une implémentation personnalisée ; seules les interfaces créées par Microsoft DirectComposition peuvent être utilisées avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="20415-128">The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="20415-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20415-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20415-130">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="20415-130">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 