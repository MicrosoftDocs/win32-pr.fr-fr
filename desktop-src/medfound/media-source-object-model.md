---
description: Modèle d’objet de source multimédia
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: Modèle d’objet de source multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d95217e881fca1a84b36caa482e0c5cfdff317db5d97d0441387f4ab0c9e4751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877792"
---
# <a name="media-source-object-model"></a>Modèle d’objet de source multimédia

Cette rubrique décrit le modèle d’objet pour les sources multimédias dans Microsoft Media Foundation. Une source multimédia doit implémenter deux objets :

-   Un descripteur de présentation, qui décrit le contenu de la source, y compris le nombre de flux et le format de chaque flux. Pour plus d’informations sur les descripteurs de présentation, consultez [descripteurs de présentation](presentation-descriptors.md).
-   Un ou plusieurs flux de données multimédias, qui génèrent les données sources.

La source ne crée pas les flux avant le démarrage de la lecture.

## <a name="media-source-interfaces"></a>Interfaces sources de média

Une source multimédia doit exposer les interfaces suivantes via **QueryInterface**.



| Interface                                                | Description                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Obligatoire pour toutes les sources multimédias.                                                                                 |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Obligatoire pour toutes les sources multimédias. L’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) hérite de cette interface. |



 

Si vous le souhaitez, une source de média peut implémenter l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) et implémenter l’une des interfaces suivantes en tant que services :



| Interface de service                                  | Description                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | Contrôle la vitesse de lecture.                                       |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | Indique la plage des taux de lecture pris en charge.           |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | Permet au gestionnaire de qualité d’ajuster la qualité audio ou vidéo. |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | Fournit des métadonnées.                                                |



 

Si la source du média peut fonctionner à des vitesses autres que la vitesse normale (1,0), elle doit exposer le service de contrôle de la fréquence ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) et [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)). Dans le cas contraire, il est supposé que la source prend uniquement en charge la lecture à la vitesse normale. Pour plus d’informations, consultez [Implementing Rate Control](implementing-rate-control.md).

Pour plus d’informations sur les interfaces de service et les [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), consultez [interfaces de service](service-interfaces.md).

## <a name="media-stream-interfaces"></a>Interfaces de flux de média

Les flux multimédias doivent implémenter les interfaces suivantes.



| Interface                                                | Description                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | Requis pour tous les flux multimédias.                                                                                 |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Requis pour tous les flux multimédias. L’interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) hérite de cette interface. |



 

Aucune interface de service n’est actuellement définie pour les flux multimédias.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sources multimédias](media-sources.md)
</dt> </dl>

 

 



