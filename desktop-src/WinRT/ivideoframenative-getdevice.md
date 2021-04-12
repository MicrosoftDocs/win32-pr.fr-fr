---
description: Cette méthode retourne un appareil associé aux données vidéo.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'IVideoFrameNative :: GetDevice, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393516"
---
# <a name="ivideoframenativegetdevice-method"></a><span data-ttu-id="0594e-103">IVideoFrameNative :: GetDevice, méthode</span><span class="sxs-lookup"><span data-stu-id="0594e-103">IVideoFrameNative::GetDevice method</span></span>

<span data-ttu-id="0594e-104">Cette méthode retourne un appareil associé aux données vidéo.</span><span class="sxs-lookup"><span data-stu-id="0594e-104">This method returns a device associated with the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0594e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0594e-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="0594e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0594e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0594e-107">*riid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0594e-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0594e-108">IID de l’appareil à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0594e-108">The IID of the device to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0594e-109">*PPV* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0594e-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0594e-110">Lorsque cette méthode est retournée avec succès, contient le pointeur d’appareil demandé dans le paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="0594e-110">When this method returns successfully, contains the device pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0594e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0594e-111">Return value</span></span>

<span data-ttu-id="0594e-112">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="0594e-112">Returns S\_OK on successful completion.</span></span>

## <a name="see-also"></a><span data-ttu-id="0594e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0594e-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0594e-114">**IVideoFrameNative**</span><span class="sxs-lookup"><span data-stu-id="0594e-114">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



