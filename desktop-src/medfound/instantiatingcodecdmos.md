---
description: Instanciation du codec DMOs
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Instanciation du codec DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b98848b3e3fee5b3c28389294869eb39005c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951152"
---
# <a name="instantiating-codec-dmos"></a>Instanciation du codec DMOs

Vous pouvez créer un codec DMO en appelant la fonction com [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . Vous devez transmettre l’identificateur de classe de DMO, l’identificateur d’interface de **IMediaObject** et un pointeur vers un pointeur **IMediaObject** .

Les identificateurs de classe du codec DMOs sont définis en tant que constantes dans le fichier d’en-tête wmcodecdsp. h.

La constante de l’identificateur d’interface **IMediaObject** est IID \_ IMediaObject.

L’exemple de code suivant montre comment créer une instance d’un codec DMO :


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

 

 
