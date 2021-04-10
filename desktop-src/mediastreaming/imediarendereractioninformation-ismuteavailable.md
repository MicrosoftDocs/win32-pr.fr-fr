---
title: Méthode IMediaRendererActionInformation IsMuteAvailable
description: Récupère une valeur qui indique si DMR est capable de désactiver l’audio.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- API de diffusion multimédia en continu de méthode IsMuteAvailable
- API de diffusion multimédia en continu de méthode IsMuteAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsMuteAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96751a7f2f1aedcd9e29be981ffadf6c43bf4008
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031127"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a><span data-ttu-id="8e209-106">IMediaRendererActionInformation :: IsMuteAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="8e209-106">IMediaRendererActionInformation::IsMuteAvailable method</span></span>

<span data-ttu-id="8e209-107">Récupère une valeur qui indique si DMR est capable de désactiver l’audio.</span><span class="sxs-lookup"><span data-stu-id="8e209-107">Retrieves a value that indicates whether the DMR is capable of muting the audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e209-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e209-108">Syntax</span></span>


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="8e209-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e209-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e209-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8e209-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e209-111">Valeur booléenne qui est **true** si la fonction DMR peut désactiver l’audio et **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="8e209-111">A boolean value that is **True** if the DMR is capable of muting the audio and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e209-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e209-112">Return value</span></span>

<span data-ttu-id="8e209-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8e209-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8e209-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8e209-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8e209-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8e209-115">Return code</span></span>                                                                          | <span data-ttu-id="8e209-116">Description</span><span class="sxs-lookup"><span data-stu-id="8e209-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8e209-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8e209-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8e209-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e209-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8e209-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e209-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e209-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="8e209-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

