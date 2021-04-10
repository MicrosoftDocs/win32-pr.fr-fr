---
description: Configuration minimale requise pour DMO
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Configuration minimale requise pour DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950243"
---
# <a name="dmo-minimum-requirements"></a>Configuration minimale requise pour DMO

Chaque DMO doit respecter la configuration minimale suivante :

-   Il doit prendre en charge l’agrégation.
-   Elle doit exposer l’interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .
-   Le modèle de thread doit être’both'. DMOs doit fonctionner correctement dans un environnement à threads libres.

L’effet audio DMOs doit prendre en charge l’interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) , pour une utilisation dans DirectMusic et DirectSound.

Les interfaces suivantes sont documentées ailleurs, mais sont utiles pour de nombreux DMOs. Toutefois, elles ne sont pas requises.

-   **ISpecifyPropertyPages**, **IPropertyPage**: ces interfaces permettent à DMO de fournir une page de propriétés, pour permettre à l’utilisateur de définir des propriétés.
-   **IPersistStream**: cette interface permet à DMO d’enregistrer son état dans un stockage persistant.
-   [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): ces interfaces permettent à un client de configurer les paramètres de compression et de format de sortie d’un encodeur. (Ces deux interfaces font partie de l’API DirectShow, mais elles sont également recommandées pour DMOs.)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



