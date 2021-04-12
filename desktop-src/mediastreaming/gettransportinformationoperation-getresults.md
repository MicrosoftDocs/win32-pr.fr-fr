---
title: GetTransportInformationOperation GetResults, méthode
description: Retourne les résultats de l’opération asynchrone démarrée par GetTransportInformationAsync.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- Méthode GetResults API de diffusion multimédia en continu
- Méthode GetResults API de diffusion multimédia en continu, interface GetTransportInformationOperation
- API de diffusion multimédia en continu de l’interface GetTransportInformationOperation, méthode GetResults
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f846a5824ed07bcaf849a540429eaabe46f3d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381899"
---
# <a name="gettransportinformationoperationgetresults-method"></a><span data-ttu-id="a3045-106">GetTransportInformationOperation :: GetResults, méthode</span><span class="sxs-lookup"><span data-stu-id="a3045-106">GetTransportInformationOperation::GetResults method</span></span>

<span data-ttu-id="a3045-107">Retourne les résultats de l’opération asynchrone démarrée par [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span><span class="sxs-lookup"><span data-stu-id="a3045-107">Returns the results of the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3045-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3045-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="a3045-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3045-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3045-110">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a3045-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a3045-111">Référence à une structure [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) qui contient les résultats de l’opération.</span><span class="sxs-lookup"><span data-stu-id="a3045-111">A reference to a [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3045-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a3045-112">Return value</span></span>

<span data-ttu-id="a3045-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a3045-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a3045-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a3045-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a3045-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a3045-115">Return code</span></span>                                                                          | <span data-ttu-id="a3045-116">Description</span><span class="sxs-lookup"><span data-stu-id="a3045-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a3045-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a3045-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a3045-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3045-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3045-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a3045-119">Remarks</span></span>

<span data-ttu-id="a3045-120">La méthode **GetResults** est généralement appelée à partir du gestionnaire d’événements qui a été enregistré en définissant la propriété [**Completed**](gettransportinformationoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="a3045-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](gettransportinformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3045-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3045-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3045-122">**GetTransportInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="a3045-122">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

