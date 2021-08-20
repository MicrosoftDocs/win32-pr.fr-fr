---
title: Pour gérer la latence de l’enregistreur
description: Pour gérer la latence de l’enregistreur
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- ASF (Advanced Systems Format), gestion de la latence de l’enregistreur
- ASF (format de systèmes avancés), gestion de la latence de l’enregistreur
- ASF (Advanced Systems Format), latence de l’enregistreur
- ASF (format de systèmes avancés), latence de l’enregistreur
- latence de l’enregistreur
- latence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0adb18814cc8153ae81ed9517834d62345f18b61f51de6aacd38e9028699331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845479"
---
# <a name="to-manage-writer-latency"></a>Pour gérer la latence de l’enregistreur

Il faut du temps pour que l’enregistreur traite les exemples. La durée entre le passage d’un exemple d’entrée et l’écriture d’un échantillon de sortie est appelée la latence du writer. Un certain nombre de facteurs contribuent à la latence de l’enregistreur et vous pouvez le réduire de plusieurs façons.

Le facteur le plus évident impliqué dans la latence du writer est le temps nécessaire pour compresser un exemple. Dans la plupart des cas, vous n’aurez que peu ou pas de contrôle sur cela. Si la bande passante n’est pas une préoccupation majeure, vous pouvez réduire la latence en utilisant moins de compression. Bien sûr, vous pouvez obtenir la latence la plus faible en passant des exemples qui sont déjà compressés.

Le facteur suivant, et celui sur lequel vous avez généralement le contrôle, est l’ordre dans lequel les exemples sont passés au lecteur. Vous pouvez obtenir une meilleure latence en passant des échantillons dans l’ordre de l’heure de présentation et en vous assurant que les échantillons d’entrée sont bien synchronisés entre tous les flux d’entrée. Plus la différence de temps de présentation entre les exemples de flux différents est importante, plus la latence sera élevée. Vous pouvez définir un maximum pour l’écart entre les exemples d’entrée en appelant [**IWMWriterAdvanced :: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




