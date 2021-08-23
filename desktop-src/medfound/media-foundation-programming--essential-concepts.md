---
description: Si vous débutez avec des médias numériques, cette rubrique présente quelques concepts que vous devez comprendre avant d’écrire une application Media Foundation.
ms.assetid: d76d655e-23f3-407c-97a1-be015b0de37d
title: 'Media Foundation : notions essentielles'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 825e84b3c7ad3060cae0a2530bc9a7af3155fd9113c490ce2c42f69771c1f9b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357258"
---
# <a name="media-foundation-essential-concepts"></a>Media Foundation : notions essentielles

Si vous débutez avec des médias numériques, cette rubrique présente quelques concepts que vous devez comprendre avant d’écrire une application Media Foundation.

-   [Flux](#streams)
-   [Compression](#compression)
-   [Conteneurs de médias](#media-containers)
-   [Formats](#formats)
-   [Rubriques connexes](#related-topics)

## <a name="streams"></a>Flux

Un *flux* est une séquence de données multimédias avec un type uniforme. Les types les plus courants sont audio et vidéo, mais un flux peut contenir presque n’importe quel type de données, notamment du texte, des commandes de script et des images fixes. Le terme *flux* dans cette documentation n’implique pas la livraison sur un réseau. Un fichier multimédia destiné à la lecture locale contient également des flux.

En règle générale, un fichier multimédia contient soit un flux audio unique, soit exactement un flux vidéo et un flux audio. Toutefois, un fichier multimédia peut contenir plusieurs flux du même type. Par exemple, un fichier vidéo peut contenir des flux audio dans différentes langues. Au moment de l’exécution, l’application sélectionne le flux à utiliser.

## <a name="compression"></a>Compression

La *compression* fait référence à tout processus qui réduit la taille d’un flux de données en supprimant les informations redondantes. Les algorithmes de compression se répartissent en deux grandes catégories :

-   Compression *sans perte* . À l’aide d’un algorithme sans perte, les données reconstruites sont identiques à celles d’origine.
-   Compression avec *perte* . À l’aide d’un algorithme de perte, les données reconstruites sont une approximation de l’original, mais n’est pas une correspondance exacte.

Dans la plupart des autres domaines, la compression avec perte n’est pas acceptable. (Imagine la récupération d’une « approximation » d’une feuille de calcul !) Toutefois, les schémas de compression avec perte sont bien adaptés à l’audio et à la vidéo, pour plusieurs raisons.

La première raison est liée à la physique de perception humaine. Lorsque nous écoutons un son complexe, comme un enregistrement musical, certaines des informations contenues dans ce son ne sont pas perceptibles à l’oreille. Avec l’aide de la théorie du traitement des signaux, il est possible d’analyser et de séparer les fréquences qui ne peuvent pas être perçues. Ces fréquences peuvent être supprimées sans effet de perception. Bien que le son reconstruit ne corresponde pas exactement à l’original, il *est le même* que celui de l’écouteur. Des principes similaires s’appliquent à la vidéo.

Deuxièmement, une certaine dégradation de la qualité du son ou de l’image peut être acceptable, en fonction de l’objectif prévu. Dans la téléphonie, par exemple, l’audio est souvent fortement compressé. Le résultat est suffisamment parfait pour une conversation téléphonique, mais vous ne souhaitez pas écouter un orchestre Symphony sur un téléphone.

La compression est également appelée « *encodage*» et un appareil qui encode est appelé « *encodeur*». Le processus inverse est le *décodage* et l’appareil est un naturellement appelé *décodeur*. Le terme général pour les encodeurs et les décodeurs est le *codec*. Les codecs peuvent être implémentés dans le matériel ou les logiciels.

La technologie de compression a changé rapidement depuis l’avènement des médias numériques et un grand nombre de schémas de compression sont actuellement utilisés. Ce fait est l’un des principaux défis de la programmation multimédia numérique.

## <a name="media-containers"></a>Conteneurs de médias

Il est rare de stocker un flux audio ou vidéo brut en tant que fichier d’ordinateur, ou d’en envoyer un directement sur le réseau. Pour une chose, il serait impossible de décoder un tel flux, sans connaître à l’avance le codec à utiliser. Par conséquent, les fichiers multimédias contiennent généralement au moins certains des éléments suivants :

-   En-têtes de fichier qui décrivent le nombre de flux, le format de chaque flux, et ainsi de suite.
-   Index qui permet l’accès aléatoire au contenu.
-   Métadonnées qui décrivent le contenu (par exemple, l’artiste ou le titre).
-   En-têtes de paquets, pour activer la transmission réseau ou l’accès aléatoire.

Cette documentation utilise le terme *conteneur* pour décrire l’ensemble du package de flux, d’en-têtes, d’index, de métadonnées et ainsi de suite. La raison de l’utilisation du terme *conteneur* plutôt que de *fichier* est que certains formats de conteneur sont conçus pour la diffusion en direct. Une application peut générer le conteneur en temps réel, ne jamais le stocker dans un fichier.

Le format de fichier AVI est un exemple précoce d’un conteneur de médias. Voici d’autres exemples : MP4 et ASF (Advanced Systems Format). Les conteneurs peuvent être identifiés par une extension de nom de fichier (par exemple, .mp4) ou par type MIME.

Le diagramme suivant montre une structure type pour un conteneur multimédia. Le diagramme ne représente pas un format spécifique. les détails de chaque format varient considérablement.

![Diagramme montrant un conteneur multimédia classique](images/concepts01.png)

Notez que la structure affichée dans le diagramme est hiérarchique, avec des informations d’en-tête apparaissant au début du conteneur. Cette structure est typique de nombreux formats de conteneur (mais pas tous). Notez également que la section Data contient des paquets audio et vidéo entrelacés. Ce type d’entrelacement est courant dans les conteneurs multimédias.

Le terme *multiplexage* fait référence au processus de transmission des flux audio et vidéo et de l’entrelacement des paquets dans le conteneur. Le processus inverse, réassemblant les flux à partir des données en paquets, est appelé *démultiplexage*.

## <a name="formats"></a>Formats

Dans les médias numériques, le *format* de terme est ambigu. Un format peut faire référence au type d' *encodage*, par exemple une vidéo H. 264 ou le *conteneur*, tel que MP4. Cette distinction est souvent déroutante pour les utilisateurs ordinaires. Les noms donnés aux formats multimédias ne sont pas toujours utiles. Par exemple, *mp3* fait référence à un format d’encodage (MPEG-1 Audio Layer 3) et à un format de fichier.

Toutefois, la distinction est importante, car la lecture d’un fichier multimédia implique en fait deux étapes :

1.  Tout d’abord, le conteneur doit être analysé. Dans la plupart des cas, le nombre de flux et le format de chaque flux ne peuvent pas être connus tant que cette étape n’est pas terminée.
2.  Ensuite, si les flux sont compressés, ils doivent être décodés à l’aide des décodeurs appropriés.

Ce fait est très naturellement une conception logicielle dans laquelle des composants distincts sont utilisés pour analyser les conteneurs et décoder les flux. En outre, cette approche se prête à un modèle de plug-in, de sorte que les tiers peuvent fournir leurs propres analyseurs et codecs. sur Windows, le modèle COM (component Object Model) fournit un moyen standard de séparer une API de son implémentation, qui est une exigence pour tout modèle de plug-in. Pour cette raison (entre autres), Media Foundation utilise des interfaces COM.

Le diagramme suivant montre les composants utilisés pour lire un fichier multimédia :

![Diagramme montrant les composants pour lire un fichier multimédia](images/concepts02.png)

L’écriture d’un fichier multimédia nécessite également deux étapes :

1.  Encodage des données audio/vidéo non compressées.
2.  Placer les données compressées dans un format de conteneur particulier.

Le diagramme suivant montre les composants utilisés pour écrire un fichier multimédia :

![Diagramme montrant les composants pour l’écriture d’un fichier multimédia.](images/concepts03.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 



