---
description: Recherche de types de sortie d’encodeur audio
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Recherche de types de sortie d’encodeur audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541179"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a>Recherche de types de sortie d’encodeur audio (Microsoft Media Foundation)

Étant donné que vous devez utiliser un format de sortie d’encodeur audio qui est énuméré par l’encodeur audio, vous devez disposer d’un moyen de rechercher le format le plus adapté à vos besoins. Le nombre de canaux, le nombre de bits par échantillon et le taux d’échantillonnage de la sortie que vous choisissez doivent correspondre aux valeurs du contenu que vous compressez. Toutefois, l’encodeur peut prendre en charge plusieurs types au sein de ces contraintes.

Le facteur de décision pour le choix d’un type est la vitesse de transmission du flux encodé. vous souhaitez trouver un type de média qui correspond à votre entrée et a une vitesse de transmission aussi proche que possible d’une valeur cible. Si vous énumérez des types de sortie VBR à un passage, il s’agit de la valeur de qualité qui détermine le type que vous utilisez. Pour plus d’informations sur les valeurs de qualité dans les types de sortie énumérés, consultez [énumération des types audio pour des modes d’encodage spécifiques](enumeratingaudiotypesforspecificencodingmodes.md).

> [!Note]  
>    L’encodeur audio énumère certains types qui sont des doublons d’autres types de presque toutes les façons. Ces doublons existent pour les formats dans lesquels le nombre de paquets par seconde ne correspond pas à la configuration requise pour le stockage dans les fichiers ASF lors de la synchronisation avec la vidéo. L’audio synchronisé avec la vidéo dans un fichier ASF doit avoir au moins 3 paquets par seconde pour les vitesses de transmission inférieures à 32000, et 5 paquets ou plus par seconde pour les vitesses de bits supérieures ou égales à 32000.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’encodage audio](configuringaudioencoding.md)
</dt> <dt>

[Énumération des types audio pour des modes d’encodage spécifiques](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



