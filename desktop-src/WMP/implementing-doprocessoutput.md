---
title: Implémentation de DoProcessOutput
description: Implémentation de DoProcessOutput
ms.assetid: c6fbcfc0-741b-4aa7-9109-e06810a2e081
keywords:
- plug-ins Lecteur Windows Media, DSP audio
- plug-ins, DSP audio
- plug-ins de traitement de signal numérique, DoProcessOutput
- Plug-ins DSP, DoProcessOutput
- plug-ins DSP audio, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2f5aa1a952f16de196bed72ed7ac93dfac95d8333496824e3f0740f506a6fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135582"
---
# <a name="implementing-doprocessoutput"></a>Implémentation de DoProcessOutput

Pour traiter des données audio, vous devez effectuer plusieurs étapes dans **DoProcessOutput**. Les étapes suivantes utilisent l’exemple de code de l’Assistant de plug-in comme exemples. Si vous souhaitez créer un plug-in DSP audio qui traite le contenu multimédia du même type que l’exemple de code de l’Assistant de plug-in, vous devez uniquement modifier le code de traitement réel mentionné à l’étape 6. Voici toutes les étapes implémentées dans **DoProcessOutput**:

-   Si le plug-in n’est pas activé actuellement, copiez simplement les données inchangées dans la mémoire tampon de sortie. Si votre plug-in convertit les données dans un format différent, vous devez également effectuer le traitement de la conversion ici.

    ```C++
    // Test whether the plug-in is disabled by the user.
    if (!m_bEnabled)
    {
        // Just copy the data without changing it.
        memcpy(pbOutputData, m_pbInputData, *cbBytesProcessed);

        return S_OK;
    }
    
    ```

    

    -   Récupère un pointeur vers la structure du format d’entrée. Vous devez récupérer les données de membre de cette structure, copiez donc le pointeur de *m \_ mtInput*.**pbformat** à une variable de pointeur locale d’un type qui correspond au type de structure de format. L’exemple suivant stocke un pointeur vers une structure de format d’entrée **WAVEFORMATEX** :

    ```C++
    WAVEFORMATEX *pWave = (WAVEFORMATEX*) m_mtInput.pbFormat;
    
    ```

    

    -   Calculez le nombre d’échantillons à traiter. L’exemple de code généré par l’Assistant de plug-in effectue cette étape en divisant le nombre d’octets à traiter par le membre **nBlockAlign** de la structure de format d’entrée WAVEFORMATEX, puis en multipliant le résultat par le nombre de canaux, qui était stocké dans le membre **nChannels** . L’exemple suivant provient de l’exemple de code de l’Assistant de plug-in :

    ```C++
    DWORD dwSamplesToProcess = (cbBytesProcessed / pWave->nBlockAlign) * pWave->nChannels;
    
    ```

    

    1.  Déterminez la profondeur de bits de l’audio. L’exemple de code de l’Assistant de plug-in détermine l’audio 8 bits ou 16 bits en inspectant le membre **wBitsPerSample** de la structure **WAVEFORMATEX** . Il utilise ensuite cette valeur dans une instruction switch pour fournir des routines de traitement distinctes pour chaque profondeur de bit. Vous devrez peut-être utiliser une autre technique pour traiter d’autres types de format et de profondes de bits.
    2.  Créez une boucle pour parcourir les exemples audio dans la mémoire tampon d’entrée.
    3.  Récupérez un exemple de la mémoire tampon d’entrée. Pour ce faire, vous devez déréférencer le pointeur de données d’entrée et stocker le résultat dans une variable de type int. Pour le son 16 bits, vous devez effectuer un reconversion du pointeur d’octet vers un pointeur vers le petit pour gérer la plus grande précision de l’échantillon audio. Une fois que vous avez la valeur, vous pouvez incrémenter immédiatement le pointeur *pbInputData* pour qu’il pointe vers l’exemple suivant. Les exemples suivants illustrent ce cas :

    ```C++
    // For 8-bit audio.
    int i = *pbInputData++;  
    
    ```

    

    -ou-

    ```C++
    // For 16-bit audio.
    // Recast the pointer.
    short *pwInputData = (short *) pbInputData; 

    // Enter the loop and then get the input sample.
    int i = *pwInputData++;
    
    ```

    

    1.  Effectuez le traitement. C’est là que vous appliquez les algorithmes qui modifient l’exemple. Voici ce que vous devez faire ici.
    2.  Écrire les données traitées dans la mémoire tampon de sortie. Incrémentez immédiatement le pointeur vers la mémoire tampon de sortie, comme dans l’exemple suivant :

    ```C++
    *pwOutputData++ = i;
    
    ```

    

    1.  Répétez la boucle jusqu’à ce que tous les échantillons aient été traités.
    2.  Retourne un **HRESULT** approprié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation d’un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




