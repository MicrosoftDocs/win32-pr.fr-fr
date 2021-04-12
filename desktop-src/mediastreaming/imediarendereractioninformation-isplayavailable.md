---
title: Méthode IMediaRendererActionInformation IsPlayAvailable
description: Récupère une valeur qui indique si le DMR accepte actuellement les méthodes PlayAsync et PlayAtSpeedAsync.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- API de diffusion multimédia en continu de méthode IsPlayAvailable
- API de diffusion multimédia en continu de méthode IsPlayAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsPlayAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 87fa3a2005772a4d948bafe32d2a0e10cc5a6914
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381897"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a><span data-ttu-id="d6b89-106">IMediaRendererActionInformation :: IsPlayAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="d6b89-106">IMediaRendererActionInformation::IsPlayAvailable method</span></span>

<span data-ttu-id="d6b89-107">Récupère une valeur qui indique si le DMR accepte actuellement les méthodes [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) et [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) .</span><span class="sxs-lookup"><span data-stu-id="d6b89-107">Retrieves a value that indicates whether the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6b89-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6b89-108">Syntax</span></span>


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="d6b89-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6b89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6b89-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6b89-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6b89-111">Valeur booléenne qui est **true** si la dernière accepte les méthodes [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) et [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) , et **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="d6b89-111">A boolean value that is **True** if the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6b89-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6b89-112">Return value</span></span>

<span data-ttu-id="d6b89-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d6b89-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d6b89-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d6b89-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d6b89-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d6b89-115">Return code</span></span>                                                                          | <span data-ttu-id="d6b89-116">Description</span><span class="sxs-lookup"><span data-stu-id="d6b89-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d6b89-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d6b89-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d6b89-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6b89-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d6b89-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6b89-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6b89-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="d6b89-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

