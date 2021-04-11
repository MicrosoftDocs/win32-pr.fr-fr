---
description: Configuration de l’encodage audio
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Configuration de l’encodage audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201172"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a>Configuration de l’encodage audio (Microsoft Media Foundation)

L’encodeur Windows Media Audio énumère tous les types de sortie pris en charge dans leur forme complète. Récupérez le type souhaité en appelant **IMediaObject :: GetOutputType** ou **IMFTransform :: GetAvailableOutputType**, puis définissez le type récupéré, non modifié, comme type de sortie en appelant **IMediaObject :: SetOutputType** ou **IMFTransform :: SetOutputType**.

Les types de supports de sortie pris en charge par les propriétés changer d’encodeur audio sont configurés. Vous devez configurer toutes les propriétés d’encodeur que vous souhaitez utiliser avant d’énumérer le type de sortie.

Les modes deux-passe et VBR sont pris en charge par les encodeurs audio, mais ils sont configurés différemment de pour la vidéo. Pour plus d’informations, consultez [énumération des types audio pour des modes d’encodage spécifiques](enumeratingaudiotypesforspecificencodingmodes.md).

Les types d’entrée pris en charge par l’encodeur audio ne sont pas disponibles tant que vous n’avez pas défini le type de sortie. Si vous appelez **IMediaObject :: GetInputType** ou **IMFTransform :: GetInputType** avant de définir un type de sortie, la méthode retourne DMO \_ e \_ n’a plus d' \_ \_ éléments ni de MFT \_ e plus de types, \_ \_ \_ respectivement. Une fois que le type de sortie est défini, l’encodeur énumère les types d’entrée qu’il prend en charge pour le type de sortie sélectionné.

Aucun rééchantillonnage audio n’est effectué par l’encodeur Windows Media Audio. Cela signifie que le type de sortie de l’encodeur et le type d’entrée de l’encodeur doivent avoir le même nombre de canaux, le nombre de bits par échantillon et le taux d’échantillonnage. Pour plus d’informations, consultez [recherche de types de sortie d’encodeur audio](findingaudioencoderoutputtypes.md).

> [!Note]  
>    Chaque type de sortie énuméré par l’encodeur audio contient une structure **WAVEFORMATEX** (pointée par **am \_ Media \_ type. pbFormat**) avec les données étendues qui lui sont ajoutées. La taille des données étendues est spécifiée par **WAVEFORMATEX. cbSize**. Ces données doivent être conservées avec le contenu encodé afin qu’elles puissent être remises au décodeur. Impossible de décompresser le contenu sans les données de format étendu.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’audio](workingwithaudio.md)
</dt> </dl>

 

 



