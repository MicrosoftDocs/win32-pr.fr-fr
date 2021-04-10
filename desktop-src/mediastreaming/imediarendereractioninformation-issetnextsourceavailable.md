---
title: Méthode IMediaRendererActionInformation IsSetNextSourceAvailable
description: Récupère une valeur qui indique si DMR accepte actuellement la méthode SetNextSourceFromUriAsync, la méthode SetNextSourceFromStreamAsync ou la méthode SetNextSourceFromMediaSourceAsync.
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- API de diffusion multimédia en continu de méthode IsSetNextSourceAvailable
- API de diffusion multimédia en continu de méthode IsSetNextSourceAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsSetNextSourceAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 265a9a96d5229e47008c60813fd6c0e3bc567800
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725892"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a><span data-ttu-id="1a18e-106">IMediaRendererActionInformation :: IsSetNextSourceAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="1a18e-106">IMediaRendererActionInformation::IsSetNextSourceAvailable method</span></span>

<span data-ttu-id="1a18e-107">Récupère une valeur qui indique si DMR accepte actuellement la méthode [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , la méthode [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) ou la méthode [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) .</span><span class="sxs-lookup"><span data-stu-id="1a18e-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a18e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a18e-108">Syntax</span></span>


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="1a18e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a18e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a18e-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1a18e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a18e-111">Valeur booléenne qui est **true** si la méthode DMR accepte actuellement la méthode [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , la méthode [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) ou la méthode [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) , et **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="1a18e-111">A boolean value that is **True** if the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a18e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a18e-112">Return value</span></span>

<span data-ttu-id="1a18e-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1a18e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1a18e-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1a18e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1a18e-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1a18e-115">Return code</span></span>                                                                          | <span data-ttu-id="1a18e-116">Description</span><span class="sxs-lookup"><span data-stu-id="1a18e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1a18e-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1a18e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1a18e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a18e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1a18e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a18e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a18e-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="1a18e-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

