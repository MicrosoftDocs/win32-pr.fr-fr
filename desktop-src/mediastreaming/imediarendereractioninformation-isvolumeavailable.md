---
title: Méthode IMediaRendererActionInformation IsVolumeAvailable
description: Récupère une valeur qui indique si DMR est capable d’ajuster le niveau de volume audio.
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- API de diffusion multimédia en continu de méthode IsVolumeAvailable
- API de diffusion multimédia en continu de méthode IsVolumeAvailable, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode IsVolumeAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb8dc60c25cf3ec12e0ebeaa863e239c287d7c46
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101509"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a><span data-ttu-id="ed414-106">IMediaRendererActionInformation :: IsVolumeAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="ed414-106">IMediaRendererActionInformation::IsVolumeAvailable method</span></span>

<span data-ttu-id="ed414-107">Récupère une valeur qui indique si DMR est capable d’ajuster le niveau de volume audio.</span><span class="sxs-lookup"><span data-stu-id="ed414-107">Retrieves a value that indicates whether the DMR is capable of adjusting the audio volume level.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed414-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed414-108">Syntax</span></span>


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="ed414-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed414-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed414-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ed414-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed414-111">Valeur booléenne qui est **true** si la fonction DMR est capable d’ajuster le niveau de volume audio et **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="ed414-111">A boolean value that is **True** if the DMR is capable of adjusting the audio volume level and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed414-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed414-112">Return value</span></span>

<span data-ttu-id="ed414-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ed414-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ed414-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ed414-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ed414-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ed414-115">Return code</span></span>                                                                          | <span data-ttu-id="ed414-116">Description</span><span class="sxs-lookup"><span data-stu-id="ed414-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ed414-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ed414-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ed414-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed414-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ed414-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed414-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed414-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="ed414-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

