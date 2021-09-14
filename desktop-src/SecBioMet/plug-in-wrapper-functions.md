---
title: Fonctions wrapper de plug-in
description: Fonctions wrapper qui vous permettent d’appeler une fonction publique sur n’importe quel adaptateur attaché au pipeline sans acquérir manuellement un pointeur vers l’adaptateur.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- Windows api de l’infrastructure biométrique Windows Biometric Framework, fonctions wrapper de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237864"
---
# <a name="plug-in-wrapper-functions"></a>Fonctions wrapper de plug-in

l’API Windows Biometric Framework comprend des fonctions wrapper qui vous permettent d’appeler une fonction publique sur n’importe quel adaptateur attaché au pipeline sans avoir à acquérir manuellement un pointeur vers l’adaptateur. Chaque Wrapper vérifie les arguments d’entrée, récupère un pointeur d’adaptateur et appelle la fonction demandée. Par exemple, le wrapper **WbioEngineSetHashAlgorithm** a la signature suivante.


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



La fonction vérifie que l’argument de *pipeline* n’est pas **null**, qu’il existe un adaptateur de moteur et que la fonction [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) existe. Toutes les fonctions wrapper sont définies dans le \_ fichier d’en-tête WinBio adapter. h. Les rubriques suivantes décrivent les wrappers disponibles.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                               | Description                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Wrappers d’adaptateur de moteur](engine-adapter-wrappers.md)<br/>   | Fonctions que vous pouvez utiliser pour appeler des fonctions sur votre adaptateur de moteur. Ces fonctions sont définies dans WinBio \_ adapter. h.<br/>  |
| [Wrappers d’adaptateur de capteur](sensor-adapter-wrappers.md)<br/>   | Fonctions que vous pouvez utiliser pour appeler des fonctions sur votre adaptateur de capteur. Ces fonctions sont définies dans WinBio \_ adapter. h.<br/>  |
| [Stockage Wrappers d’adaptateur](storage-adapter-wrappers.md)<br/> | Fonctions que vous pouvez utiliser pour appeler des fonctions sur votre adaptateur de stockage. Ces fonctions sont définies dans WinBio \_ adapter. h.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du plug-in](plug-in-reference.md)
</dt> </dl>

 

 





