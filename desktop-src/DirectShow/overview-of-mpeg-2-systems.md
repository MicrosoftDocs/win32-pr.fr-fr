---
description: Vue d’ensemble des systèmes MPEG-2
ms.assetid: 1ebfb194-002f-40ac-9be5-267861b6687b
title: Vue d’ensemble des systèmes MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4206b36db7b3172c6e161745922e83490855c73c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312321"
---
# <a name="overview-of-mpeg-2-systems"></a>Vue d’ensemble des systèmes MPEG-2

Cette section fournit une vue d’ensemble générale et non technique de la couche de systèmes MPEG-2. Le système MPEG-2 est la norme qui définit la façon dont les flux audio et vidéo sont multiplexés dans MPEG-2.

**Flux élémentaire**

Le multiplexage MPEG-2 démarre avec un ou plusieurs flux d’octets, appelés flux élémentaires, qui contiennent des données vidéo, audio ou autres. Par exemple, une vidéo ES contient des images vidéo compressées, ainsi que des en-têtes de séquence, des en-têtes de groupe d’images et tout autre objet requis par le décodeur pour décoder le flux. La couche systèmes ne définit pas le contenu du flux d’octets ES.

Un flux élémentaire est divisé en paquets, formant un *flux élémentaire de paquets* (PES). Les paquets PES ont une longueur variable. Le contenu du paquet est appelé la *charge utile*. Chaque paquet PES comprend également un en-tête. Le multiplexeur attribue un ID de flux de 1 octets à chaque extension PES ; les paquets PES individuels sont identifiés par l’ID de flux dans l’en-tête de paquet. Pour les flux audio, l’ID de flux se présente sous la forme 110 *xxxxx*. Pour la vidéo, l’ID de flux se présente sous la forme 1110 *yyyy*.

La norme MPEG-2 définit deux méthodes pour fournir des flux élémentaires en paquets : les *flux de programme* et les *flux de transport*.

**Flux de programme**

Les flux de programme sont conçus pour les environnements qui sont sans erreur, tels que le stockage de fichiers local. Dans un flux de programme, les paquets PES sont multiplexés et organisés en unités appelées *packs*. Tous les flux PES dans un flux de programme sont synchronisés avec la même horloge.

**Flux de transport**

Les flux de transport (TS) sont conçus pour les environnements non fiables ou sujets aux erreurs, tels que les diffusions réseau. Ils peuvent également contenir plusieurs programmes synchronisés avec différentes horloges. Un flux de transport ajoute une deuxième couche de paquets de paquets. les flux PES sont empaquetés dans des paquets de flux de transport, qui ont une taille fixe de 188 octets par paquet. Les paquets TS peuvent également contenir des flux d’informations de programme, qui sont décrits dans la section suivante.

Chaque paquet TS possède un en-tête de 4 octets, ainsi qu’un champ d’adaptation facultatif qui contient des informations d’en-tête supplémentaires. Le multiplexeur attribue un ID de programme (PID) à chaque flux ou flux d’informations de programme PES. Les PID servent à identifier les paquets TS, à l’instar de la façon dont les ID de flux identifient les paquets PES. (Si un flux de transport contient plusieurs programmes, les ID de *flux* peuvent ne pas être uniques, mais les attributions PID sont uniques dans le flux de transport.)

**Informations spécifiques au programme**

Comme un flux de transport peut comporter plusieurs programmes, il doit exister un moyen d’associer les différents paquets PES aux programmes auxquels ils appartiennent. Cela s’effectue à l’aide de tables qui identifient les flux de programme. Collectivement, ces données sont appelées informations spécifiques au programme (PSI). Les données PSI sont transmises dans des paquets TS, tout comme les données PES. Il existe différents types de données PSI, notamment :

-   Table d’association de programmes (PAT). Le PAT est toujours affecté au PID 0x000. Chaque entrée de la PAT est un PID qui identifie les paquets VPM pour ce programme (voir élément suivant).
-   Table de mappage de programmes (VPM). Chaque VPM définit un programme. VPM contient une liste de flux. chaque entrée de table fournit le PID pour ce flux, ainsi qu’un code qui identifie le type de flux. ISO/IEC 13818-1 définit certains types de flux standard ; une liste abrégée est présentée dans le tableau suivant.

    | type de flux \_ | Description  |
    |--------------|--------------|
    | 0x01         | Vidéo MPEG-1 |
    | 0x02         | Vidéo MPEG-2 |
    | 0x03         | MPEG-1 audio |
    | 0x04         | Audio MPEG-2 |
    | 0x80-0xFF  | Utilisateur privé |

    

     

    D’autres normes basées sur MPEG-2, telles que ATSC, peuvent définir des types de flux supplémentaires dans la plage « User Private ». Par exemple, ATSC définit 0x81 comme audio Dolby AC-3.

-   Tables d’accès conditionnel (CAT)
-   Tables d’identification réseau (Nil)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge de MPEG-2 dans DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



