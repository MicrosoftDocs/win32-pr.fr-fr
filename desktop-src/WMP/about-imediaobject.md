---
title: À propos de IMediaObject
description: À propos de IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Plug-ins du lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
- Plug-ins du lecteur Windows Media, interface IMediaObject
- plug-ins, interface IMediaObject
- plug-ins de traitement de signal numérique, interface IMediaObject
- Plug-ins DSP, interface IMediaObject
- Interface IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671565"
---
# <a name="about-imediaobject"></a>À propos de IMediaObject

L’interface **IMediaObject** est l’interface requise pour DMOs. **IMediaObject** contient les méthodes qu’un plug-in Windows Media Player utilise pour obtenir des données à partir du lecteur Windows Media, pour traiter les données et pour retourner les données traitées au lecteur Windows Media. Pour obtenir la documentation complète de l’interface **IMediaObject** , consultez la section DirectShow de la SDK Windows.

Les méthodes de **IMediaObject** peuvent être classées comme suit :

## <a name="methods-that-handle-format-negotiation"></a>Méthodes qui gèrent la négociation de format

Il s’agit des méthodes appelées par le lecteur Windows Media pour obtenir des informations sur les formats de données pris en charge par le plug-in. Ces méthodes incluent les tâches suivantes :

-   **GetInputMaxLatency**
-   **GetInputSizeInfo**
-   **GetInputStreamInfo**
-   **GetInputType**
-   **GetOutputSizeInfo**
-   **GetOutputStreamInfo**
-   **GetOutputType**
-   **GetStreamCount**
-   **SetInputMaxLatency**
-   **SetInputType**
-   **SetOutputType**

Plusieurs de ces méthodes, telles que **GetInputType** et **SetInputType**, utilisent la structure de **\_ \_ type de média DMO** pour décrire le format des données utilisées par un flux. Lorsque le lecteur Windows Media appelle ces méthodes, il fournit un pointeur vers une structure de **\_ \_ type de média DMO** . Si une méthode telle que **SetInputType** spécifie les informations sur le type de média, le plug-in doit copier la structure de **\_ \_ type de média DMO** sur une variable membre et inspecter ses membres de données pour déterminer le type de données que le lecteur Windows Media fournira dans la mémoire tampon d’entrée. Si une méthode telle que **GetInputType** récupère les informations sur le type de média, le plug-in doit copier l’adresse de la variable membre contenant la structure de **\_ \_ type de média DMO** vers le pointeur fourni par le lecteur Windows Media dans la liste de paramètres.

Le lecteur Windows Media utilise principalement deux membres de la structure de **\_ \_ type de média DMO** :

-   **MajorType**: identificateur global unique (Guid) qui spécifie la catégorie globale des médias, tels que l’audio ou la vidéo.
-   **SubType**: GUID qui spécifie une description plus détaillée du média, telle que l’audio PCM.

Ces GUID se trouvent dans l’en-tête nommé UUID. h, qui est inclus avec le SDK Windows.

Des méthodes telles que **GetInputSizeInfo** fournissent des informations au lecteur Windows Media quant à la quantité de mémoire requise pour allouer les tampons de traitement. Les méthodes telles que **GetStreamCount** et **GetOutputStreamInfo** fournissent des informations au lecteur Windows Media sur le nombre et le caractère des flux pris en charge par le plug-in DSP.

**GetInputMaxLatency** et **SetInputMaxLatency** sont implémentés par DMOs dans des cas spéciaux. Les plug-ins du lecteur Windows Media DSP doivent retourner E \_ NOTIMPL.

## <a name="methods-that-specify-or-retrieve-state-information"></a>Méthodes qui spécifient ou récupèrent les informations d’État

Il s’agit des méthodes que le lecteur Windows Media appelle pour récupérer ou définir les valeurs relatives à l’état actuel du plug-in. Ces méthodes incluent les tâches suivantes :

-   **GetInputCurrentType**
-   **GetInputStatus**
-   **GetOutputCurrentType**

**GetInputCurrentType** et **GetOutputCurrentType** utilisent la structure de **\_ \_ type de média DMO** pour retourner au lecteur Windows Media des informations sur les types de médias précédemment définis pour les flux d’entrée et de sortie. **GetInputStatus** retourne un indicateur qui indique à Windows Media Player si le plug-in DSP peut accepter des données d’entrée.

## <a name="methods-that-handle-buffering-and-processing-data"></a>Méthodes qui gèrent la mise en mémoire tampon et le traitement des données

Il s’agit des méthodes que le lecteur Windows Media appelle pour initier les différents processus que le plug-in effectue pour effectuer le traitement du signal numérique. Ces méthodes incluent les tâches suivantes :

-   **AllocateStreamingResources**
-   **Discontinuité**
-   **Purge**
-   **FreeStreamingResources**
-   **Verrou**
-   **ProcessInput**
-   **ProcessOutput**

Le lecteur Windows Media appelle **AllocateStreamingResources** et **FreeStreamingResources** pour fournir au plug-in DSP la possibilité de configurer ou de libérer des tampons supplémentaires que le plug-in peut nécessiter pour le traitement interne.

Les plug-ins du lecteur Windows Media DSP n’ont pas besoin d’utiliser la méthode de **discontinuisation** DMO.

Le lecteur Windows Media appelle **flush** pour demander au plug-in DSP de vider toutes les données mises en mémoire tampon. Le plug-in doit libérer toutes les références aux interfaces **IMediaBuffer** , effacer toutes les valeurs qui spécifient l’horodatage ou l’exemple de longueur pour la mémoire tampon du média, et réinitialiser tous les États internes qui dépendent du contenu de l’exemple de support.

Le lecteur Windows Media appelle ProcessInput pour passer un pointeur vers une interface **IMediaBuffer** vers le plug-in DSP. Cette interface fournit l’accès à la mémoire tampon d’entrée allouée par le lecteur Windows Media pour fournir des données au plug-in. Le lecteur Windows Media appelle ensuite **ProcessOutput** pour passer un pointeur vers une interface **IMediaBuffer** qui fournit l’accès à la mémoire tampon de sortie allouée par le lecteur Windows Media pour recevoir les données traitées du plug-in DSP.

L’interface **IMediaObject** comprend une méthode nommée **Lock**. Cette méthode est conçue pour acquérir ou libérer un verrou sur DMO afin de conserver la méthode DMO sérialisée lors de l’exécution de plusieurs opérations. La version de **IMediaObject :: Lock** dans le code de l’Assistant remplace l’implémentation ATL de **Lock**. Étant donné que le lecteur Windows Media sérialise les appels passés à l’interface DMO d’un plug-in DSP, l’implémentation de **Lock** retourne simplement S \_ OK. Pour plus d’informations sur la création d’un multithread DMO, reportez-vous à la section DirectShow de l’SDK Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interfaces requises**](required-interfaces.md)
</dt> </dl>

 

 




