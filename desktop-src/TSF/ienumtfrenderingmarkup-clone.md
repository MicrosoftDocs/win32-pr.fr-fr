---
title: IEnumTfRenderingMarkup Clone (méthode)
description: La méthode Clone IEnumTfRenderingMarkup crée une copie de l’objet énumérateur.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Cloner la méthode Text Services Framework
- Cloner la méthode Text Services Framework, interface IEnumTfRenderingMarkup
- IEnumTfRenderingMarkup interface Text Services Framework, Clone, méthode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512110"
---
# <a name="ienumtfrenderingmarkupclone-method"></a><span data-ttu-id="67c33-106">IEnumTfRenderingMarkup :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="67c33-106">IEnumTfRenderingMarkup::Clone method</span></span>

<span data-ttu-id="67c33-107">La méthode **IEnumTfRenderingMarkup :: Clone** crée une copie de l’objet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="67c33-107">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>

## <a name="syntax"></a><span data-ttu-id="67c33-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67c33-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="67c33-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67c33-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67c33-110">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="67c33-110">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67c33-111">\[\]pointeur vers une interface [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="67c33-111">\[out\] A pointer to a [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67c33-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67c33-112">Return value</span></span>

<span data-ttu-id="67c33-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="67c33-113">This method can return one of these values.</span></span>



| <span data-ttu-id="67c33-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="67c33-114">Value</span></span>                                                                                        | <span data-ttu-id="67c33-115">Description</span><span class="sxs-lookup"><span data-stu-id="67c33-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="67c33-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="67c33-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="67c33-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="67c33-117">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="67c33-118"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="67c33-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="67c33-119">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="67c33-119">An unspecified error occurred.</span></span><br/>      |
| <dl> <span data-ttu-id="67c33-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="67c33-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="67c33-121">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="67c33-121">One or more parameters are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67c33-122">Notes</span><span class="sxs-lookup"><span data-stu-id="67c33-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="67c33-123">Cette méthode n’est pas actuellement dans les fichiers d’en-tête publics.</span><span class="sxs-lookup"><span data-stu-id="67c33-123">This method is not currently in the public header files.</span></span> <span data-ttu-id="67c33-124">Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="67c33-124">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

