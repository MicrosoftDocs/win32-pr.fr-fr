---
title: Rééchantillonnage audio
description: Rééchantillonnage audio
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows Media Format SDK, rééchantillonnage audio
- Windows Media Format SDK, rééchantillonnage de l’audio
- ASF (Advanced Systems Format), rééchantillonnage audio
- ASF (format des systèmes avancés), rééchantillonnage audio
- ASF (Advanced Systems Format), rééchantillonnage de l’audio
- ASF (format des systèmes avancés), rééchantillonnage de l’audio
- rééchantillonnage audio
- rééchantillonnage de l’audio, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5d95ed50117ac9d0fe7d71a2148314e1b9faf3ba8a26b99bb69083029b991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434473"
---
# <a name="audio-resampling"></a>Rééchantillonnage audio

Chaque format compressé d’un codec audio a un taux d’échantillonnage et une taille d’échantillon spécifiques. Ils n’ont pas besoin de correspondre aux paramètres du format d’entrée ou du format de sortie. Si un format d’entrée a des paramètres différents de ceux du format compressé décrit dans le profil, le writer rééchantillonnera l’audio, pendant le processus d’encodage, pour qu’il corresponde au format compressé. Seuls certains formats sont acceptés par le writer comme entrée. Lorsque vous énumérez les formats d’entrée pour un flux audio compressé, tous les formats récupérés peuvent être rééchantillonnés pour correspondre au format du profil.

Lors de la lecture de l’audio compressé, le lecteur rééchantillonnera le contenu pour qu’il corresponde au format de sortie. Vous devez utiliser l’un des formats de sortie énumérés par le lecteur, afin de garantir que l’audio peut être rééchantillonné aux paramètres de format de sortie.

Chaque rééchantillonnage peut affecter la qualité du son. Lorsque cela est possible, vous devez utiliser des formats d’entrée et de sortie avec des paramètres qui correspondent au format compressé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités d’écriture de fichier**](file-writing-features.md)
</dt> <dt>

[**Utilisation des entrées**](working-with-inputs.md)
</dt> <dt>

[**Utilisation des sorties**](working-with-outputs.md)
</dt> </dl>

 

 




