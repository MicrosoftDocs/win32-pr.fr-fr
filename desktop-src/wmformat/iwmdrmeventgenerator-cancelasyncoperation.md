---
title: Méthode IWMDRMEventGenerator CancelAsyncOperation (wmdrmsdk. h)
description: La méthode CancelAsyncOperation annule une opération asynchrone.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Méthode CancelAsyncOperation format Windows Media
- Méthode CancelAsyncOperation format Windows Media, interface IWMDRMEventGenerator
- Interface IWMDRMEventGenerator Windows Media format, méthode CancelAsyncOperation
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539224"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a><span data-ttu-id="b84c1-106">IWMDRMEventGenerator :: CancelAsyncOperation, méthode</span><span class="sxs-lookup"><span data-stu-id="b84c1-106">IWMDRMEventGenerator::CancelAsyncOperation method</span></span>

<span data-ttu-id="b84c1-107">La méthode **CancelAsyncOperation** annule une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b84c1-107">The **CancelAsyncOperation** method cancels an asynchronous operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b84c1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b84c1-108">Syntax</span></span>


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="b84c1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b84c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b84c1-110">*punkCancelationCookie* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b84c1-110">*punkCancelationCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b84c1-111">Pointeur vers le cookie d’annulation qui identifie l’opération asynchrone à annuler.</span><span class="sxs-lookup"><span data-stu-id="b84c1-111">Pointer to the cancellation cookie that identifies the asynchronous operation to be canceled.</span></span> <span data-ttu-id="b84c1-112">Ce cookie est fourni par la méthode utilisée pour démarrer l’opération.</span><span class="sxs-lookup"><span data-stu-id="b84c1-112">This cookie is provided by the method used to start the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b84c1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b84c1-113">Return value</span></span>

<span data-ttu-id="b84c1-114">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b84c1-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b84c1-115">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b84c1-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b84c1-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b84c1-116">Return code</span></span>                                                                          | <span data-ttu-id="b84c1-117">Description</span><span class="sxs-lookup"><span data-stu-id="b84c1-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b84c1-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b84c1-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b84c1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b84c1-119">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b84c1-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b84c1-120">Remarks</span></span>

<span data-ttu-id="b84c1-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b84c1-121">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b84c1-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b84c1-122">Requirements</span></span>



| <span data-ttu-id="b84c1-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b84c1-123">Requirement</span></span> | <span data-ttu-id="b84c1-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b84c1-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b84c1-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b84c1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b84c1-126"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b84c1-126"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="b84c1-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b84c1-127">Library</span></span><br/> | <dl> <span data-ttu-id="b84c1-128"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b84c1-128"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b84c1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b84c1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b84c1-130">**Interface IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="b84c1-130">**IWMDRMEventGenerator Interface**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





