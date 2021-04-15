---
title: Utilisation de la structure WAVEFORMATEX
description: Utilisation de la structure WAVEFORMATEX
ms.assetid: 9b668e1e-cb5f-4065-802b-23974925eacf
keywords:
- Wave audio, structure WAVEFORMATEX
- audio auxiliaire, structure WAVEFORMATEX
- WAVEFORMATEX, structure
- Données audio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1534cf660c2f2423dc526c3d29f8eca06878fc0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463030"
---
# <a name="using-the-waveformatex-structure"></a><span data-ttu-id="ff61b-107">Utilisation de la structure WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="ff61b-107">Using the WAVEFORMATEX Structure</span></span>

<span data-ttu-id="ff61b-108">Pour les données audio PCM sur un maximum de deux canaux et avec des exemples de 8 ou 16 bits, utilisez la structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) pour spécifier le format de données.</span><span class="sxs-lookup"><span data-stu-id="ff61b-108">For PCM audio data on no more than two channels and with 8-bit or 16-bit samples, use the [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to specify the data format.</span></span>

<span data-ttu-id="ff61b-109">L’exemple suivant montre comment configurer une structure **WAVEFORMATEX** pour une chaîne mono 8 bits 11,025 kilohertz (kHz) et pour une chaîne stéréo de 44,1 kHz 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ff61b-109">The following example shows how to set up a **WAVEFORMATEX** structure for 11.025 kilohertz (kHz) 8-bit mono and for 44.1 kHz 16-bit stereo.</span></span> <span data-ttu-id="ff61b-110">Après la configuration de **WAVEFORMATEX**, l’exemple appelle la fonction IsFormatSupported pour vérifier que l’appareil de sortie Waveform PCM prend en charge le format.</span><span class="sxs-lookup"><span data-stu-id="ff61b-110">After setting up **WAVEFORMATEX**, the example calls the IsFormatSupported function to verify that the PCM waveform output device supports the format.</span></span> <span data-ttu-id="ff61b-111">Le code source pour IsFormatSupported est présenté dans un exemple pour [déterminer la prise en charge des formats non standard](determining-nonstandard-format-support.md).</span><span class="sxs-lookup"><span data-stu-id="ff61b-111">The source code for IsFormatSupported is shown in an example in [Determining Nonstandard Format Support](determining-nonstandard-format-support.md).</span></span>


```C++
UINT wReturn; 
WAVEFORMATEX pcmWaveFormat; 
 
// Set up WAVEFORMATEX for 11 kHz 8-bit mono. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 1; 
pcmWaveFormat.nSamplesPerSec = 11025L; 
pcmWaveFormat.nAvgBytesPerSec = 11025L; 
pcmWaveFormat.nBlockAlign = 1; 
pcmWaveFormat.wBitsPerSample = 8; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono is supported.", 
       "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono NOT supported.", 
       "", MB_ICONINFORMATION); 
else 
     MessageBox(hMainWnd, "Error opening waveform device.", 
       "Error", MB_ICONEXCLAMATION); 
 
// Set up WAVEFORMATEX for 44.1 kHz 16-bit stereo. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 2; 
pcmWaveFormat.nSamplesPerSec = 44100L; 
pcmWaveFormat.nAvgBytesPerSec = 176400L; 
pcmWaveFormat.nBlockAlign = 4; 
pcmWaveFormat.wBitsPerSample = 16; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in the system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo is supported.", 
      "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo NOT supported.", 
      "", MB_ICONINFORMATION); 
else 
    MessageBox(hMainWnd, "Error opening waveform device.", 
      "Error", MB_ICONEXCLAMATION); 

```



 

 