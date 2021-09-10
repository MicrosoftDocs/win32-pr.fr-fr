---
title: Positionner dans Flux
description: Positionner dans Flux
ms.assetid: 97ab491d-1a58-4b4b-a13a-215be24dac1c
keywords:
- AVIStreamStart fonction)
- AVIStreamFindSample fonction)
- AVIStreamSampleToTime fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252aa938d32c323da9fcf7ae106d11db0ff2fb4
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369255"
---
# <a name="positioning-in-streams"></a>Positionner dans Flux

AVIFile offre plusieurs moyens de rechercher et de déplacer vers une position dans un flux de données. Les fonctions et les macros de cette section permettent à votre application de rechercher la position de départ, la longueur et les images clés (contenant une image complète dans l’exemple) dans un flux. Les fonctions et les macros associent également le temps à des positions dans un flux en calculant le temps écoulé nécessaire pour lire un flux de son début à n’importe quel point dans un flux.

## <a name="finding-the-starting-position"></a>Recherche de la position de départ

Vous pouvez récupérer le numéro de l’échantillon de la première image d’un flux vidéo à l’aide de la fonction [**AVIStreamStart**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart) . (Les frames d’un film peuvent commencer par l’exemple 0 ou 1, selon la préférence de l’auteur.) Vous pouvez également obtenir ces informations à l’aide de la fonction [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) . Cette fonction stocke le nombre d’échantillons dans le membre **dwStart** de la structure [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) . Vous pouvez récupérer l’heure de début du premier échantillon d’un flux à l’aide de la macro [**AVIStreamStartTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime) .

Vous pouvez récupérer la longueur du flux à l’aide de la fonction [**AVIStreamLength**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength) . Cette fonction retourne le nombre d’échantillons dans le flux. Vous pouvez également obtenir ces informations à l’aide de la fonction **AVIStreamInfo** . Cette fonction stocke la longueur du flux dans le membre **dwLength** de la structure **AVISTREAMINFO** . Pour récupérer la longueur d’un flux en millisecondes, utilisez la macro [**AVIStreamLengthTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime) .

Dans un flux vidéo, chaque échantillon correspond généralement à une image de la vidéo. Toutefois, il peut y avoir des exemples pour lesquels aucune donnée vidéo n’est présente. Si vous appelez la fonction [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) en spécifiant l’une de ces positions, elle retourne une longueur de données de 0 octet. Vous pouvez trouver des exemples qui contiennent des données à l’aide de la fonction [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) et en spécifiant l’indicateur de recherche \_ .

Dans un flux audio, chaque exemple correspond à un bloc de données de données audio. Par exemple, si les données audio ont un format 22 kHz ADPCM (modulation différentielle par impulsion de code), chaque échantillon pour **AVIStreamLength** correspond à un bloc de 256 octets de données audio compressées. Ce bloc de données audio contient environ 500 échantillons audio lors de la décompression. Toutefois, les fonctions et les macros de AVIFile traitent chaque bloc de 256 octets comme un seul échantillon.

> [!Note]  
> Positions valides dans une plage de flux depuis le début jusqu’à la fin du flux, qui est la somme du point de départ du flux et de sa longueur. La position représentée par la somme de la position de départ et de la longueur correspond à une heure après le rendu des dernières données ; il ne contient aucune donnée. Vous pouvez récupérer l’exemple de numéro qui représente la fin du flux à l’aide de la macro [**AVIStreamEnd**](/windows/desktop/api/Vfw/nf-vfw-avistreamend) . Vous pouvez récupérer la valeur de temps en millisecondes qui représente la fin du flux à l’aide de la macro [**AVIStreamEndTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime) .

 

## <a name="finding-sample-and-key-frames"></a>Recherche d’exemples et d’images clés

Vous pouvez rechercher différents types d’exemples dans un flux à l’aide de la fonction [**AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) . Cette fonction effectue une recherche vers l’arrière ou vers l’avant dans un flux pour obtenir un exemple du type approprié, en commençant par l’exemple de nombre que vous spécifiez. Vous pouvez rechercher différents types d’exemples dans un flux en spécifiant un indicateur dans la séquence d’appel **AVIStreamFindSample** . Spécifiez l' \_ indicateur de recherche pour localiser les exemples non vides ou pour ignorer les exemples qui n’ont pas de données. Spécifiez l' \_ indicateur de recherche de clé pour rechercher les images clés qui contiennent les données pour afficher une image complète sans avoir à référencer des frames précédents. Spécifiez l' \_ indicateur de format de recherche pour rechercher les modifications apportées au format. **AVIStreamFindSample** est principalement utilisé avec les flux vidéo.

Plusieurs macros qui utilisent des fonctions AVIFile complètent les fonctionnalités de recherche de flux. La liste suivante fournit une brève description de chaque macro. Les macros qui recherchent une position ou un type de données spécifique nécessitent la spécification d’un emplacement de départ dans le flux.



| Macro                                                                | Description                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)                   | Indique si un exemple dans un flux spécifié est une image clé.                                                            |
| [**AVIStreamNearestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)         | Localise l’image clé au niveau ou au-dessus d’une position spécifiée dans un flux.                                                     |
| [**AVIStreamNearestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime) | Détermine l’heure correspondant au début de l’image clé la plus proche (au plus près) à une heure spécifiée dans un flux. |
| [**AVIStreamNearestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)             | Localise l’exemple non vide le plus proche à la position spécifiée ou avant dans un flux.                                       |
| [**AVIStreamNearestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)     | Détermine l’heure correspondant au début d’un échantillon le plus proche d’une heure spécifiée dans un flux.             |
| [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)               | Localise l’image clé suivante à la suite d’une position spécifiée dans un flux.                                                      |
| [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)       | Retourne l’heure de l’image clé suivante dans un flux, en commençant à un moment donné.                                               |
| [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)                   | Localise l’exemple non vide suivant à partir d’une position spécifiée dans un flux.                                                     |
| [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)           | Retourne l’heure à laquelle un exemple passe à l’exemple suivant dans le flux.                                                    |
| [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)               | Localise l’image clé qui précède une position spécifiée dans un flux.                                                       |
| [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)       | Retourne l’heure de l’image clé précédente dans le flux, en commençant à un moment donné.                                         |
| [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)                   | Localise l’exemple non vide qui précède une position spécifiée dans un flux.                                                 |
| [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)           | Détermine l’heure à laquelle l’exemple précédent remplace son prédécesseur dans le flux.                                    |
| [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)           | Retourne l’exemple dans un flux qui se produit en même temps qu’un exemple qui se produit dans un deuxième flux.                     |



 

## <a name="switching-between-samples-and-time"></a>Basculement entre les exemples et l’heure

Vous pouvez déterminer le temps écoulé entre le début d’un flux et un exemple à l’aide de la fonction [**AVIStreamSampleToTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime) . Cette fonction convertit l’échantillon de nombre en une valeur d’heure exprimée en millisecondes. Pour une image vidéo (qui s’étend sur plusieurs millisecondes), cette valeur représente l’heure de début de la lecture de l’échantillon depuis le début de la lecture et suppose que le clip vidéo est lu à la vitesse normale. Dans le cas d’un exemple audio (qui a plusieurs échantillons en millisecondes), la valeur de temps correspond à l’heure à laquelle l’échantillon commence à jouer et suppose que le flux audio est lu à la vitesse normale.

À l’inverse, vous pouvez trouver l’exemple de numéro associé à une valeur d’heure à l’aide de la fonction [**AVIStreamTimeToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample) . Cette fonction convertit la valeur de milliseconde en un nombre échantillon et suppose que le clip vidéo est lu à la vitesse normale.

Étant donné que **AVIStreamSampleToTime** retourne l’heure de début de la lecture d’une image, la relation entre **AVIStreamSampleToTime** et **AVIStreamTimeToSample** n’est pas véritablement inverse. Elles déterminent la position dans un fichier plus acurately qu’elles ne déterminent l’heure. Par exemple, deux échantillons audio consécutifs peuvent être lus dans la même milliseconde. L’utilisation de **AVIStreamSampleToTime** pour convertir les exemples de nombres donne des valeurs de temps identiques. Si vous reconvertissez la valeur d’heure en un nombre d’échantillons à l’aide de **AVIStreamTimeToSample**, un seul échantillon est référencé.

 

 




