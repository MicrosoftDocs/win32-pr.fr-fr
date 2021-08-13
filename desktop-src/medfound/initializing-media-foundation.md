---
description: Initialisation de Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Initialisation de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202ab57db5821b252001a723eb8765493eb86362111da5c54e5e16e9fca4219a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268919"
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

 

 



