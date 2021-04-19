---
title: XAudio2, fonctions
description: Cette section contient des informations sur les fonctions fournies par l’API Microsoft XAudio2.
ms.assetid: 870a0425-3226-7848-bcc0-0ba7145135cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd8bcfdb00565d6f8bbc31ae0ee6a24f106dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530083"
---
# <a name="xaudio2-functions"></a>XAudio2, fonctions

Cette section contient des informations sur les fonctions fournies par l’API Microsoft XAudio2.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                       | Description                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx)<br/>                                                                     | Crée une instance de l’effet [XAPOFX](xapofx-overview.md) demandé.<br/>                                                                                                                                                         |
| [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo)<br/>                                                           | Crée une instance de l’interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) pour le traitement de la fonction de transfert liée aux têtes (HRTF).<br/>                                                                                                                  |
| [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)<br/>                                 | Fonction inline qui convertit les paramètres I3DL2 (Interactive 3D audio Rendering Guidelines niveau 2,0) en paramètres XAudio2 natifs.<br/>                                                                                                 |
| [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)<br/>                                                   | Calcule les paramètres DSP en ce qui concerne les paramètres 3D.<br/>                                                                                                                                                                             |
| [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)<br/>                                                 | Définit toutes les constantes audio 3D globales.<br/>                                                                                                                                                                                                |
| [**XAudio2AmplitudeRatioToDecibels**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2amplituderatiotodecibels)<br/>                       | Fonction inline qui convertit une valeur de rapport d’amplitude en valeur décibel.<br/>                                                                                                                                                         |
| [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)<br/>                                                           | Crée un nouvel objet **XAudio2** et retourne un pointeur vers son interface [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .<br/>                                                                                                                              |
| [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)<br/>                                               | Crée un nouvel objet de traitement audio de réverbération (APO) et retourne un pointeur vers celui-ci.<br/>                                                                                                                                                   |
| [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter)<br/>                                     | Crée un objet de traitement audio de compteur de volume (APO) et retourne un pointeur vers celui-ci.<br/>                                                                                                                                              |
| [**XAudio2CutoffFrequencyToOnePoleCoefficient**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoonepolecoefficient)<br/> | Fonction inline qui convertit les fréquences de coupure de filtre exprimées en Hertz en les coefficients de filtre utilisés avec le membre **Frequency** de la structure de [**\_ \_ paramètres de filtre XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) .<br/>   |
| [**XAudio2CutoffFrequencyToRadians**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2cutofffrequencytoradians)<br/>                       | Fonction inline qui convertit les fréquences de coupure de filtre exprimées en Hertz en valeurs de fréquence en radians utilisées dans le membre **Frequency** de la structure de [**\_ \_ paramètres de filtre XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) .<br/> |
| [**XAudio2DecibelsToAmplitudeRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2decibelstoamplituderatio)<br/>                       | Fonction inline qui convertit une valeur décibel en valeur de rapport d’amplitude.<br/>                                                                                                                                                         |
| [**XAudio2FrequencyRatioToSemitones**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2frequencyratiotosemitones)<br/>                     | Fonction inline qui convertit une valeur de rapport de fréquence en valeur en demi-tons.<br/>                                                                                                                                                         |
| [**XAudio2RadiansToCutoffFrequency**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2radianstocutofffrequency)<br/>                       | Fonction inline qui convertit les fréquences en radians utilisées dans les [**\_ \_ paramètres de filtre XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters) en fréquences absolues en Hertz.<br/>                                                          |
| [**XAudio2SemitonesToFrequencyRatio**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2semitonestofrequencyratio)<br/>                     | Fonction inline qui convertit une valeur de demi-tons en valeur de rapport de fréquence.<br/>                                                                                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[XAudio2 : référence rogramming :P](programming-reference.md)
</dt> </dl>

 

 




