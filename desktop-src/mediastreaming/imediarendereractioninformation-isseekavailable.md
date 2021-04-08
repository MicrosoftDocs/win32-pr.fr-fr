---
title: Méthode IMediaRendererActionInformation IsSeekAvailable
description: Récupère une valeur qui indique si DMR accepte actuellement la méthode SeekAsync.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- API de diffusion multimédia en continu de méthode IsSeekAvailable
- API de diffusion multimédia en continu de méthode IsSeekAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsSeekAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 700afb72efbab01bbd3a8f5e15fa444eb6b06272
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842237"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a><span data-ttu-id="f5483-106">IMediaRendererActionInformation :: IsSeekAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="f5483-106">IMediaRendererActionInformation::IsSeekAvailable method</span></span>

<span data-ttu-id="f5483-107">Récupère une valeur qui indique si DMR accepte actuellement la méthode [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) .</span><span class="sxs-lookup"><span data-stu-id="f5483-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5483-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5483-108">Syntax</span></span>


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="f5483-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5483-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5483-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f5483-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5483-111">Valeur booléenne qui est **true** si DMR accepte actuellement la méthode [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) et **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="f5483-111">A boolean value that is **True** if the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5483-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5483-112">Return value</span></span>

<span data-ttu-id="f5483-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f5483-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f5483-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f5483-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f5483-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f5483-115">Return code</span></span>                                                                          | <span data-ttu-id="f5483-116">Description</span><span class="sxs-lookup"><span data-stu-id="f5483-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f5483-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5483-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f5483-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5483-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f5483-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5483-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5483-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="f5483-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

