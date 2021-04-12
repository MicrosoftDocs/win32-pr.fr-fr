---
title: Méthode ITransportParameters ActionInformation
description: Obtient une interface IMediaRendererActionInformation qui fournit des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- API de diffusion multimédia en continu de méthode ActionInformation
- API de diffusion multimédia en continu de méthode ActionInformation, interface ITransportParameters
- API de diffusion multimédia en continu de l’interface ITransportParameters, méthode ActionInformation
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b194da50e71402b6af69eb4cc9d67902e8ae89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031140"
---
# <a name="itransportparametersactioninformation-method"></a><span data-ttu-id="f07aa-106">ITransportParameters :: ActionInformation, méthode</span><span class="sxs-lookup"><span data-stu-id="f07aa-106">ITransportParameters::ActionInformation method</span></span>

<span data-ttu-id="f07aa-107">Obtient une interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) qui fournit des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.</span><span class="sxs-lookup"><span data-stu-id="f07aa-107">Obtains an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface that provides information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="f07aa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f07aa-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="f07aa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f07aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f07aa-110">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f07aa-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f07aa-111">Reçoit une référence à une interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .</span><span class="sxs-lookup"><span data-stu-id="f07aa-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f07aa-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f07aa-112">Return value</span></span>

<span data-ttu-id="f07aa-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f07aa-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f07aa-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f07aa-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f07aa-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f07aa-115">Return code</span></span>                                                                          | <span data-ttu-id="f07aa-116">Description</span><span class="sxs-lookup"><span data-stu-id="f07aa-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f07aa-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f07aa-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f07aa-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f07aa-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f07aa-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f07aa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f07aa-120">**ITransportParameters**</span><span class="sxs-lookup"><span data-stu-id="f07aa-120">**ITransportParameters**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

