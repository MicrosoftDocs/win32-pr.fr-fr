---
title: BasicDevice. icons, propriété
description: Obtient un vecteur d’interfaces IDeviceIcon.
ms.assetid: 54933FD0-27A6-48D8-A49A-200AD9214B9A
keywords:
- Propriété Icons Media Streaming API
- Propriété d’icônes API de diffusion multimédia en continu, interface BasicDevice
- API de diffusion multimédia en continu de l’interface BasicDevice, propriété Icons
topic_type:
- apiref
api_name:
- BasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdd0235a2b07ea86cbace87defb92f44d6b42315
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381927"
---
# <a name="basicdeviceicons-property"></a><span data-ttu-id="cc7b3-106">BasicDevice. icons, propriété</span><span class="sxs-lookup"><span data-stu-id="cc7b3-106">BasicDevice.Icons property</span></span>

<span data-ttu-id="cc7b3-107">Obtient un vecteur d’interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="cc7b3-107">Gets a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span>

<span data-ttu-id="cc7b3-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cc7b3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc7b3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc7b3-109">Syntax</span></span>


```C++
HRESULT get_Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="property-value"></a><span data-ttu-id="cc7b3-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cc7b3-110">Property value</span></span>

<span data-ttu-id="cc7b3-111">Collection énumérable de pointeurs d’interface [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="cc7b3-111">An enumerable collection of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interface pointers.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc7b3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc7b3-112">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc7b3-113">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc7b3-113">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

 