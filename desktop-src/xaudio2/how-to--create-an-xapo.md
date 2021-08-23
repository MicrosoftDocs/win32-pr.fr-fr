---
description: L’API XAPO fournit l’interface IXAPO et la classe CXAPOBase pour la génération de nouveaux types XAPO.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: 'Procédure : Créer un XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea17729c5a6d872d98443c85f79dc72e8eee6dd2233b99f31e189a9eb28708e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583849"
---
# <a name="how-to-create-an-xapo"></a>Procédure : Créer un XAPO

L’API XAPO fournit l’interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) et la classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) pour la génération de nouveaux types XAPO. L’interface **IXAPO** contient toutes les méthodes qui doivent être implémentées pour créer un nouveau XAPO. La classe **CXAPOBase** fournit une implémentation de base de l’interface **IXAPO** . **CXAPOBase** implémente toutes les méthodes d’interface **IXAPO** , à l’exception de la méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , qui est unique à chaque XAPO.

## <a name="to-create-a-new-static-xapo"></a>Pour créer un XAPO statique

1.  Dérivez une nouvelle classe XAPO à partir de la classe de base [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .

    > [!Note]  
    > XAPOs implémente l’interface **IUnknown** . Les interfaces [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) et [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluent les trois méthodes **IUnknown** : **QueryInterface**, **AddRef** et **Release**. [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) fournit des implémentations des trois méthodes **IUnknown** . Une nouvelle instance de **CXAPOBase** aura un compte de référence de 1. Elle sera détruite quand son décompte de références devient 0. Pour permettre à XAudio2 de détruire une instance d’un XAPO lorsqu’il n’est plus nécessaire, appelez **IUnknown :: Release** sur le XAPO après qu’il a été ajouté à une chaîne d’effet XAudio2. Pour plus d’informations sur l’utilisation d’un XAPO avec XAudio2, voir [How to : Use an XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md) .

     

2.  Substituez l’implémentation de la classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) de la méthode [**IXAPO :: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .

    Le remplacement de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) permet d’obtenir des informations sur le format des données audio à stocker en vue de leur utilisation dans [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

3.  Implémentez la méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) .

    XAudio2 appelle la méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) chaque fois qu’un XAPO doit traiter des données audio. Le **processus** contient l’essentiel du code pour un XAPO.

## <a name="implementing-the-process-method"></a>Implémentation de la méthode Process

La méthode [**IXAPO ::P tionnaire**](/windows/win32/api/xapo/nf-xapo-ixapo-process) accepte les mémoires tampons de flux pour les données audio d’entrée et de sortie. Un XAPO classique attend une mémoire tampon de flux d’entrée et une mémoire tampon de flux de sortie. Vous devez baser le traitement des données à partir de la mémoire tampon du flux d’entrée au format spécifié dans la fonction [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) et tous les indicateurs passés à la fonction de **traitement** avec la mémoire tampon du flux d’entrée. Copiez les données de mémoire tampon du flux d’entrée traitées dans la mémoire tampon du flux de sortie. Définissez le paramètre BufferFlags de la mémoire tampon du flux de sortie en tant que tampon [**XAPO \_ \_ valide**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) ou **XAPO en \_ \_ mode silencieux**.

L’exemple suivant illustre une implémentation de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) et de [**processus**](/windows/win32/api/xapo/nf-xapo-ixapo-process) qui copie simplement les données d’une mémoire tampon d’entrée vers une mémoire tampon de sortie. Toutefois, il n’y a aucun traitement si la mémoire tampon d’entrée est marquée avec le [**\_ \_ mode silencieux de la mémoire tampon XAPO**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).


```
STDMETHOD(LockForProcess) (UINT32 InputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pInputLockedParameters,
          UINT32 OutputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pOutputLockedParameters)
{
    assert(!IsLocked());
    assert(InputLockedParameterCount == 1);
    assert(OutputLockedParameterCount == 1);
    assert(pInputLockedParameters != NULL);
    assert(pOutputLockedParameters != NULL);
    assert(pInputLockedParameters[0].pFormat != NULL);
    assert(pOutputLockedParameters[0].pFormat != NULL);


    m_uChannels = pInputLockedParameters[0].pFormat->nChannels;
    m_uBytesPerSample = (pInputLockedParameters[0].pFormat->wBitsPerSample >> 3);

    return CXAPOBase::LockForProcess(
        InputLockedParameterCount,
        pInputLockedParameters,
        OutputLockedParameterCount,
        pOutputLockedParameters);
}
STDMETHOD_(void, Process)(UINT32 InputProcessParameterCount,
           const XAPO_PROCESS_BUFFER_PARAMETERS* pInputProcessParameters,
           UINT32 OutputProcessParameterCount,
           XAPO_PROCESS_BUFFER_PARAMETERS* pOutputProcessParameters,
           BOOL IsEnabled)
{
    assert(IsLocked());
    assert(InputProcessParameterCount == 1);
    assert(OutputProcessParameterCount == 1);
    assert(NULL != pInputProcessParameters);
    assert(NULL != pOutputProcessParameters);


    XAPO_BUFFER_FLAGS inFlags = pInputProcessParameters[0].BufferFlags;
    XAPO_BUFFER_FLAGS outFlags = pOutputProcessParameters[0].BufferFlags;

    // assert buffer flags are legitimate
    assert(inFlags == XAPO_BUFFER_VALID || inFlags == XAPO_BUFFER_SILENT);
    assert(outFlags == XAPO_BUFFER_VALID || outFlags == XAPO_BUFFER_SILENT);

    // check input APO_BUFFER_FLAGS
    switch (inFlags)
    {
    case XAPO_BUFFER_VALID:
        {
            void* pvSrc = pInputProcessParameters[0].pBuffer;
            assert(pvSrc != NULL);

            void* pvDst = pOutputProcessParameters[0].pBuffer;
            assert(pvDst != NULL);

            memcpy(pvDst,pvSrc,pInputProcessParameters[0].ValidFrameCount * m_uChannels * m_uBytesPerSample);
            break;
        }

    case XAPO_BUFFER_SILENT:
        {
            // All that needs to be done for this case is setting the
            // output buffer flag to XAPO_BUFFER_SILENT which is done below.
            break;
        }

    }

    // set destination valid frame count, and buffer flags
    pOutputProcessParameters[0].ValidFrameCount = pInputProcessParameters[0].ValidFrameCount; // set destination frame count same as source
    pOutputProcessParameters[0].BufferFlags     = pInputProcessParameters[0].BufferFlags;     // set destination buffer flags same as source

}
```



Lors de l’écriture d’une méthode de [**processus**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , il est important de noter que les données audio XAudio2 sont entrelacées. Cela signifie que les données de chaque canal sont adjacentes pour un exemple de numéro particulier. Par exemple, si une vague à 4 canaux est lue dans une voix source XAudio2, les données audio sont un exemple de canal 0, un exemple de canal 1, un exemple de canal 2, un exemple de canal 3, puis l’échantillon suivant de canaux 0, 1, 2, 3, etc.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets audio](audio-effects.md)
</dt> <dt>

[Présentation de XAPO](xapo-overview.md)
</dt> </dl>

 

 
