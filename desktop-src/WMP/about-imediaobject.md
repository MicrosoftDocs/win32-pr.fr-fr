---
title: À propos de IMediaObject
description: À propos de IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- plug-ins Lecteur Windows Media, interfaces
- plug-ins, interfaces
- plug-ins de traitement de signal numérique, interfaces
- Plug-ins DSP, interfaces
- interfaces, plug-ins DSP
- plug-ins Lecteur Windows Media, interface IMediaObject
- plug-ins, interface IMediaObject
- plug-ins de traitement de signal numérique, interface IMediaObject
- Plug-ins DSP, interface IMediaObject
- Interface IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dbf44a527d61d924045a4bcceded5d90bb174fef608e3b7667338e99aa1efe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583906"
---
# <a name="about-imediaobject"></a>À propos de IMediaObject

L’interface **IMediaObject** est l’interface requise pour DMOs. **IMediaObject** contient les méthodes qu’un plug-in Lecteur Windows Media DSP utilise pour obtenir des données à partir d’Lecteur Windows Media, pour traiter les données et pour retourner les données traitées à Lecteur Windows Media. pour obtenir la documentation complète de l’interface **IMediaObject** , consultez la section DirectShow de la SDK Windows.

Les méthodes de **IMediaObject** peuvent être classées comme suit :

## <a name="methods-that-handle-format-negotiation"></a>Méthodes qui gèrent la négociation de format

il s’agit des méthodes que Lecteur Windows Media appelle pour obtenir des informations sur les formats de données pris en charge par le plug-in. Ces méthodes incluent les tâches suivantes :

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

plusieurs de ces méthodes, telles que **GetInputType** et **SetInputType**, utilisent la structure de **\_ \_ TYPE de média DMO** pour décrire le format des données utilisées par un flux. lorsque Lecteur Windows Media appelle ces méthodes, il fournit un pointeur vers une structure de **\_ \_ TYPE de média DMO** . si une méthode telle que **SetInputType** spécifie les informations sur le type de média, le plug-in doit copier la structure du **\_ \_ type de média DMO** sur une variable membre et inspecter ses membres de données pour déterminer le type de données que Lecteur Windows Media fournira dans la mémoire tampon d’entrée. si une méthode telle que **GetInputType** récupère les informations de type de média, le plug-in doit copier l’adresse de la variable membre contenant la structure de **\_ \_ type de média DMO** vers le pointeur fourni par Lecteur Windows Media dans la liste de paramètres.

Lecteur Windows Media utilise principalement deux membres de la structure de **\_ \_ TYPE de média DMO** :

-   **MajorType**: identificateur global unique (Guid) qui spécifie la catégorie globale des médias, tels que l’audio ou la vidéo.
-   **SubType**: GUID qui spécifie une description plus détaillée du média, telle que l’audio PCM.

ces guid se trouvent dans l’en-tête nommé uuid. h, qui est inclus avec le SDK Windows.

les méthodes telles que **GetInputSizeInfo** fournissent des informations pour Lecteur Windows Media sur la quantité de mémoire requise pour allouer les tampons de traitement. les méthodes telles que **GetStreamCount** et **GetOutputStreamInfo** fournissent des informations pour Lecteur Windows Media sur le nombre et le caractère des flux pris en charge par le plug-in DSP.

**GetInputMaxLatency** et **SetInputMaxLatency** sont implémentés par DMOs dans des cas spéciaux. Lecteur Windows Media Les plug-ins DSP doivent retourner E \_ NOTIMPL.

## <a name="methods-that-specify-or-retrieve-state-information"></a>Méthodes qui spécifient ou récupèrent les informations d’État

il s’agit des méthodes qui Lecteur Windows Media appellent pour récupérer ou définir des valeurs relatives à l’état actuel du plug-in. Ces méthodes incluent les tâches suivantes :

-   **GetInputCurrentType**
-   **GetInputStatus**
-   **GetOutputCurrentType**

**GetInputCurrentType** et **GetOutputCurrentType** utilisent la structure de **\_ \_ TYPE de média DMO** pour renvoyer des informations à Lecteur Windows Media sur les types de média précédemment définis pour les flux d’entrée et de sortie. **GetInputStatus** retourne un indicateur qui indique à Lecteur Windows Media si le plug-in DSP peut accepter des données d’entrée.

## <a name="methods-that-handle-buffering-and-processing-data"></a>Méthodes qui gèrent la mise en mémoire tampon et le traitement des données

il s’agit des méthodes que Lecteur Windows Media appelle pour initier les différents processus que le plug-in effectue pour effectuer le traitement du signal numérique. Ces méthodes incluent les tâches suivantes :

-   **AllocateStreamingResources**
-   **Discontinuité**
-   **Purge**
-   **FreeStreamingResources**
-   **Verrou**
-   **ProcessInput**
-   **ProcessOutput**

Lecteur Windows Media appelle **AllocateStreamingResources** et **FreeStreamingResources** pour fournir au plug-in DSP la possibilité de configurer ou de libérer des mémoires tampons supplémentaires pouvant être requises par le plug-in pour le traitement interne.

Lecteur Windows Media les plug-ins DSP n’ont pas besoin d’utiliser la méthode de **discontinuation** DMO.

Lecteur Windows Media appelle **flush** pour demander au plug-in DSP de vider toutes les données mises en mémoire tampon. Le plug-in doit libérer toutes les références aux interfaces **IMediaBuffer** , effacer toutes les valeurs qui spécifient l’horodatage ou l’exemple de longueur pour la mémoire tampon du média, et réinitialiser tous les États internes qui dépendent du contenu de l’exemple de support.

Lecteur Windows Media appelle ProcessInput pour passer un pointeur vers une interface **IMediaBuffer** vers le plug-in DSP. cette interface fournit l’accès à la mémoire tampon d’entrée allouée par Lecteur Windows Media pour fournir des données au plug-in. Lecteur Windows Media appelle ensuite **ProcessOutput** pour passer un pointeur vers une interface **IMediaBuffer** qui fournit l’accès à la mémoire tampon de sortie allouée par Lecteur Windows Media pour recevoir les données traitées du plug-in DSP.

L’interface **IMediaObject** comprend une méthode nommée **Lock**. cette méthode est conçue pour acquérir ou libérer un verrou sur le DMO pour que les DMO sérialisés lors de l’exécution de plusieurs opérations. La version de **IMediaObject :: Lock** dans le code de l’Assistant remplace l’implémentation ATL de **Lock**. étant donné que Lecteur Windows Media sérialise les appels passés à l’interface DMO d’un plug-in DSP, l’implémentation de **Lock** retourne simplement S \_ OK. pour plus d’informations sur la création d’un DMO multithread, reportez-vous à la section DirectShow de la SDK Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interfaces requises**](required-interfaces.md)
</dt> </dl>

 

 




