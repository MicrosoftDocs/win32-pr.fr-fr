---
title: Création de l’effet Echo
description: Création de l’effet Echo
ms.assetid: 3fac6c74-8221-4656-997b-0f903fae85b7
keywords:
- plug-ins Lecteur Windows Media, méthode DoProcessOutput d’exemple Echo
- plug-ins, ECHO, exemple DoProcessOutput, méthode
- plug-ins de traitement de signal numérique, méthode DoProcessOutput d’exemple Echo
- DSP plug-ins, ECHO, exemple DoProcessOutput, méthode
- Echo DSP, exemple de plug-in, méthode DoProcessOutput
- Echo DSP, exemple de plug-in, création d’un effet d’écho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e978562ff4cdee016f92409d183990cd4bb178b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919279"
---
# <a name="creating-the-echo-effect"></a>Création de l’effet Echo

Vous devez d’abord supprimer le code de l’exemple d’assistant qui met à l’échelle l’audio. Dans la section 8 bits, supprimez le code suivant :


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



(N’oubliez pas que m \_ fScaleFactor a été remplacé par m \_ dwDelayTime.)

Dans la section 16 bits, supprimez le code suivant :


```C++
// Apply scale factor to sample.
i = int( ((double) i) * m_dwDelayTime );

```



l’implémentation de **DoProcessOutput** fournie par l’exemple de code de l’assistant de plug-in crée une boucle while qui itère une fois pour chaque échantillon dans la mémoire tampon d’entrée fournie par Lecteur Windows Media. Cette boucle fonctionne de la même façon pour les données audio 8 bits et 16 bits, bien qu’une boucle distincte soit requise pour chacune d’elles. Dans chaque cas, la boucle démarre avec le test suivant :


```C++
while (dwSamplesToProcess--)

```



Une fois à l’intérieur de la boucle, les routines de traitement sont très similaires pour les fichiers audio 8 bits et 16 bits. La principale différence est que le code de la section 8 bits remplace la plage de valeurs de données par-128 par 127, puis reconvertit la plage avant d’écrire les données dans la mémoire tampon de sortie. Il est important de conserver la symétrie de la forme d’onde audio lors du traitement.

Vous pouvez maintenant commencer à ajouter et à remplacer du code dans la boucle de traitement.

## <a name="retrieve-a-sample-from-the-input-buffer"></a>Récupérer un exemple à partir de la mémoire tampon d’entrée

Pendant chaque itération de la boucle, un seul échantillon est récupéré à partir de la mémoire tampon d’entrée. Pour le son 8 bits, l’échantillon est décalé vers la nouvelle plage, puis le pointeur vers la mémoire tampon d’entrée est avancé jusqu’à l’exemple suivant. Le code suivant provient de l’Assistant de plug-in :


```C++
// Get the input sample and normalize to -128 .. 127
int i = (*pbInputData++) - 128;

```



Pour le son 16 bits, le processus est le même, à l’exception de la normalisation :


```C++
// Get the input sample.
int i = *pwInputData++;

```



N’oubliez pas que les pointeurs du code 16 bits ont été convertis en type **short**.

## <a name="retrieve-a-sample-from-the-delay-buffer"></a>Récupérer un échantillon de la mémoire tampon de délai

Ensuite, récupérez un seul échantillon de la mémoire tampon de délai. Pour le code 8 bits, les échantillons de délai sont stockés dans leur plage Native comprise entre 0 et 255. Le code suivant, que vous devez ajouter, récupère un exemple de délai 8 bits :


```C++
// Get the delay sample and normalize to -128 .. 127
int delay = m_pbDelayPointer[0] - 128;

```



Pour le son 16 bits, le processus est similaire :


```C++
// Get the delay sample.
int delay = *pwDelayPointer;

```



## <a name="write-the-input-sample-to-the-delay-buffer"></a>Écrire l’exemple d’entrée dans le tampon de délai

À présent, vous devez stocker l’exemple d’entrée dans le tampon de délai dans le même emplacement que celui à partir duquel vous avez récupéré l’exemple Delay. Voici le code que vous devez ajouter pour l’audio 8 bits :


```C++
// Write the input sample into the delay buffer.
m_pbDelayPointer[0] = i + 128;

```



Voici le code à ajouter pour la section 16 bits :


```C++
// Write the input sample to the delay buffer.
*pwDelayPointer = i;

```



## <a name="move-the-delay-buffer-pointer"></a>Déplacer le pointeur de mémoire tampon de délai

Maintenant que le travail dans la mémoire tampon de délai est terminé pour cette itération, vous pouvez avancer le pointeur mobile sur la mémoire tampon de délai. Si le pointeur atteint la fin de la mémoire tampon circulaire, vous devez modifier sa valeur pour qu’elle pointe vers l’en-tête de la mémoire tampon. Pour ce faire, utilisez le code suivant :


```C++
// Increment the delay pointer.
// If it has passed the end of the buffer,
// then move it to the head of the buffer.
if (++m_pbDelayPointer > pbEOFDelayBuffer)
    m_pbDelayPointer = m_pbDelayBuffer;

```



Voici le code de la section 16 bits :


```C++
// Increment the local delay pointer.
// If it is past the end of the buffer,
// then move it to the head of the buffer.
if (++pwDelayPointer > pwEOFDelayBuffer)
    pwDelayPointer = pwDelayBuffer;

```



Étant donné que le pointeur dans la section 16 bits est en réalité une copie de la variable membre, vous devez penser à mettre à jour la valeur dans la variable membre avec la nouvelle adresse. Si vous ne le faites pas, le pointeur de mémoire tampon de délai pointera vers la tête de la mémoire tampon à plusieurs reprises et votre effet d’écho ne fonctionnera pas comme prévu. Ajoutez le code suivant à la section 16 bits :


```C++
// Move the global delay pointer.
m_pbDelayPointer = (BYTE *) pwDelayPointer;

```



## <a name="mix-the-input-sample-with-the-delay-sample"></a>Mélanger l’exemple d’entrée avec l’exemple Delay

C’est là que vous utilisez les valeurs de mélange humide et à sec pour créer l’échantillon de sortie final. Vous multipliez simplement chaque échantillon par la valeur à virgule flottante qui représente le pourcentage du signal final de l’échantillon. Multipliez l’exemple d’entrée par la valeur stockée dans m \_ fDryMix ; multipliez l’exemple Delay par la valeur stockée dans m \_ fWetMix. Ajoutez ensuite les deux valeurs. Le code que vous devez ajouter est identique pour les sections 8 bits et 16 bits :


```C++
// Mix the delay with the dry signal.
i = (int)((i * m_fDryMix ) + (delay * m_fWetMix));   

```



## <a name="write-the-data-to-the-output-buffer"></a>Écrire les données dans la mémoire tampon de sortie

Enfin, copiez l’échantillon mixte dans la mémoire tampon de sortie, puis avancez le pointeur de la mémoire tampon de sortie. Pour l’audio 8 bits, l’Assistant de plug-in utilise le code suivant pour retourner l’exemple à sa plage d’origine :


```C++
// Convert back to 0..255 and write to output buffer.
*pbOutputData++ = (BYTE)(i + 128);

```



Pour le son 16 bits, l’Assistant utilise le code suivant comme dernière étape de la boucle de traitement :


```C++
// Write to output buffer.
*pwOutputData++ = i;

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de CEcho ::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




