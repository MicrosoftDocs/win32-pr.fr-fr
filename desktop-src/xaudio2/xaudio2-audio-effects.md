---
description: Un effet audio est un objet qui utilise des données audio entrantes et effectue une opération sur les données avant de les transmettre. Vous pouvez utiliser un effet pour effectuer diverses tâches, notamment ajouter un verbe à un flux audio et surveiller les niveaux de volume des pics.
ms.assetid: 8c3fa4ca-dcff-bd23-7220-7d0aeb6c6068
title: Effets audio XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8de87a65ea4321b5e8d73a837f79a3e56e8e3a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544698"
---
# <a name="xaudio2-audio-effects"></a>Effets audio XAudio2

Un effet audio est un objet qui utilise des données audio entrantes et effectue une opération sur les données avant de les transmettre. Vous pouvez utiliser un effet pour effectuer diverses tâches, notamment ajouter un verbe à un flux audio et surveiller les niveaux de volume des pics.

## <a name="effect-chains"></a>Chaînes d’effet

Toute voix XAudio2 peut héberger une chaîne d’effets audio. Vous pouvez utiliser un tableau de structures de [**\_ \_ descripteur d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) pour spécifier des chaînes d’effet. Chaque descripteur contient un pointeur vers un objet Effect fourni par le client. Ces objets doivent implémenter les interfaces d’objet de traitement audio (APO). Pour plus d’informations sur le modèle APO, consultez la [vue d’ensemble de XAPO](xapo-overview.md) .

Les chaînes d’effet peuvent être modifiées de façon dynamique par le client (pendant que le moteur XAudio2 est en cours d’exécution), les effets peuvent être activés ou désactivés individuellement, et les paramètres d’effet peuvent être modifiés, le tout sans aucune interruption de l’audio. Chaque fois qu’un aspect du graphique d’effet change, XAudio2 optimise le graphique pour éviter tout traitement inutile. Consultez [**IXAudio2Voice :: SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), [**IXAudio2Voice :: EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)et [**IXAudio2Voice :: SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters).

Une fois qu’un effet est attaché à une voix XAudio2, XAudio2 prend le contrôle de l’effet et le client ne doit pas effectuer d’autres appels à celui-ci. Le moyen le plus simple de s’en assurer consiste à libérer tous les pointeurs vers l’effet.

Les effets de la chaîne d’effet d’une voix XAudio2 donnée doivent consommer et produire un audio à virgule flottante au taux d’échantillonnage de traitement de cette voix. Le seul aspect du format audio qu’il peut modifier est le nombre de canaux (par exemple, un effet de réverbération peut convertir les données mono vers 5,1). Le client peut utiliser le [**\_ \_ descripteur d’effet XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor).**Champ OutputChannels** pour spécifier le nombre de canaux que chaque effet doit produire. La chaîne d’effet échoue si l’un des effets ne peut pas répondre à ces exigences, ou si un effet produit un nombre de canaux que l’effet suivant ne peut pas gérer. Tous les appels [**IXAudio2Voice :: EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) ou [**IXAudio2Voice ::D isableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) qui empêchent la chaîne d’effet d’arrêter de répondre à ces exigences échoueront.

Les interfaces APO utilisées dans XAudio2 doivent être *destructrices*. Cela signifie qu’ils remplacent toujours toutes les données qu’ils trouvent dans leurs mémoires tampons de sortie. Dans le cas contraire, l’audio résultant peut être incorrect, car XAudio2 ne garantit pas que ces mémoires tampons ont été précédemment initialisées avec le silence.

## <a name="xaudio2-built-in-effects"></a>Effets intégrés XAudio2

Le tableau suivant répertorie l’ensemble des effets audio intégrés fournis par XAudio2 et leurs méthodes de création. 

| Résultat       | Méthode de création                                              |
|--------------|--------------------------------------------------------------|
| Réverbération       | [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)           |
| Compteur de volume | [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) |



 

Pour obtenir un exemple de création et d’utilisation d’une instance d’un effet audio, consultez [How to : Create a Effect Chain](how-to--create-an-effect-chain.md).

## <a name="custom-effects-in-xaudio2"></a>Effets personnalisés dans XAudio2

L’API [XAPO](xapo-overview.md) fournit une infrastructure pour créer des effets audio personnalisés que vous pouvez utiliser dans XAudio2. Pour obtenir un exemple de création d’un effet personnalisé avec XAPO, consultez [Comment : créer un XAPO](how-to--create-an-xapo.md).

## <a name="xapo-effect-library-xapofx"></a>Bibliothèque d’effets XAPO (XAPOFX)

[XAPOFX](xapofx-overview.md) fournit une bibliothèque supplémentaire de XAPOs et d’un mécanisme commun pour les créer. Pour obtenir un exemple d’utilisation de XAPOFX avec XAudio2, consultez [Comment : utiliser XAPOFX dans XAudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets audio](audio-effects.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> </dl>

 

 
