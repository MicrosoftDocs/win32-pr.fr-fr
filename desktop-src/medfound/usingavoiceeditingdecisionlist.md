---
description: Utilisation d’une liste de décisions de modification pour l’encodage vocal
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Utilisation d’une liste de décisions de modification pour l’encodage vocal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536136"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a>Utilisation d’une liste de décisions de modification pour l’encodage vocal

Une liste de décisions de modification (EDL) est fournie à un codec qui fournit des informations sur la façon dont des parties spécifiques du contenu doivent être encodées. Le codec vocal Windows Media Audio 9 prend en charge un EDL simple dans lequel vous pouvez spécifier les portions de contenu qui contiennent de la musique. Par défaut, le codec détecte les passages de musique lui-même lorsqu’il est configuré pour encoder du contenu mixte. Vous devez utiliser un EDL uniquement si le codec ne détecte pas correctement les types de contenu.

Pour utiliser un EDL, l’encodeur vocal doit être défini pour encoder le contenu mixte. Configurez le mode du codec vocal sur « mixed » en affectant à la propriété [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) la valeur 2. Définissez l’EDL à l’aide de la propriété [ \_ \_ \_ EDL MFPKEY WMAVOICE enc](mfpkey-wmavoice-enc-edlproperty.md) . La valeur de cette propriété est une chaîne contenant une liste délimitée par des virgules des plages de temps du contenu qui doivent être encodées en musique. Le premier élément de la liste est la version de l’EDL, qui est toujours 1. Le deuxième élément est le nombre de sections de musique décrites dans la liste. Après le deuxième élément, plusieurs paires de valeurs sont égales au deuxième élément ; chaque paire de valeurs décrit le point de départ et le point de fin d’un passage de musique dans le contenu, en millisecondes.

Par exemple, la chaîne EDL « 1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000 » spécifie quatre passages musicaux, chacun d’entre eux étant une seconde longue. Si les informations de la chaîne EDL ne sont pas valides, elles sont ignorées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec vocal Windows Media Audio 9](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Utilisation de l’audio](workingwithaudio.md)
</dt> </dl>

 

 



