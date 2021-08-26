---
description: Cette rubrique décrit comment Media Foundation transformations doit gérer les horodatages.
ms.assetid: 4ab576ce-becd-4736-921e-e463c0dff841
title: Horodatages et durées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22452e8b6b8094e643126f479f13b2c447db584588f3be1c1aa6595b3e7e2bb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953199"
---
# <a name="time-stamps-and-durations"></a>Horodatages et durées

Cette rubrique décrit comment [Media Foundation transformations](media-foundation-transforms.md) doit gérer les horodatages.

Un MFT doit définir un horodatage et une durée aussi précis que possible sur tous les échantillons de sortie. Pour une table MFT simple qui prend une mémoire tampon d’entrée et la traite complètement dans une mémoire tampon de sortie, la table MFT doit simplement copier l’horodatage et la durée directement de l’exemple d’entrée vers l’exemple de sortie. Toutefois, de nombreuses transformations sont plus complexes que cela et peuvent nécessiter des calculs plus complexes de l’heure de sortie. Toutes les MFTs doivent respecter les règles de base suivantes :

-   Une table MFT doit essayer de placer un horodatage et une durée sur tous les échantillons de sortie vidéo ou audio non compressés si un horodatage ou une durée précis est donné (e) sur les échantillons d’entrée ou peut être calculé. L’interpolation peut être nécessaire pour certains horodatages de sortie, en particulier pour les décodeurs.
-   Les horodatages et les durées des échantillons d’entrée doivent être préservés autant que possible sur les échantillons de sortie.
-   Les horodatages de sortie ou les durées peuvent ne pas correspondre à l’entrée, car la table MFT contient des données de retour ou des données de sortie dans des parties de taille différente de celles de l’entrée. Dans ce cas, la table MFT doit calculer l’horodatage de sortie à partir de l’exemple d’entrée le plus ancien qui contient les données utilisées pour créer l’exemple de sortie. Pour calculer l’horodatage de sortie, ajoutez l’horodatage d’entrée de l’exemple d’entrée approprié à la durée des données qui ont déjà été transformées à partir de cet exemple. Le deuxième exemple à la fin de cette section illustre cette idée.
-   Si les échantillons d’entrée ont une durée, cette durée doit être conservée. Si un exemple d’entrée n’a pas de durée, la table MFT doit calculer une durée si possible à partir de la taille de la mémoire tampon de sortie ou le débit de données donné par le type de média.
-   Les durées calculées doivent être tronquées (arrondies vers le bas), pas arrondies à l’incrément le plus proche. Le pipeline a suffisamment de marge pour gérer les durées légèrement inexactes, mais il est plus facile pour le pipeline de gérer une durée de 1% trop petite qu’une durée de 1% trop longue. Cela dit, il n’y a aucune raison de raccourcir délibérément les durées, à l’exception de l’arrondi.

### <a name="decoders"></a>Décodeurs

Un décodeur convertit les paquets compressés en données non compressées. Étant donné que la sortie est décompressée, les décodeurs ont une obligation spéciale d’obtenir les horodatages et les durées correctes. Certains formats compressés, plus particulièrement MPEG-2, n’ont pas de datage pour tous les paquets en entrée et n’ont souvent aucune durée sur aucun paquet. Pour ces formats, le décodeur est chargé de placer un horodatage et une durée valides pour chaque échantillon de sortie, en additionnant les durées implicites de l’ensemble de la sortie depuis le dernier exemple d’entrée horodaté.

Pour la vidéo, si la durée n’est pas disponible dans le format compressé, le décodeur doit calculer la durée comme l’inverse de la fréquence d’images, converti en unités de nanosecondes 100 et arrondi à la valeur inférieure.

Pour l’audio, si la durée n’est pas disponible dans le format compressé, le décodeur doit calculer la durée comme l’inverse du taux d’échantillonnage audio multiplié par le nombre d’échantillons dans la mémoire tampon de sortie, convertis en unités de 100 nanosecondes et arrondis à la baisse.

La seule fois où une transformation doit générer un exemple sans horodatage est si la table MFT n’a jamais reçu d’horodatage sur un échantillon d’entrée, ou s’il n’existe aucun moyen de calculer un horodatage de sortie précis à partir de l’horodatage d’entrée précédent.

### <a name="audio-decoders"></a>Décodeurs audio

Pour les décodeurs audio, la durée de chaque échantillon de sortie est calculée à partir de la fréquence d’échantillonnage audio et du nombre d’échantillons PCM par canal dans la mémoire tampon de sortie.

La méthode correcte pour calculer les horodatages de sortie varie selon que les exemples d’entrée contiennent des horodatages.

Si les exemples d’entrée contiennent des horodatages, le décodeur calcule les horodatages de sortie à partir des horodatages d’entrée, comme suit :

-   Si chaque mémoire tampon d’entrée contient un ou plusieurs frames compressés complets, sans frames partiels, l’horodatage de sortie est égal à l’horodatage d’entrée, moins la latence connue du décodeur. Par exemple, un décodeur Dolby Digital (AC-3) a une latence de 256 PCM. Par exemple, au taux d’échantillonnage de 48 kHz, la latence est de 5,33 millisecondes (MS). Par conséquent, si l’horodatage d’entrée est 1000 ms, l’horodatage de sortie est 1000-5,33 = 994,66 ms. Si la mémoire tampon d’entrée contient plusieurs frames compressés entiers, le décodeur produira un échantillon de sortie pour chaque frame de l’exemple d’entrée. Tous les échantillons de sortie seront horodatés correctement, de sorte qu’il n’y a pas d’écarts.
-   Selon le format de transport, une mémoire tampon d’entrée peut contenir des frames partiels. Par exemple, une mémoire tampon peut contenir une partie d’un frame à partir de la mémoire tampon d’entrée précédente, suivie d’un ou de plusieurs frames complets, suivi du début du frame suivant. Dans ce cas, il est généralement correct de supposer que l’horodatage d’entrée correspond au premier frame qui démarre dans la mémoire tampon. (Autrement dit, un frame partiel qui a démarré dans la mémoire tampon précédente n’est pas inclus dans l’horodatage de la mémoire tampon actuelle.) Calculez l’horodatage de sortie en conséquence.

Si les exemples d’entrée ne contiennent pas d’horodatage :

-   Le décodeur doit générer ses propres horodatages, en définissant le premier horodatage de sortie sur zéro.
-   La durée de l’échantillon est calculée à partir du nombre d’échantillons de sortie dans la mémoire tampon et du taux d’échantillonnage.
-   Les horodatages suivants sont calculés à partir de l’horodatage précédent et de la durée : horodatage actuel + durée actuelle = horodatage suivant. Il ne doit y avoir aucun écart dans les horodatages de sortie.

Si le flux d’entrée contient initialement des horodatages, mais pour une raison quelconque, pour une raison quelconque, le décodeur doit continuer à générer ses propres horodatages de sortie, de sorte qu’ils soient continus et qu’il n’y ait aucun intervalle.

Si le flux d’entrée contient des horodatages, mais qu’il y a des écarts dans les temps, le décodeur propage simplement ces lacunes. En d’autres termes, le décodeur ne doit pas tenter de corriger les horodatages incohérents dans le flux d’entrée.

### <a name="mixers"></a>Mélangeurs

> [!Note]  
> dans Windows Vista, le pipeline Media Foundation ne prend pas en charge MFTs avec plus d’une entrée. les MFTs à entrées multiples sont pris en charge dans Windows 7.

 

Un mélangeur prend plusieurs entrées et les mélange en une seule sortie. Si les flux d’entrée ne sont pas complètement verrouillés, ou sont légèrement décalés les uns des autres, il peut y avoir une ambiguïté sur le temps à définir sur la sortie. Voici quelques instructions, selon le type de média :

-   HD. Au démarrage ou immédiatement après un drainage ou un vidage, un mélangeur audio doit attendre pour produire des échantillons de sortie jusqu’à ce qu’il ait reçu un échantillon d’entrée sur tous les flux d’entrée requis. À ce stade, il doit choisir l’horodatage le plus ancien des échantillons initiaux à utiliser comme référence pour les horodatages de sortie. Les autres flux doivent être remplis avec un silence pour commettre les différences de temps. Si un exemple est reçu sur un flux d’entrée facultatif, il doit également être pris en compte dans le calcul. À partir de ce point, la MFT doit s’efforcer de produire une chaîne continue et ininterrompue d’horodatages de sortie. En général, la table MFT ne doit pas essayer de tenir compte d’une dérive de flux par rapport à une autre. Au lieu de cela, il doit calculer les horodatages de sortie à partir de l’horodatage de la ligne de base, le taux de sortie et les tailles de mémoire tampon. Lorsqu’un autre drainage ou vidage se produit, la table MFT doit réinitialiser ses horodatages de référence.

-   Vidéo. Au démarrage ou immédiatement après un drainage ou un vidage, un mélangeur vidéo doit attendre de produire des échantillons de sortie jusqu’à ce qu’il ait reçu un échantillon d’entrée sur tous les flux d’entrée requis. À ce stade, il doit choisir l’horodatage le plus ancien des échantillons initiaux à utiliser comme référence pour les horodatages de sortie. En général, elle doit s’efforcer de conserver les horodatages de sortie continus et réguliers et les durées fixes, même si l’entrée n’est pas aussi régulière, si nécessaire, en répétant les trames d’entrée.

### <a name="encoders"></a>Encodeurs

Un encodeur convertit le contenu audio ou vidéo non compressé en paquets compressés. Un encodeur doit suivre les instructions suivantes :

-   L’encodeur doit respecter les conventions du format de sortie. Si le format n’a pas d’horodatage pour chaque échantillon, comme dans MPEG-2, tous les échantillons de sortie n’ont pas besoin d’un horodatage et d’une durée.

-   Les horodatages d’entrée doivent être conservés dans le format de sortie, si le format contient des champs pour les horodatages, à moins que des informations de temps plus performantes soient disponibles à partir d’une autre source, telle que l’application elle-même.

### <a name="multiplexers"></a>Multiplexeurs

> [!Note]  
> dans Windows Vista, le pipeline Media Foundation ne prend pas en charge MFTs avec plus d’une entrée. les MFTs à entrées multiples sont pris en charge dans Windows 7.

 

Un multiplexeur combine deux flux audio ou vidéo différents en un seul format entrelacé, tel que le flux de transport AVI ou MPEG-2. Un multiplexeur doit suivre les instructions suivantes :

-   Le multiplexeur doit respecter les conventions du format de sortie. Si le format n’a pas d’horodatage pour chaque échantillon, comme dans MPEG-2, tous les échantillons de sortie n’ont pas besoin d’un horodatage et d’une durée.

-   L’horodatage doit refléter l’heure la plus ancienne qui serait placée sur toute image qui commence dans ce paquet, ou l’heure du premier échantillon audio qui serait décodé à partir de ce paquet. Ignorez cette règle si elle est en conflit avec les conventions du format de sortie.

### <a name="demultiplexers"></a>Démultiplexeurs

Un démultiplexeur fractionne un format entrelacé, tel qu’un flux de transport AVI ou MPEG-2, dans les flux audio et vidéo sous-jacents.

Si le format contient des informations d’horodatage spécifiques qui peuvent être utilisées pour calculer des horodatages de sortie précis en fonction des horodatages d’entrée, ces informations doivent être utilisées. Toutefois, si le format contient des heures dans une base complètement différente qui ne porte aucune relation avec les horodatages d’entrée, et qu’un décalage précis de l’horodatage d’entrée ne peut pas être calculé, les heures propres au format doivent être ignorées.

Si le format n’a pas d’informations d’horodatage utilisables, le démultiplexeur doit suivre les règles suivantes :

-   Si possible, les flux de sortie non compressés doivent avoir des horodatages et des durées valides, calculés à partir de l’horodatage d’entrée précédent le plus proche.

-   Les flux de sortie compressés doivent avoir des horodatages uniquement pour le premier échantillon de sortie dérivé d’un exemple d’entrée avec un horodatage. Si l’exemple d’entrée n’a pas d’horodatage, aucun échantillon de sortie dérivé de cet exemple d’entrée ne doit avoir un horodatage. Si l’exemple d’entrée est divisé en plusieurs exemples de sortie, seul le premier exemple de sortie doit avoir un horodatage, et le reste ne doit pas avoir de datage.

### <a name="examples"></a>Exemples

Exemple 1. Supposons qu’un effet vidéo prend toujours une trame d’entrée non compressée, applique l’effet et le copie dans la sortie. Elle ne conserve jamais de frame ou de tampons d’entrée. Cette table MFT copie simplement l’horodatage et la durée de l’exemple d’entrée vers l’exemple de sortie, s’ils sont disponibles, et n’effectue aucun calcul de temps.

Exemple 2. Supposons qu’un effet audio transforme tout sauf 10 millisecondes (MS) de chaque mémoire tampon d’entrée, ce qui permet d’économiser 10 ms supplémentaires pour combiner avec la mémoire tampon suivante. Elle obtient un flux d’exemples qui ont tous une durée de 50 ms. Les heures d’entrée sont indiquées dans le tableau suivant.



| Exemple | Heure d’entrée | Durée d’entrée | Heure de sortie | Durée de sortie |
|--------|------------|----------------|-------------|-----------------|
| 1      | 20         | 50             | 20          | 40              |
| 2      | 70         | 50             | 60          | 50              |
| 3      | 121        | 50             | 110         | 50              |
| 4      | 171        | 50             | 161         | 50              |



 

Notez la différence de 1-ms entre la durée réelle de l’échantillon 2 et la durée implicite basée sur l’horodatage suivant (121 ? 70 = 51).

Étant donné que la MFT conserve 10 ms, il génère le premier 40 ms de l’échantillon d’entrée 1 comme exemple de sortie 1, avec un horodatage de 20 ms et une durée de 40 ms.

L’exemple de sortie 2 combine le 10 ms précédemment retenu avec 40 ms de l’exemple d’entrée 2. Cet exemple reçoit un horodatage de 60 ms (horodatage de l’exemple d’entrée précédent, 20 ms, plus la durée des données déjà traitées à partir de cet exemple, 40ms). Elle reçoit une durée de 50 ms.

De même, l’exemple suivant a un horodatage de 110ms (70ms + 40ms) avec une durée de 50 ms.

Le calcul suivant est plus intéressant. L’horodatage implicite de l’heure et de la durée de sortie précédentes serait 160 ms (horodatage 110 MS + Duration 50 ms). Toutefois, l’horodatage de sortie est supposé être calculé à partir de l’horodatage d’entrée de l’exemple d’entrée le plus ancien qui chevauche l’échantillon de sortie dans le temps, plus la longueur de toutes les données déjà traitées à partir de cet exemple. L’exemple d’entrée qui se chevauche le plus proche est l’exemple 4 (horodatage = 171), mais ce n’est pas le plus ancien. L’exemple qui se chevauche le plus ancien est Sample 3 (horodatage = 121). Si vous ajoutez le 40ms qui a déjà été traité à partir de cet exemple, le résultat est 161.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’une table MFT personnalisée](writing-a-custom-mft.md)
</dt> </dl>

 

 



