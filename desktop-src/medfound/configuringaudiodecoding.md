---
description: Configuration du décodage audio
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Configuration du décodage audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee274fd714065a1c89c9d634dd80de4d59c9eb567d67ed8045d2b89bece87d74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664642"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a>Configuration du décodage audio (Microsoft Media Foundation)

le décodage de contenu Windows Media Audio est beaucoup plus facile que son encodage. Après avoir créé un objet décodeur audio, définissez le type d’entrée à l’aide de la méthode **IMediaObject :: SetInputType** ou **IMFTransform :: SetInputType** . Le type de média que vous utilisez pour l’entrée du décodeur doit correspondre au type de sortie qui a été utilisé lors de l’encodage du contenu. Cela comprend les données de format étendu ajoutées à la structure **WAVEFORMATEX** . Vous devez vous assurer que ces données sont correctes, car le décodeur ne peut pas traiter les exemples sans celui-ci.

Après avoir défini le type d’entrée, vous pouvez configurer les fonctionnalités de décodeur que vous souhaitez utiliser. Les fonctionnalités de décodeur, comme celles utilisées pour l’encodage, sont définies à l’aide des méthodes de **IPropertyBag** ou **IPropertyStore**.

Une fois que le type d’entrée est défini et que toutes les fonctionnalités du décodeur sont configurées, vous pouvez énumérer les types de sortie pris en charge par le décodeur en effectuant des appels à **IMediaObject :: GetOutputType** ou **IMFTransform :: GetOutputType**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’audio](workingwithaudio.md)
</dt> </dl>

 

 



