---
title: GetPositionInformationOperation. GetResults, méthode
description: Retourne les résultats de l’opération asynchrone démarrée par GetPositionInformationAsync.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- Méthode GetResults API de diffusion multimédia en continu
- Méthode GetResults API de diffusion multimédia en continu, interface GetPositionInformationOperation
- API de diffusion multimédia en continu de l’interface GetPositionInformationOperation, méthode GetResults
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a0b4311c3be814a73ddb1e2a9b18d8e19aea9ee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726757"
---
# <a name="getpositioninformationoperationgetresults-method"></a><span data-ttu-id="523c3-106">GetPositionInformationOperation. GetResults, méthode</span><span class="sxs-lookup"><span data-stu-id="523c3-106">GetPositionInformationOperation.GetResults method</span></span>

<span data-ttu-id="523c3-107">Retourne les résultats de l’opération asynchrone démarrée par [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span><span class="sxs-lookup"><span data-stu-id="523c3-107">Returns the results of the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="523c3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="523c3-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="523c3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="523c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="523c3-110">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="523c3-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="523c3-111">Référence à une structure [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) qui contient les résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="523c3-111">A reference to a [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="523c3-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="523c3-112">Return value</span></span>

<span data-ttu-id="523c3-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="523c3-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="523c3-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="523c3-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="523c3-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="523c3-115">Return code</span></span>                                                                          | <span data-ttu-id="523c3-116">Description</span><span class="sxs-lookup"><span data-stu-id="523c3-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="523c3-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="523c3-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="523c3-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="523c3-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="523c3-119">Notes</span><span class="sxs-lookup"><span data-stu-id="523c3-119">Remarks</span></span>

<span data-ttu-id="523c3-120">La méthode **GetResults** est généralement appelée à partir du gestionnaire d’événements qui a été enregistré en définissant la propriété [**Completed**](getpositioninformationoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="523c3-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getpositioninformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="523c3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="523c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523c3-122">**GetPositionInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="523c3-122">**GetPositionInformationOperation**</span></span>](getpositioninformationoperation.md)
</dt> </dl>

 

