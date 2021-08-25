---
description: Instanciation du codec DMOs
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Instanciation du codec DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180fcb6a3de7c581f48c7f78981e12b544963cbfb590e521d43413732bcc1e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957549"
---
# <a name="instantiating-codec-dmos"></a>Instanciation du codec DMOs

vous pouvez créer un DMO de codec en appelant la fonction COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . vous devez passer l’identificateur de classe de la DMO, l’identificateur d’interface de **IMediaObject** et un pointeur vers un pointeur **IMediaObject** .

Les identificateurs de classe du codec DMOs sont définis en tant que constantes dans le fichier d’en-tête wmcodecdsp. h.

La constante de l’identificateur d’interface **IMediaObject** est IID \_ IMediaObject.

L’exemple de code suivant montre comment créer une instance d’un DMO de codec :


```
HRESULT CreateVideoEncoderDMO(IMediaObject** ppDMO)
{
    if(ppDMO == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMediaObject, 
                            (void**)ppDMO);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
