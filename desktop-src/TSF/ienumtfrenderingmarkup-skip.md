---
title: IEnumTfRenderingMarkup Skip (méthode)
description: La méthode IEnumTfRenderingMarkup Skip obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Ignorer la méthode Text Services Framework
- Ignorer la méthode Text Services Framework, interface IEnumTfRenderingMarkup
- IEnumTfRenderingMarkup interface Text Services Framework, Skip, méthode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678314"
---
# <a name="ienumtfrenderingmarkupskip-method"></a><span data-ttu-id="4e0ed-106">IEnumTfRenderingMarkup :: Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="4e0ed-106">IEnumTfRenderingMarkup::Skip method</span></span>

<span data-ttu-id="4e0ed-107">La méthode **IEnumTfRenderingMarkup :: Skip** obtient, à partir de la position actuelle, le nombre spécifié d’éléments dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="4e0ed-107">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e0ed-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e0ed-108">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a><span data-ttu-id="4e0ed-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e0ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e0ed-110">*ulCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e0ed-110">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e0ed-111">\[dans \] spécifie le nombre d’éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="4e0ed-111">\[in\] Specifies the number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e0ed-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e0ed-112">Return value</span></span>

<span data-ttu-id="4e0ed-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="4e0ed-113">This method can return one of these values.</span></span>



| <span data-ttu-id="4e0ed-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e0ed-114">Value</span></span>                                                                                   | <span data-ttu-id="4e0ed-115">Description</span><span class="sxs-lookup"><span data-stu-id="4e0ed-115">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4e0ed-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4e0ed-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="4e0ed-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="4e0ed-117">The method was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="4e0ed-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4e0ed-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="4e0ed-119">La méthode a atteint la fin de l’énumération avant que le nombre spécifié d’éléments puisse être ignoré.</span><span class="sxs-lookup"><span data-stu-id="4e0ed-119">The method reached the end of the enumeration before the specified number of elements could be skipped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e0ed-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4e0ed-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4e0ed-121">Cette méthode n’est pas actuellement dans les fichiers d’en-tête publics.</span><span class="sxs-lookup"><span data-stu-id="4e0ed-121">This method is not currently in the public header files.</span></span> <span data-ttu-id="4e0ed-122">Pour utiliser cette API, vous devez effectuer une compilation MIDL du [prototype](prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="4e0ed-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 





