---
title: IBasicDevice, méthode d’icônes
description: Retourne un vecteur d’interfaces IDeviceIcon.
ms.assetid: 0C083AF3-FE22-4A8E-87B7-0FFA7B65ADBD
keywords:
- Méthode d’icônes API de diffusion multimédia en continu
- Icon Method Media Streaming API, IBasicDevice interface
- API de diffusion multimédia en continu de l’interface IBasicDevice, méthode Icons
topic_type:
- apiref
api_name:
- IBasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fb6e4b708b4e38ffb39f152308cec7b885a772f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724988"
---
# <a name="ibasicdeviceicons-method"></a><span data-ttu-id="20543-106">IBasicDevice :: icons, méthode</span><span class="sxs-lookup"><span data-stu-id="20543-106">IBasicDevice::Icons method</span></span>

<span data-ttu-id="20543-107">Retourne un vecteur d’interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="20543-107">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="20543-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20543-108">Syntax</span></span>


```C++
HRESULT Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="parameters"></a><span data-ttu-id="20543-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20543-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20543-110">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="20543-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20543-111">Reçoit une collection énumérable de pointeurs d’interface [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="20543-111">Receives an enumerable collection of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20543-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20543-112">Return value</span></span>

<span data-ttu-id="20543-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="20543-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="20543-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="20543-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="20543-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="20543-115">Return code</span></span>                                                                          | <span data-ttu-id="20543-116">Description</span><span class="sxs-lookup"><span data-stu-id="20543-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="20543-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="20543-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="20543-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="20543-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="20543-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20543-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20543-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="20543-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

