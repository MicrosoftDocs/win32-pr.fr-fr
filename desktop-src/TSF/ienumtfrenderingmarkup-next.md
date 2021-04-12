---
title: IEnumTfRenderingMarkup méthode Next
description: La méthode Next IEnumTfRenderingMarkup obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Infrastructure des services de texte méthode suivante
- Méthode Next Text Services Framework, interface IEnumTfRenderingMarkup
- IEnumTfRenderingMarkup interface Text Services Framework, Next, méthode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031489"
---
# <a name="ienumtfrenderingmarkupnext-method"></a><span data-ttu-id="00753-106">IEnumTfRenderingMarkup :: Next, méthode</span><span class="sxs-lookup"><span data-stu-id="00753-106">IEnumTfRenderingMarkup::Next method</span></span>

<span data-ttu-id="00753-107">La méthode **IEnumTfRenderingMarkup :: Next** obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="00753-107">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="00753-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00753-108">Syntax</span></span>


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="00753-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00753-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00753-110">*ulCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="00753-110">*ulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00753-111">\[out \] spécifie le nombre d’éléments à obtenir.</span><span class="sxs-lookup"><span data-stu-id="00753-111">\[out\] Specifies the number of elements to obtain.</span></span>

</dd> <dt>

<span data-ttu-id="00753-112">*ppElement* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="00753-112">*ppElement* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00753-113">\[pointeur de sortie \] vers un tableau de structures [ \_ RENDERINGMARKUP TF](/windows/desktop/TSF/tf-renderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="00753-113">\[out\] Pointer to an array of [TF\_RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) structures.</span></span> <span data-ttu-id="00753-114">Ce tableau doit avoir au moins *ulCount* éléments de taille.</span><span class="sxs-lookup"><span data-stu-id="00753-114">This array must be at least *ulCount* elements in size.</span></span>

</dd> <dt>

<span data-ttu-id="00753-115">*pcFetched* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="00753-115">*pcFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00753-116">\[\]pointeur vers une valeur ulong qui reçoit le nombre d’éléments réellement obtenus.</span><span class="sxs-lookup"><span data-stu-id="00753-116">\[out\] Pointer to a ULONG value that receives the number of elements actually obtained.</span></span> <span data-ttu-id="00753-117">Cette valeur peut être inférieure au nombre d’éléments demandés.</span><span class="sxs-lookup"><span data-stu-id="00753-117">This value can be less than the number of items requested.</span></span> <span data-ttu-id="00753-118">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="00753-118">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00753-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00753-119">Return value</span></span>

<span data-ttu-id="00753-120">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="00753-120">This method can return one of these values.</span></span>



| <span data-ttu-id="00753-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="00753-121">Value</span></span>                                                                                        | <span data-ttu-id="00753-122">Description</span><span class="sxs-lookup"><span data-stu-id="00753-122">Description</span></span>                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00753-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="00753-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="00753-124">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="00753-124">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="00753-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="00753-125"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="00753-126">La méthode a atteint la fin de l’énumération avant que le nombre spécifié d’éléments puisse être obtenu.</span><span class="sxs-lookup"><span data-stu-id="00753-126">The method reached the end of the enumeration before the specified number of elements could be obtained.</span></span><br/> |
| <dl> <span data-ttu-id="00753-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="00753-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="00753-128">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="00753-128">One or more parameters are invalid.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="00753-129">Notes</span><span class="sxs-lookup"><span data-stu-id="00753-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="00753-130">Cette méthode n’est pas actuellement dans les fichiers d’en-tête publics.</span><span class="sxs-lookup"><span data-stu-id="00753-130">This method is not currently in the public header files.</span></span> <span data-ttu-id="00753-131">Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="00753-131">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

