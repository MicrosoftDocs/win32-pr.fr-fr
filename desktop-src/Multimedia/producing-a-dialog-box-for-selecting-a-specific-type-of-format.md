---
title: Génération d’une boîte de dialogue pour la sélection d’un type de format spécifique
description: Génération d’une boîte de dialogue pour la sélection d’un type de format spécifique
ms.assetid: e454f9d6-5cbf-4e1b-937e-771cf1dd38ba
keywords:
- Gestionnaire de compression audio (ACM), génération de boîtes de dialogue
- ACM (gestionnaire de compression audio), génération de boîtes de dialogue
- Exemples ACM, génération de boîtes de dialogue
- génération de boîtes de dialogue
- acmFormatChoose fonction)
- Gestionnaire de compression audio (ACM), sélection des types de format
- ACM (gestionnaire de compression audio), sélection des types de format
- Exemples ACM, sélection des types de format
- sélection des types de format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfc5d73d1b03f22923e6001d65898c05e2bd853e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364067"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a>Génération d’une boîte de dialogue pour la sélection d’un type de format spécifique

Vous pouvez souhaiter qu’une application autorise l’utilisateur à sélectionner un format dans une liste restreinte de formats dans une boîte de dialogue. Les restrictions peuvent limiter le nombre de canaux, le taux d’échantillonnage, la balise de format audio Waveform ou le nombre de bits par échantillon. Dans tous ces cas, vous pouvez générer la liste à l’aide de la fonction [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , en définissant les membres **fdwEnum** et **pwfxEnum** de la structure [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) . L'exemple suivant illustre ce processus.


```C++
MMRESULT            mmr; 
ACMFORMATCHOOSE     afc; 
WAVEFORMATEX        wfxSelection; 
WAVEFORMATEX        wfxEnum; 
 
// Initialize the ACMFORMATCHOOSE members. 
memset(&afc, 0, sizeof(afc)); 
 
afc.cbStruct    = sizeof(afc); 
afc.fdwStyle    = 0L;               // no special style flags 
afc.hwndOwner   = hwnd;             // hwnd of parent window 
afc.pwfx        = &wfxSelection;    // wfx to receive selection 
afc.cbwfx       = sizeof(wfxSelection); 
afc.pszTitle    = TEXT("16 Bit PCM Selection"); 
 
//  Request that all 16-bit PCM formats be displayed for the user 
//  to select from. 
memset(&wfxEnum, 0, sizeof(wfxEnum)); 
wfxEnum.wFormatTag = WAVE_FORMAT_PCM; 
wfxEnum.wBitsPerSample = 16; 
afc.fdwEnum = ACM_FORMATENUMF_WFORMATTAG | 
    ACM_FORMATENUMF_WBITSPERSAMPLE; 
afc.pwfxEnum = &wfxEnum; 
mmr = acmFormatChoose(&afc); 
if ((MMSYSERR_NOERROR != mmr) && (ACMERR_CANCELED != mmr)) 
{ 
    // There was a fatal error in bringing up the list 
    // dialog box (probably invalid input parameters). 
} 
 
```



 

 




