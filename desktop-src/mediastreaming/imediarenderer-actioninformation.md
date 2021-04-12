---
title: Méthode IMediaRenderer ActionInformation
description: Récupère des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- API de diffusion multimédia en continu de méthode ActionInformation
- API de diffusion multimédia en continu de méthode ActionInformation, interface IMediaRenderer
- API de diffusion multimédia en continu de l’interface IMediaRenderer, méthode ActionInformation
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 346e43d6aaf3503c21f6a7586db5a731f0a7c478
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031155"
---
# <a name="imediarendereractioninformation-method"></a><span data-ttu-id="e7fc7-106">IMediaRenderer :: ActionInformation, méthode</span><span class="sxs-lookup"><span data-stu-id="e7fc7-106">IMediaRenderer::ActionInformation method</span></span>

<span data-ttu-id="e7fc7-107">Récupère des informations sur les méthodes qui peuvent être appelées actuellement sur la DMR.</span><span class="sxs-lookup"><span data-stu-id="e7fc7-107">Retrieves information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7fc7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7fc7-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="e7fc7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7fc7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7fc7-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e7fc7-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7fc7-111">Reçoit une référence à une interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .</span><span class="sxs-lookup"><span data-stu-id="e7fc7-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7fc7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7fc7-112">Return value</span></span>

<span data-ttu-id="e7fc7-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e7fc7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e7fc7-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e7fc7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e7fc7-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e7fc7-115">Return code</span></span>                                                                          | <span data-ttu-id="e7fc7-116">Description</span><span class="sxs-lookup"><span data-stu-id="e7fc7-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e7fc7-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e7fc7-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e7fc7-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7fc7-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e7fc7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7fc7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7fc7-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="e7fc7-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

