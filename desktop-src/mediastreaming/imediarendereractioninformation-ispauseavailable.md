---
title: Méthode IMediaRendererActionInformation IsPauseAvailable
description: Récupère une valeur qui indique si DMR accepte actuellement la méthode PauseAsync.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- API de diffusion multimédia en continu de méthode IsPauseAvailable
- API de diffusion multimédia en continu de méthode IsPauseAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsPauseAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9eb0b750f5a04528aef830d87376c276bdaf6674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842238"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a><span data-ttu-id="cf56c-106">IMediaRendererActionInformation :: IsPauseAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="cf56c-106">IMediaRendererActionInformation::IsPauseAvailable method</span></span>

<span data-ttu-id="cf56c-107">Récupère une valeur qui indique si DMR accepte actuellement la méthode [**PauseAsync**](imediarenderer-pauseasync.md) .</span><span class="sxs-lookup"><span data-stu-id="cf56c-107">Retrieves a value that indicates whether the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf56c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf56c-108">Syntax</span></span>


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="cf56c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf56c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf56c-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cf56c-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf56c-111">Valeur booléenne qui est **true** si DMR accepte actuellement la méthode [**PauseAsync**](imediarenderer-pauseasync.md) et **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="cf56c-111">A boolean value that is **True** if the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf56c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf56c-112">Return value</span></span>

<span data-ttu-id="cf56c-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cf56c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cf56c-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cf56c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cf56c-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cf56c-115">Return code</span></span>                                                                          | <span data-ttu-id="cf56c-116">Description</span><span class="sxs-lookup"><span data-stu-id="cf56c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cf56c-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf56c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cf56c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf56c-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="cf56c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf56c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf56c-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="cf56c-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

