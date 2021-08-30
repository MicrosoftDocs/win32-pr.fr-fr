---
title: Variables pour effectuer le traitement
description: Variables pour effectuer le traitement
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- plug-ins Lecteur Windows Media, méthode DoProcessOutput d’exemple Echo
- plug-ins, ECHO, exemple DoProcessOutput, méthode
- plug-ins de traitement de signal numérique, méthode DoProcessOutput d’exemple Echo
- DSP plug-ins, ECHO, exemple DoProcessOutput, méthode
- Echo DSP, exemple de plug-in, méthode DoProcessOutput
- Echo DSP, exemple de plug-in, traitement de variables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f856808c1e9a00602fe3d2fe03d4255fd79bcfeb44c2021f2434ea670706cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001339"
---
# <a name="variables-to-perform-processing"></a>Variables pour effectuer le traitement

Les variables membres pour la gestion de la mémoire tampon de délai traitent les quantités en **octets** ; Il s’agit de pointeurs d' **octets** et d’un entier qui stocke un nombre d’octets. Cela est idéal pour le traitement de données audio 8 bits, car un échantillon de 8 bits s’intègre parfaitement dans un octet de mémoire. Toutefois, lors du traitement de l’audio 16 bits, il est plus pratique de les convertir en pointeurs **courts** , de sorte que le traitement peut se produire deux octets à la fois.

L’exemple de code suivant alloue les nouveaux pointeurs 16 bits et ajoute une variable pointeur qui stocke l’adresse de la fin de la mémoire tampon de délai. Insérez-le dans la section « case 16 » juste avant le point d’entrée de boucle :


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



Le code pour le traitement 8 bits alloue également une variable qui stocke l’adresse de la fin de la mémoire tampon de délai. Le stockage de cette valeur permet de tester facilement si le pointeur de la mémoire tampon de délai mobile a atteint la fin de la mémoire tampon de délai. L’exemple de code suivant calcule la valeur :


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation de CEcho ::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




