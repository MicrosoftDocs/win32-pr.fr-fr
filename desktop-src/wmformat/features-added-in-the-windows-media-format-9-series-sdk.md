---
title: fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media Format 9 Series
description: fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media Format 9 Series
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows Media Format SDK, fonctionnalités
- Windows Media Format SDK, nouvelles fonctionnalités
- Windows Media Format SDK, lecteurs synchrones
- Windows Kit de développement logiciel (SDK) Media format, indexation basée sur des trames
- Windows Media Format SDK, codes temporels SMPTE
- Windows kit de développement logiciel (SDK) Media Format, filtres DirectShow
- Windows Media Format SDK, fonctionnalité d’écriture DRM
- Windows Media Format SDK, récepteurs de fichiers
- Windows Media Format SDK, DirectX Video Acceleration (DXVA)
- Windows Media Format SDK, audio multicanal
- Windows Media Format SDK, filigrane
- Windows Media Format SDK, prise en charge de plusieurs langues
- Windows Media Format SDK, modèles de conformité des appareils
- Windows Media Format SDK, énumérations de codec
- Windows Media Format SDK, exclusion mutuelle
- Windows Kit de développement logiciel (SDK) Media format, à débit binaire multiple (MBR)
- Windows Media Format SDK, transcodage avec la recompression intelligente
- Windows Media Format SDK, recompression intelligente
- Windows Media Format SDK, recompression
- Windows Media Format SDK, métadonnées
- Windows Media Format SDK, proportions de pixels dynamiques
- Windows Media Format SDK, flux vidéo entrelacés
- Windows Media Format SDK, encodage en deux passes
- Windows Media Format SDK, WMStub. lib
- lecteurs synchrones, à propos de
- indexation basée sur des frames
- Codes temporels SMPTE, à propos de
- filtres de DirectShow
- récepteurs de fichiers, améliorations
- audio multicanal, à propos de
- filigrane, à propos de
- codecs, énumérations
- exclusion mutuelle, à propos de
- gestion des droits numériques (DRM), capacité d’écriture
- DRM (gestion des droits numériques), capacité d’écriture
- DirectX Video Acceleration (DXVA), à propos de
- DXVA (DirectX Video Acceleration), à propos de
- ASF (Advanced Systems Format), prise en charge de plusieurs langues
- ASF (Advanced Systems Format), prise en charge de plusieurs langues
- débit binaire multiple (MBR), à propos de
- MBR (vitesses de transmission multiples), à propos de
- transcodage avec recompression intelligente
- recompression intelligente
- recompression
- métadonnées, Windows Media Format SDK
- proportions de pixels dynamiques
- flux vidéo entrelacés
- encodage en deux passes, à propos de
- 2-encodage Pass, à propos de
- WMStub. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76dc0f4a8c0b23ba33409039ae7f1d46ada1b3299790ef82fb98b8714f616117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547449"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a>fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media Format 9 Series

le kit de développement logiciel (SDK) Windows Media Format 9 Series a introduit de nombreuses améliorations et fonctionnalités. Cette section fournit une vue d’ensemble de ces fonctionnalités pour les utilisateurs qui migrent à partir d’une version antérieure du kit de développement logiciel (SDK).

## <a name="synchronous-reading"></a>Lecture synchrone

Vous pouvez lire des fichiers ASF avec des appels synchrones. Lors de la lecture d’un fichier de façon synchrone, vous pouvez modifier les paramètres du lecteur pendant sa lecture. Les opérations de lecture synchrones du kit de développement logiciel (SDK) ne prennent pas en charge la lecture des fichiers sur Internet, mais vous pouvez utiliser l’interface COM standard, **IStream**, pour lire à partir de sources personnalisées.

## <a name="frame-based-indexing"></a>Indexation basée sur des frames

Vous pouvez indexer des fichiers ASF basés sur des images vidéo. Le lecteur et le lecteur synchrone peuvent rechercher un frame d’un flux vidéo et synchroniser les autres flux avec ce frame.

## <a name="indexing-and-seeking-with-smpte-time-code"></a>Indexation et recherche avec le code temporel SMPTE

le kit de développement logiciel (SDK) Windows Media Format vous permet de stocker des codes temporels SMPTE dans des fichiers ASF. Les fichiers peuvent être indexés par code temporel SMPTE, et le lecteur asynchrone et le lecteur synchrone peuvent rechercher des entrées d’index de code temporel SMPTE.

## <a name="directshow-filters"></a>DirectShow Filtres

le kit de développement logiciel (SDK) Windows Media Format comprend deux filtres Microsoft DirectShow® qui permettent aux applications basées sur DirectShow de lire et d’écrire des fichiers ASF. DirectShow permet également aux applications de capturer des données à partir de périphériques audio et de décompresser des données à partir de différents formats avant de les encoder en tant que contenu multimédia Windows.

## <a name="enhanced-profiles"></a>Profils améliorés

Les profils peuvent contenir des informations de partage de bande passante et des informations de hiérarchisation de flux. Le partage de bande passante vous permet de spécifier que deux flux ou plus, indépendamment de leurs vitesses de transmission individuelles, n’utiliseront jamais plus d’une quantité de bande passante spécifiée. Les données de partage de bande passante dans un profil sont purement informatifs. elle n’est pas appliquée par aucune logique dans le kit de développement logiciel (SDK). La hiérarchisation des flux vous permet de spécifier un ordre de priorité pour les flux dans un profil. S’il n’y a pas suffisamment de bande passante lors de la lecture pour diffuser correctement le fichier, les flux de priorité les plus bas peuvent être ignorés afin d’améliorer les performances.

## <a name="drm-writing-capability"></a>Fonctionnalité d’écriture DRM

en plus de la prise en charge de la lecture DRM existante, le kit de développement logiciel (SDK) de la série Media Format 9 a ajouté Windows la prise en charge de l’écriture de fichiers ASF avec la protection drm version 1 ou drm version 7. Cette nouvelle fonctionnalité permet des scénarios « DRM en direct », tels que la diffusion en continu à l’affichage de la diffusion d’événements sportifs ou de concerts en direct.

## <a name="enhanced-file-sink"></a>Récepteur de fichiers amélioré

Plusieurs nouvelles fonctionnalités de récepteur de fichiers ont été ajoutées à la version 9 Series du kit de développement logiciel (SDK). Vous pouvez configurer le récepteur de fichiers pour désactiver l’indexation automatique des fichiers ASF nouvellement créés. Vous avez également la possibilité de le configurer pour l’entrée et la sortie non mises en mémoire tampon.

## <a name="directx-video-acceleration"></a>Accélération vidéo DirectX

DirectX Video Acceleration (DXVA) est une technologie qui permet la lecture d’une vidéo à débit élevé (qualité DVD ou meilleure) sur des machines moins puissantes avec des cartes graphiques compatibles DXVA. Vous pouvez utiliser l’objet lecteur de ce kit de développement logiciel (SDK) pour activer l’accélération vidéo DirectX, si le matériel le prend en charge, lors de la lecture de fichiers ASF.

## <a name="multichannel-audio"></a>Audio multicanal

Vous pouvez encoder et lire de l’audio multicanal. le codec Windows Media Audio 9 Professional prend en charge les formats avec 6 canaux et 8 canaux, ainsi que le stéréo haute définition.

## <a name="watermarking"></a>Le filigranage

Vous pouvez encoder des fichiers ASF avec des filigranes numériques pour la sécurité. Tous les systèmes de filigrane sont différents dans leur approche, mais ils incorporent tous l’identification dans le contenu encodé. Le filigrane est effectué à l’aide d’objets DMOs Media et® DirectX tiers spéciaux.

## <a name="support-for-multiple-languages-in-asf-files"></a>Prise en charge de plusieurs langues dans les fichiers ASF

Vous pouvez prendre en charge plusieurs langues dans des fichiers ASF, à la fois dans les flux et dans les métadonnées. Par exemple, vous pouvez créer un fichier vidéo avec des flux audio dans plusieurs langues. Lors de la lecture, l’utilisateur peut sélectionner la langue à utiliser, ou votre application peut interroger les informations système sur l’ordinateur en train de jouer et sélectionner une langue automatiquement. Les attributs de métadonnées peuvent également être entrés plusieurs fois, avec les valeurs dans des langues différentes.

## <a name="device-conformance-templates"></a>Modèles de conformité des appareils

pour faciliter le ciblage du contenu sur des appareils clients spécifiques, les codecs multimédias Windows prennent désormais en charge les modèles de conformité des appareils. Chaque modèle contient une plage de paramètres définie et des fonctionnalités de codec qui doivent être utilisées pour les médias destinés à une catégorie particulière de plateformes. les profils système ne sont plus pris en charge avec les dernières versions des codecs de média Windows. Tous les profils doivent être personnalisés en fonction de vos besoins. Vous pouvez utiliser des modèles de conformité des appareils pour vous aider à concevoir vos profils.

## <a name="expanded-codec-enumeration"></a>Énumération de codec développée

l’objet gestionnaire de profils peut interroger les codecs vidéo et Windows Media Audio pour les formats pris en charge. Vous pouvez définir des paramètres pour les formats récupérés. par exemple, vous pouvez récupérer tous les formats de taux de bits variables basés sur la qualité pris en charge par le codec Windows Media Audio 9.

## <a name="improved-mutual-exclusion"></a>Exclusion mutuelle améliorée

Vous pouvez créer des enregistrements nommés contenant plusieurs flux dans un objet d’exclusion mutuelle. Vous pouvez également nommer des objets d’exclusion mutuelle pour faciliter leur identification. Cela vous permet de créer des couches d’exclusion mutuelle. Par exemple, un fichier peut contenir des flux qui sont mutuellement exclusifs par vitesse de transmission et par langue. L’exclusion mutuelle basée sur le langage implique des groupes de flux, chaque groupe constitué de flux dans la même langue mais mutuellement exclusifs par vitesse de transmission.

## <a name="expanded-multiple-bit-rate-support"></a>Prise en charge de plusieurs vitesses de transmission

La prise en charge de l’exclusion mutuelle est incluse pour l’audio à débit binaire multiple (MBR) et pour la vidéo avec des flux de différentes tailles d’image.

## <a name="attributes-for-streams"></a>Attributs pour Flux

Vous pouvez affecter des attributs à des flux individuels dans des fichiers ASF. Vous devez toujours utiliser des attributs de niveau fichier pour les fichiers MP3. Cette fonctionnalité n’ajoute aucune méthode au kit de développement logiciel (SDK), mais les méthodes existantes acceptent désormais des numéros de flux autres que zéro.

## <a name="transcoding-with-smart-recompression"></a>Transcodage avec recompression intelligente

la recompression intelligente vous permet de transcoder des fichiers audio Windows Media à partir d’un débit élevé vers une vitesse de transmission inférieure, avec une meilleure qualité que précédemment réalisable.

## <a name="expanded-metadata-support"></a>Prise en charge des métadonnées étendues

le kit de développement logiciel (SDK) Windows Media Format fournit les nouvelles fonctionnalités de métadonnées suivantes :

-   Balises de métadonnées basées sur l’index, permettant l’activation de plusieurs balises portant le même nom.
-   Possibilité de lire les attributs d’en-tête DRM sans fichier WMStubDRM. lib.
-   Attributs avec plus de 64 kilo-octets de données associées.
-   Attributs dans plusieurs langues.
-   Des dizaines de nouveaux attributs prédéfinis.

## <a name="dynamic-pixel-aspect-ratio"></a>Proportions de pixels dynamiques

Les flux vidéo composés de différents types de contenu peuvent être pris en compte en identifiant les proportions de pixels des exemples disparates dans le flux. Cela permet à l’application de jouer de fournir une meilleure lecture de ce contenu.

## <a name="interlaced-video-streams"></a>Flux vidéo entrelacée

les versions précédentes du kit de développement logiciel (SDK) Windows Media Format ont permis de coder le contenu [*entrelacé*](wmformat-glossary.md) en un flux vidéo d’analyse progressive. à partir du kit de développement logiciel (SDK) Windows Media Format 9 Series, vous pouvez encoder une vidéo entrelacée tout en conservant son Format entrelacé. Cela peut entraîner une amélioration de la lecture, en particulier sur les appareils entrelacés, tels que les groupes de télévision.

## <a name="two-pass-encoding"></a>Encodage Two-Pass

le nouveau Windows codecs multimédias active l’encodage en deux passes. Le contenu encodé en deux passes peut obtenir une sortie de qualité supérieure.

## <a name="new-speech-codec"></a>Nouveau codec vocal

ce kit de développement logiciel (SDK) comprend le nouveau codec vocal Windows Media Audio 9 qui est optimisé pour l’encodage de la voix humaine tout en utilisant un faible taux de bits. Ce codec offre également des performances supérieures pour le contenu mixte musical-Voice.

## <a name="accessible-video-frame-duration"></a>Durée de l’image vidéo accessible

Vous pouvez faire en sorte que l’objet writer de ce kit de développement logiciel (SDK) fournisse la durée des images vidéo au lecteur.

## <a name="streaming-html"></a>Streaming HTML

Avec la version précédente de ce kit de développement logiciel (SDK), vous avez pu utiliser une commande de script pour signaler à votre application d’ouvrir une page Web. à compter du kit de développement logiciel (SDK) Windows Media Format 9 Series, vous pouvez stocker les composants des pages Web dans vos fichiers ASF pour vous assurer qu’il n’y a aucun décalage dans les présentations.

## <a name="wmstublib-no-longer-required-for-build-environment"></a>WMStub. lib n’est plus nécessaire pour l’environnement de génération

les paramètres d’environnement de génération pour le kit de développement logiciel (sdk) de format multimédia Windows modifiés à compter du kit sdk Windows media format 9 Series. Vous n’avez plus besoin d’inclure WMStub. lib pour les applications utilisant ce kit de développement logiciel (SDK). Toutefois, les applications compatibles DRM doivent toujours obtenir et signer un contrat de licence distinct, et obtenir une bibliothèque statique unique auprès de Microsoft. wmla@microsoft.comPour plus d’informations sur la bibliothèque DRM et le contrat de licence, contactez. pour plus d’informations sur la génération de projets avec ce kit de développement logiciel (SDK), consultez [fichiers de bibliothèque et Paramètres du compilateur](library-files-and-compiler-settings.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**à propos du kit de développement logiciel (SDK) Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




