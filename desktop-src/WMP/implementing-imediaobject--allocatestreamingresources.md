---
title: Implémentation de IMediaObject AllocateStreamingResources
description: Implémentation de IMediaObject AllocateStreamingResources
ms.assetid: 630550fe-2cca-4bfa-a824-a355f7fc5e02
keywords:
- plug-ins Lecteur Windows Media, ressources de streaming d’exemples Echo
- plug-ins, exemples de ressources de streaming
- plug-ins de traitement de signal numérique, exemples de ressources de streaming d’écho
- Plug-ins DSP, exemples de ressources de streaming
- Echo DSP, exemple de plug-in, ressources de streaming
- Echo DSP, exemple de plug-in, tampon de délai
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291b1f9627d9dfb78ae2aff9d34b6fadd47cbf28a5c2f0830f5833d9e83cde21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508959"
---
# <a name="implementing-imediaobjectallocatestreamingresources"></a>Implémentation de IMediaObject :: AllocateStreamingResources

Dans l’exemple Echo, la méthode **AllocateStreamingResources** crée la mémoire tampon de délai. Pour ce faire, il effectue les opérations suivantes :

1.  Calcul de la taille de la mémoire tampon qui correspond au délai spécifié pour le type de média donné.
2.  Allouez une nouvelle mémoire ou réallouez la taille de la mémoire tampon si elle existe déjà.
3.  Appel d’une méthode qui remplit la mémoire tampon avec des valeurs représentant le silence.

La valeur de silence est différente selon la profondeur de bit. Pour le son 8 bits, le silence est représenté par la valeur hexadécimale 80 ; pour le son 16 bits, le silence est représenté par zéro.

## <a name="calculating-the-delay-buffer-size"></a>Calcul de la taille de la mémoire tampon de délai

Pour calculer la taille requise pour la mémoire tampon de délai, vous devez d’abord récupérer une structure **WAVEFORMATEX** qui contient des informations sur les données audio. l’exemple suivant récupère un pointeur vers cette structure à partir de l’entrée DMO structure du **\_ \_ TYPE de média** :


```
// Get a pointer to the WAVEFORMATEX structure.
WAVEFORMATEX *pWave = ( WAVEFORMATEX * ) m_mtInput.pbFormat;
if (NULL == pWave)
{
    return E_FAIL;
}
```



Une fois que vous avez stocké un pointeur vers la structure **WAVEFORMATEX** appropriée, vous pouvez inspecter ses membres et les utiliser pour calculer la taille de mémoire tampon requise. L’exemple de code suivant illustre ceci :


```
// Get the size of the buffer required.
m_cbDelayBuffer = (m_dwDelayTime * pWave->nSamplesPerSec * pWave->nBlockAlign) / 1000;
```



Cet algorithme calcule la taille de la mémoire tampon en multipliant le délai, en millisecondes, du nombre d’échantillons par milliseconde, puis en multipliant le résultat par le nombre de canaux, puis en multipliant le résultat par le nombre d’octets par échantillon. Le nombre de canaux et le nombre d’octets par échantillon ne sont pas évidents ; elles sont encodées dans le membre nBlockAlign. La division par 1000 réduit la valeur nSamplesPerSec à des échantillons par milliseconde. la milliseconde est l’unité souhaitée, car le délai est exprimé en millisecondes.

## <a name="allocating-the-delay-buffer-memory"></a>Allocation de la mémoire tampon de délai

Une fois que vous avez calculé les besoins en mémoire, vous pouvez allouer la mémoire tampon. Il peut être nécessaire de supprimer la mémoire tampon, le cas échéant, par exemple lorsque l’utilisateur appelle la page de propriétés pour modifier la valeur du délai. Le code suivant illustre l’allocation de la mémoire tampon de délai :


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    // A buffer already exists.
    // Delete the delay buffer.
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
}

// Allocate the buffer.
m_pbDelayBuffer = new BYTE[m_cbDelayBuffer];

if (!m_pbDelayBuffer)
    return E_OUTOFMEMORY;
```



Si la mémoire tampon est correctement allouée, vous devez déplacer le pointeur mobile vers l’en-tête de la mémoire tampon, comme illustré dans l’exemple suivant :


```
// Move the echo pointer to the head of the delay buffer.
m_pbDelayPointer = m_pbDelayBuffer;
```



## <a name="filling-the-delay-buffer-with-silence"></a>Remplissage de la mémoire tampon de délai avec silence

Il est pratique d’écrire une méthode pour remplir la mémoire tampon de délai avec des valeurs représentant le silence. La méthode doit recevoir le pointeur vers la structure WAVEFORMATEX valide, puis inspecter le membre wBitsPerSample pour déterminer si le son est 8 bits ou supérieur. L’exemple suivant remplit la mémoire tampon de délai avec la valeur correcte pour le silence :


```
void CEcho::FillBufferWithSilence(WAVEFORMATEX *pWfex)
{
    if (8 == pWfex->wBitsPerSample)
    {
    ::FillMemory(m_pbDelayBuffer, m_cbDelayBuffer, 0x80);
    }
    else
    ::ZeroMemory(m_pbDelayBuffer, m_cbDelayBuffer);
}
```



N’oubliez pas d’ajouter la déclaration anticipée pour la fonction au fichier d’en-tête Echo. h dans la section private :


```
void FillBufferWithSilence(WAVEFORMATEX *pWfex);
```



Vous devez ajouter du code à la fin de AllocateStreamingResources pour appeler cette méthode chaque fois que la mémoire tampon de délai est créée ou redimensionnée. L’exemple de code suivant passe le pointeur WAVEFORMATEX nommé pWave à la nouvelle méthode :


```
// Fill the buffer with values representing silence.
FillBufferWithSilence(pWave);
```



## <a name="reallocating-the-delay-buffer-memory"></a>Réallocation de la mémoire tampon de délai

Lorsque l’utilisateur modifie le délai d’attente à l’aide de la page de propriétés, la taille de la mémoire tampon de délai doit également être modifiée. Vous avez déjà ajouté le code à AllocateStreamingResources pour redimensionner la mémoire tampon, mais vous devez ajouter une ligne de code à CEcho ::p \_ délai pour appeler la méthode d’allocation de ressources chaque fois que la valeur de la propriété change. Voici le code :


```
// Reallocate the delay buffer.
AllocateStreamingResources();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des ressources de streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




