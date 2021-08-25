---
description: Instanciation du codec MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Instanciation du codec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a73af4055aee1d5b7e6a3ea137ab2204c9e59194f57ae4776e6c8368429db877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827609"
---
# <a name="instantiating-codec-mfts"></a>Instanciation du codec MFTs

Les [transformations de Media Foundation](media-foundation-transforms.md) (MFTS) sont des objets COM qui implémentent l’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) . Une table MFT est un objet permettant de transformer des données multimédias dans le cadre d’un pipeline. Un pipeline est un graphique acycliques dirigé, qui se compose de sources multimédias, de transformations multimédia et de récepteurs multimédias. Un pipeline traite la diffusion en continu de données multimédias de manière asynchrone.

Bien que MFTs puisse être instancié et utilisé indépendamment de l’infrastructure de pipeline Media Foundation, il est préférable d’utiliser l’infrastructure MediaFoundation dans la mesure du possible.

Vous pouvez créer une table MFT de codec en appelant la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . Vous devez passer l’identificateur de classe de la table MFT, l’identificateur d’interface de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)et un pointeur vers un pointeur **IMFTransform** .

Les identificateurs de classe du codec MFTs sont définis en tant que constantes dans le fichier d’en-tête wmcodecdsp. h.

La constante de l’identificateur d’interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) est IID \_ IMFTransform.

L’exemple de code suivant montre comment créer une instance d’une table MFT de codec :


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 
