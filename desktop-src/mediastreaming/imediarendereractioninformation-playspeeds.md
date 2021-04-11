---
title: Méthode IMediaRendererActionInformation PlaySpeeds
description: Récupère la liste complète des valeurs PlaySpeed acceptées par le DMR.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- API de diffusion multimédia en continu de méthode PlaySpeeds
- API de diffusion multimédia en continu de méthode PlaySpeeds, interface IMediaRendererActionInformation
- API de diffusion multimédia en continu de l’interface IMediaRendererActionInformation, méthode PlaySpeeds
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31089dd7616c035ebde4079c51988b94d1c27562
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314987"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a><span data-ttu-id="024eb-106">IMediaRendererActionInformation ::P méthode laySpeeds</span><span class="sxs-lookup"><span data-stu-id="024eb-106">IMediaRendererActionInformation::PlaySpeeds method</span></span>

<span data-ttu-id="024eb-107">Récupère la liste complète des valeurs [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) acceptées par le DMR.</span><span class="sxs-lookup"><span data-stu-id="024eb-107">Retrieves the complete list of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) values that are accepted by the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="024eb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="024eb-108">Syntax</span></span>


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a><span data-ttu-id="024eb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="024eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="024eb-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="024eb-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="024eb-111">Reçoit un vecteur de structures [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) spécifiant la liste complète des valeurs **PlaySpeed** qui sont acceptées par le DMR.</span><span class="sxs-lookup"><span data-stu-id="024eb-111">Receives a vector of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) structures specifying the complete list of **PlaySpeed** values that are accepted by the DMR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="024eb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="024eb-112">Return value</span></span>

<span data-ttu-id="024eb-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="024eb-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="024eb-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="024eb-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="024eb-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="024eb-115">Return code</span></span>                                                                          | <span data-ttu-id="024eb-116">Description</span><span class="sxs-lookup"><span data-stu-id="024eb-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="024eb-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="024eb-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="024eb-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="024eb-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="024eb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="024eb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024eb-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="024eb-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

