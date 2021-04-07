---
title: Capacités du pilote de capture
description: Capacités du pilote de capture
ms.assetid: 6e74635e-9dac-419d-a264-08fee04ae7b7
keywords:
- Message WM_CAP_DRIVER_GET_CAPS
- capDriverGetCaps macro)
- CAPDRIVERCAPS, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87fb4f9cb439229721b6c10aa6207af601f9ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028810"
---
# <a name="capture-driver-capabilities"></a><span data-ttu-id="79f4a-106">Capacités du pilote de capture</span><span class="sxs-lookup"><span data-stu-id="79f4a-106">Capture Driver Capabilities</span></span>

<span data-ttu-id="79f4a-107">Vous pouvez récupérer les fonctionnalités matérielles du pilote de capture actuellement connecté à l’aide du message de la [**\_ prise en main du pilote WM Cap \_ \_ \_**](wm-cap-driver-get-caps.md) (ou de la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) ).</span><span class="sxs-lookup"><span data-stu-id="79f4a-107">You can retrieve the hardware capabilities of the currently connected capture driver by using the [**WM\_CAP\_DRIVER\_GET\_CAPS**](wm-cap-driver-get-caps.md) message (or the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro).</span></span> <span data-ttu-id="79f4a-108">Ce message retourne les fonctionnalités du pilote de capture et du matériel sous-jacent dans la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="79f4a-108">This message returns the capabilities of the capture driver and underlying hardware in the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

 

 




