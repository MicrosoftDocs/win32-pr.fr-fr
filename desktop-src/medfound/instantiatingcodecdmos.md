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
# <a name="instantiating-codec-dmos"></a><span data-ttu-id="53ae0-103">Instanciation du codec DMOs</span><span class="sxs-lookup"><span data-stu-id="53ae0-103">Instantiating Codec DMOs</span></span>

<span data-ttu-id="53ae0-104">Vous pouvez créer un codec DMO en appelant la fonction com [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="53ae0-104">You can create a codec DMO by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="53ae0-105">Vous devez transmettre l’identificateur de classe de DMO, l’identificateur d’interface de **IMediaObject** et un pointeur vers un pointeur **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="53ae0-105">You must pass the class identifier of the DMO, the interface identifier of **IMediaObject**, and a pointer to an **IMediaObject** pointer.</span></span>

<span data-ttu-id="53ae0-106">Les identificateurs de classe du codec DMOs sont définis en tant que constantes dans le fichier d’en-tête wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="53ae0-106">The class identifiers of the codec DMOs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="53ae0-107">La constante de l’identificateur d’interface **IMediaObject** est IID \_ IMediaObject.</span><span class="sxs-lookup"><span data-stu-id="53ae0-107">The constant for the **IMediaObject** interface identifier is IID\_IMediaObject.</span></span>

<span data-ttu-id="53ae0-108">L’exemple de code suivant montre comment créer une instance d’un codec DMO :</span><span class="sxs-lookup"><span data-stu-id="53ae0-108">The following code example demonstrates how to create an instance of a codec DMO:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="53ae0-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53ae0-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53ae0-110">Utilisation du codec DMOs</span><span class="sxs-lookup"><span data-stu-id="53ae0-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
