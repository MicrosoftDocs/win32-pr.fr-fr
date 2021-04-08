---
title: Variables pour effectuer le traitement
description: Variables pour effectuer le traitement
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Plug-ins du lecteur Windows Media, méthode DoProcessOutput d’exemple Echo
- plug-ins, ECHO, exemple DoProcessOutput, méthode
- plug-ins de traitement de signal numérique, méthode DoProcessOutput d’exemple Echo
- DSP plug-ins, ECHO, exemple DoProcessOutput, méthode
- Echo DSP, exemple de plug-in, méthode DoProcessOutput
- Echo DSP, exemple de plug-in, traitement de variables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673605"
---
# <a name="variables-to-perform-processing"></a><span data-ttu-id="57a9b-109">Variables pour effectuer le traitement</span><span class="sxs-lookup"><span data-stu-id="57a9b-109">Variables to Perform Processing</span></span>

<span data-ttu-id="57a9b-110">Les variables membres pour la gestion de la mémoire tampon de délai traitent les quantités en **octets** ; Il s’agit de pointeurs d' **octets** et d’un entier qui stocke un nombre d’octets.</span><span class="sxs-lookup"><span data-stu-id="57a9b-110">The member variables for handling the delay buffer deal with **BYTE** quantities; they are **BYTE** pointers and an integer that stores a count of bytes.</span></span> <span data-ttu-id="57a9b-111">Cela est idéal pour le traitement de données audio 8 bits, car un échantillon de 8 bits s’intègre parfaitement dans un octet de mémoire.</span><span class="sxs-lookup"><span data-stu-id="57a9b-111">This is ideal for processing 8-bit audio, since an 8-bit sample fits nicely into one byte of memory.</span></span> <span data-ttu-id="57a9b-112">Toutefois, lors du traitement de l’audio 16 bits, il est plus pratique de les convertir en pointeurs **courts** , de sorte que le traitement peut se produire deux octets à la fois.</span><span class="sxs-lookup"><span data-stu-id="57a9b-112">When processing 16-bit audio, though, it is more convenient to convert these to **short** pointers, so the processing can occur two bytes at a time.</span></span>

<span data-ttu-id="57a9b-113">L’exemple de code suivant alloue les nouveaux pointeurs 16 bits et ajoute une variable pointeur qui stocke l’adresse de la fin de la mémoire tampon de délai.</span><span class="sxs-lookup"><span data-stu-id="57a9b-113">The following example code allocates the new 16-bit pointers, and adds a pointer variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="57a9b-114">Insérez-le dans la section « case 16 » juste avant le point d’entrée de boucle :</span><span class="sxs-lookup"><span data-stu-id="57a9b-114">Insert it in the "case 16" section just before the loop entry point:</span></span>


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



<span data-ttu-id="57a9b-115">Le code pour le traitement 8 bits alloue également une variable qui stocke l’adresse de la fin de la mémoire tampon de délai.</span><span class="sxs-lookup"><span data-stu-id="57a9b-115">The code for 8-bit processing also allocates a variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="57a9b-116">Le stockage de cette valeur permet de tester facilement si le pointeur de la mémoire tampon de délai mobile a atteint la fin de la mémoire tampon de délai.</span><span class="sxs-lookup"><span data-stu-id="57a9b-116">Storing this value makes it easy to test whether the movable delay buffer pointer has reached the end of the delay buffer.</span></span> <span data-ttu-id="57a9b-117">L’exemple de code suivant calcule la valeur :</span><span class="sxs-lookup"><span data-stu-id="57a9b-117">The following example code calculates the value:</span></span>


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a><span data-ttu-id="57a9b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57a9b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57a9b-119">**Implémentation de CEcho ::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="57a9b-119">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




