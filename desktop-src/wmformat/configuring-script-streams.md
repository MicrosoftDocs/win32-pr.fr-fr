---
title: Configuration de flux de script
description: Configuration de flux de script
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- flux, configuration de flux de script
- codecs, configuration de flux de script
- flux de script, configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029083"
---
# <a name="configuring-script-streams"></a><span data-ttu-id="9b2e2-106">Configuration de flux de script</span><span class="sxs-lookup"><span data-stu-id="9b2e2-106">Configuring Script Streams</span></span>

<span data-ttu-id="9b2e2-107">Comme tous les types de flux arbitraires, les flux de script doivent avoir une fenêtre de mémoire tampon et une vitesse de transmission définies pour eux.</span><span class="sxs-lookup"><span data-stu-id="9b2e2-107">Like all arbitrary stream types, script streams need to have a bit rate and buffer window defined for them.</span></span> <span data-ttu-id="9b2e2-108">Le type de média majeur dans la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) doit être défini sur WMMEDIATYPE \_ script.</span><span class="sxs-lookup"><span data-stu-id="9b2e2-108">The major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure must be set to WMMEDIATYPE\_Script.</span></span>

<span data-ttu-id="9b2e2-109">Les flux de script doivent avoir le membre **formatType** du **\_ \_ type de média WM** défini sur WMFORMAT \_ script, qui indique que le membre **pbFormat** pointe vers une structure [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) .</span><span class="sxs-lookup"><span data-stu-id="9b2e2-109">Script streams need to have the **formattype** member of **WM\_MEDIA\_TYPE** set to WMFORMAT\_Script, which indicates that the **pbFormat** member points to a [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) structure.</span></span>

<span data-ttu-id="9b2e2-110">Il n’existe qu’un seul type de script pris en charge, WMSCRIPTTYPE \_ TwoStrings.</span><span class="sxs-lookup"><span data-stu-id="9b2e2-110">There is only one supported script type, WMSCRIPTTYPE\_TwoStrings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b2e2-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b2e2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b2e2-112">**Configuration commune à tous les flux**</span><span class="sxs-lookup"><span data-stu-id="9b2e2-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="9b2e2-113">**Configuration de types de flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="9b2e2-113">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="9b2e2-114">**Commandes de script**</span><span class="sxs-lookup"><span data-stu-id="9b2e2-114">**Script Commands**</span></span>](script-commands.md)
</dt> </dl>

 

 




