---
description: Utilisation de l’audio High-Definition
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Utilisation de l’audio High-Definition (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313646"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a>Utilisation de l’audio High-Definition (Microsoft Media Foundation)

l’audio haute définition, dans le contexte des codecs Windows Media Audio, est tout type audio avec plus de deux canaux ou plus de 16 bits par échantillon. le son haute définition est pris en charge par les catégories Professional et sans perte de l' [encodeur Windows Media Audio](windowsmediaaudioencoder.md).

Les types audio haute définition non compressés sont définis à l’aide de la structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) . **WAVEFORMATEXTENSIBLE** est une extension structurée de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) . lorsque vous utilisez DMOs, le membre **formattype** de la structure [**de \_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) qui décrit un type audio haute définition doit avoir la valeur WMCFORMAT \_ WaveFormatEx, comme c’est le cas pour le son normal ; il n’existe aucun identificateur de format spécial pour **WAVEFORMATEXTENSIBLE**. Si un format utilise **WAVEFORMATEXTENSIBLE** , vous devez définir le membre **cbSize** de la structure **WAVEFORMATEX** sur 22.

Lorsque vous utilisez Media Foundation, vous pouvez construire le type de média approprié à partir d’une structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) à l’aide de la fonction [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).

les types de sortie à plusieurs canaux pris en charge par le codec Windows Media Audio 10 Professional n’utilisent pas [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), mais signalent le nombre correct de canaux et de bits par échantillon dans la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) . comme avec tous les types audio décrivant le contenu Windows Media Audio compressé, des informations supplémentaires sont ajoutées à la structure **WAVEFORMATEX** utilisée par le décodeur pour la décompression.

## <a name="decoding-high-definition-audio"></a>Décodage High-Definition audio

Pour décoder un son haute définition, vous devez définir la propriété [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) sur variant \_ true. Si cette propriété n’est pas définie, le décodeur fournit du contenu stéréo avec un maximum de 16 bits par échantillon, quel que soit le format compressé.

> [!Note]  
> le son haute définition est pris en charge uniquement pour Windows XP, Windows Vista et versions ultérieures. dans les versions antérieures de Windows, Windows Media Audio le contenu encodé à l’aide de la haute définition est rendu sous la forme Audio à deux canaux, avec un maximum de 16 bits par échantillon.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’audio](workingwithaudio.md)
</dt> </dl>

 

 
