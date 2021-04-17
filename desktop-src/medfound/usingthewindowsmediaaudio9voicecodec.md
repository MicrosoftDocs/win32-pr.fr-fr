---
description: Utilisation du codec Windows Media Audio Voice
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Utilisation du codec Windows Media Audio Voice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530466"
---
# <a name="using-the-windows-media-audio-voice-codec"></a>Utilisation du codec Windows Media Audio Voice

Le codec Windows Media Audio Voice offre une compression à vitesse de transmission faible et optimisée pour le son contenant de la parole. La capacité du codec à produire de tels petits exemples est due à la plage de fréquences limitée des sons de la voix humaine. Cette optimisation signifie qu’un encodeur vocal dédié crée une sortie de qualité médiocre pour le contenu qui contient des sons plus compliqués, tels que la musique. Toutefois, le codec Windows Media Audio Voice compense ce problème de qualité potentiel en fournissant des modes distincts pour la voix, la musique et le contenu mixte. Le codec analyse le contenu mixte pour déterminer le mode à utiliser pour chaque partie du fichier.

Le codec Windows Media Audio Voice est implémenté dans l’objet encodeur identifié par l’identificateur de classe CLSID \_ CWMSPEncMediaObject2, et dans l’objet décodeur identifié par l’identificateur de classe CLSID \_ CWMSPDecMediaObject. La balise de format des types de média utilisant ce codec est 0x00A.

## <a name="configuring-the-encoder"></a>Configuration de l’encodeur

L’encodeur vocal prend en charge trois modes : la reconnaissance vocale, la musique et la combinaison. Chaque mode est optimisé pour obtenir les meilleurs résultats pour ce type de contenu. Vous pouvez configurer le mode de l’encodeur vocal à l’aide des méthodes de **IPropertyStore** pour définir la propriété [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) .

Lorsqu’il est configuré pour du contenu mixte, le codec Windows Media Audio Voice détecte automatiquement les passages de musique dans le contenu. Si vous n’êtes pas satisfait des résultats, vous pouvez spécifier l’emplacement de musique dans le contenu à l’aide d’une liste de décisions de modification (EDL). Pour plus d’informations, consultez [utilisation d’une liste de décisions de modification pour l’encodage vocal](usingavoiceeditingdecisionlist.md).

Contrairement aux autres encodeurs audio, vous pouvez définir la valeur de la fenêtre de mémoire tampon pour le contenu vocal à l’aide de la propriété [MFPKEY \_ WMAVOICE \_ enc \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) . Toutefois, les valeurs par défaut devraient fonctionner correctement dans la plupart des cas.

> [!Note]  
>    Lors de la configuration de l’encodeur vocal, il est très important de définir le type de sortie avant de définir le type d’entrée. Il s’agit de l’ordre d’opérations recommandé pour tous les codecs audio, mais l’encodeur vocal peut signaler des types de sortie erronés si une entrée est définie lorsque vous appelez **IMediaObject :: GetOutputType** ou **IMFTransform :: GetOutputType**.

 

## <a name="decoding"></a>Décodage

Il n’existe aucune exigence particulière pour décoder l’audio vocal. Pour plus d’informations, consultez [configuration du décodage audio](configuringaudiodecoding.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’audio](workingwithaudio.md)
</dt> </dl>

 

 



