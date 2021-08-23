---
title: Variables pour gérer la mémoire tampon de délai
description: Variables pour gérer la mémoire tampon de délai
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- plug-ins Lecteur Windows Media, ressources de streaming d’exemples Echo
- plug-ins, exemples de ressources de streaming
- plug-ins de traitement de signal numérique, exemples de ressources de streaming d’écho
- Plug-ins DSP, exemples de ressources de streaming
- Echo DSP, exemple de plug-in, ressources de streaming
- Echo DSP, exemple de plug-in, tampon de délai
- mémoire tampon de délai
- mémoires tampons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be71bc7f2ded34dcd5f29bc10ce01796b6498d36a9a194a48b0bfdec0e14662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571739"
---
# <a name="variables-to-manage-the-delay-buffer"></a>Variables pour gérer la mémoire tampon de délai

Vous devez ajouter les déclarations pour les variables membres dont vous avez besoin pour gérer la mémoire tampon de délai. Ajoutez les déclarations suivantes à ECHO. h dans la section « private » :


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



Ajoutez le code suivant au constructeur CEcho pour initialiser les variables de mémoire tampon de délai :


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des ressources de streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




