---
description: Initialisation de Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Initialisation de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106532363"
---
# <a name="initializing-media-foundation"></a><span data-ttu-id="f2492-103">Initialisation de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2492-103">Initializing Media Foundation</span></span>

<span data-ttu-id="f2492-104">Avant d’utiliser des objets ou des interfaces Microsoft Media Foundation, vous devez appeler la fonction [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="f2492-104">Before using any Microsoft Media Foundation objects or interfaces, you must call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="f2492-105">Transmettez la **\_ version** de la constante MF.</span><span class="sxs-lookup"><span data-stu-id="f2492-105">Pass in the constant **MF\_VERSION**.</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



<span data-ttu-id="f2492-106">La fonction [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) initialise la plateforme Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f2492-106">The [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function initializes the Media Foundation platform.</span></span> <span data-ttu-id="f2492-107">Si **MFStartup** retourne MF \_ E \_ mauvaise \_ \_ version de démarrage, cela signifie que votre application a été compilée à l’aide d’une version des en-têtes de Media Foundation qui ne correspond pas à la Media Foundation dll sur votre système.</span><span class="sxs-lookup"><span data-stu-id="f2492-107">If **MFStartup** returns MF\_E\_BAD\_STARTUP\_VERSION, it means your application was compiled using a version of the Media Foundation headers that does not match the Media Foundation DLLs on your system.</span></span>

<span data-ttu-id="f2492-108">Pour chaque appel à [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), votre application doit appeler [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="f2492-108">For every call to [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), your application must call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>


```C++
MFShutdown();
```



## <a name="related-topics"></a><span data-ttu-id="f2492-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f2492-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2492-110">Architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2492-110">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="f2492-111">API de plateforme Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f2492-111">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



