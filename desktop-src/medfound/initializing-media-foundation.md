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
# <a name="initializing-media-foundation"></a>Initialisation de Media Foundation

Avant d’utiliser des objets ou des interfaces Microsoft Media Foundation, vous devez appeler la fonction [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) . Transmettez la **\_ version** de la constante MF.


```C++
    hr = MFStartup(MF_VERSION);
```



La fonction [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) initialise la plateforme Media Foundation. Si **MFStartup** retourne MF \_ E \_ mauvaise \_ \_ version de démarrage, cela signifie que votre application a été compilée à l’aide d’une version des en-têtes de Media Foundation qui ne correspond pas à la Media Foundation dll sur votre système.

Pour chaque appel à [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), votre application doit appeler [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).


```C++
MFShutdown();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Architecture Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[API de plateforme Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



