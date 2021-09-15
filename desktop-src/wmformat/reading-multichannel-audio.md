---
title: Lecture de l’audio multicanal
description: Lecture de l’audio multicanal
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Media Format SDK, lecture audio multicanal
- ASF (Advanced Systems Format), lecture audio multicanal
- ASF (format des systèmes avancés), lire l’audio multicanal
- ASF (Advanced Systems Format), audio multicanal
- ASF (format de systèmes avancés), audio multicanal
- codecs, lecture de l’audio multicanal
- audio multicanal, lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404648"
---
# <a name="reading-multichannel-audio"></a>Lecture de l’audio multicanal

le codec Windows Media Audio 9 Professional peut encoder l’Audio multicanal (plus de deux canaux). Lors de la lecture d’un fichier à l’aide de l’audio multicanal, vous devez configurer la sortie correctement ou l’audio sera remis à une qualité inférieure et en stéréo. Pour définir une sortie pour la remise audio multicanal, vous devez définir deux paramètres de sortie : g \_ wszEnableDiscreteOutput et g \_ wszSpeakerConfig.

Le paramètre g \_ wszEnableDiscreteOutput sur **true** définit le codec pour fournir une sortie audio haute définition. le son haute définition est encodé par le codec Windows Media Audio 9 avec des échantillons de 24 bits en stéréo ou plusieurs canaux. Si ce paramètre a la **valeur false**, seule une sortie stéréo de 16 bits sera remise.

Le nombre de haut-parleurs sur l’ordinateur de jeu est défini avec g \_ wszSpeakerConfig. Ce paramètre est une valeur **DWORD** définie sur l’une des constantes de haut-parleur DirectSound indiquées dans le tableau suivant. Pour résoudre ces noms de constantes pour votre compilateur, vous devez inclure dsound. h.



| Constante             | Valeur      | Description                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ DIRECTOUT | 0x00000000 | L’audio est transmis directement, sans être configuré pour les intervenants. |
| \_casque DSSPEAKER | 0x00000001 | L’ordinateur client est équipé d’un casque.                             |
| \_mono DSSPEAKER      | 0x00000002 | L’ordinateur client est équipé d’un orateur mono.                     |
| DSSPEAKER \_ Quad      | 0x00000003 | L’ordinateur client est équipé de haut-parleurs Quadraphonic.                  |
| \_stéréo DSSPEAKER    | 0x00000004 | L’ordinateur client est équipé de haut-parleurs stéréo.                        |
| DSSPEAKER \_ surround  | 0x00000005 | L’ordinateur client est équipé de haut-parleurs Surround audio à quatre canaux.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | L’ordinateur client est équipé de cinq enceintes et d’un caisson de basses.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | L’ordinateur client est équipé de sept haut-parleurs et d’un caisson de basses.         |



 

Pour définir ces paramètres, utilisez [**IWMReaderAdvanced2 :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).

Enfin, pour que les canaux s’affichent discrètement, sans pli vers le stéréo, vous devez définir le type de support approprié sur la sortie en procédant comme suit :

1.  Appelez [**IWMReader :: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) pour obtenir le nombre de formats pris en charge pour la sortie audio appropriée. Les index de format de sortie sont de base zéro.
2.  Pour chaque format pris en charge, appelez [**IWMReader :: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) pour récupérer l’interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) sur l’objet Propriétés du média de sortie.
3.  Appelez [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) pour récupérer le type de média.
4.  Si le type de média récupéré est le type Multichannel souhaité, définissez-le en appelant [**IWMReader :: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).

Une fois que vous avez défini une sortie discrète et la configuration de l’orateur, les formats de sortie énumérés par le lecteur doivent inclure des formats multicanaux qui utilisent la structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) . Si vous énumérez les formats de sortie avant de définir les propriétés, seuls les formats avec 1 ou 2 canaux et un maximum de 16 bits par canal seront inclus. Comme pour les autres formats audio, vous devez utiliser uniquement les formats énumérés par le lecteur. ne configurez pas votre propre.

> [!Note]  
> vous pouvez générer l’audio multicanal uniquement si votre application s’exécute sur microsoft Windows XP ou une version ultérieure de microsoft Windows.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**entrées, Flux et sorties**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> <dt>

[**Paramètres de sortie**](output-settings.md)
</dt> <dt>

[**Utilisation d' High-Resolution audio PCM**](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 