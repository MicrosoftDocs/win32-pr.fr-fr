---
title: Écriture de fichiers ASF
description: Écriture de fichiers ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Media Format SDK, écriture de fichiers ASF
- Windows Media Format SDK, création de fichiers ASF
- Windows Media Format SDK, ASF (Advanced Systems Format)
- ASF (Advanced Systems Format), écriture de fichiers
- ASF (format de systèmes avancés), écriture de fichiers
- ASF (Advanced Systems Format), création de fichiers
- ASF (format des systèmes avancés), création de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4bec466a9f38dfedaa7e860fdc5e3eda56e0ca5fa1f1240bc18c54dfd51513
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590619"
---
# <a name="writing-asf-files"></a>Écriture de fichiers ASF

vous pouvez utiliser l’objet writer du kit de développement logiciel (SDK) de Format multimédia Windows pour créer des fichiers ASF à partir de données multimédias numériques. Pour créer une instance de l’objet Writer, appelez la fonction [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . l’objet writer coordonne les fonctionnalités d’un certain nombre de composants, y compris les codecs, qui sont externes au kit de développement logiciel (SDK) de Format multimédia Windows.

Les fonctionnalités de base de l’objet Writer peuvent être décomposées selon les étapes suivantes. dans ces étapes, « l’application » fait référence au programme que vous écrivez à l’aide du kit de développement logiciel (SDK) de Format multimédia Windows.

1.  L’application fournit à l’enregistreur un profil à utiliser pour créer le fichier ASF. Lorsque l’enregistreur charge les données de profil, il attribue un numéro d’entrée à chaque connexion du profil.
2.  L’application fournit au writer un nom de fichier de sortie pour le fichier à écrire. L’enregistreur crée un objet récepteur de fichiers de Writer pour gérer la création et l’entrée de fichier. Pour plus d’informations, consultez [objet récepteur de fichiers](writer-file-sink-object.md)de l’enregistreur.
3.  L’enregistreur crée un en-tête pour le nouveau fichier en fonction des informations contenues dans le profil.
4.  L’application transmet des exemples non compressés au writer. Les exemples sont passés un par un dans des mémoires tampons encapsulées dans des objets de mémoire tampon. L’application doit transmettre simultanément des exemples pour chaque flux afin que le writer reçoive tous les exemples dans l’ordre de la présentation.
5.  Le writer passe les exemples au codec approprié pour la compression. Lorsque l’enregistreur reçoit les exemples compressés, il les entrelace avec des échantillons des autres flux afin que les exemples entrent dans le fichier dans l’ordre chronologique des présentations, quel que soit le flux. Les exemples de données sont ensuite transformés en paquets et écrits dans la section de données du fichier.
6.  Lorsque tous les échantillons sont traités, le writer peut ajouter un index au fichier pour améliorer les performances de la recherche.

Ces étapes sont illustrées dans l’exemple d’application WMStats, entre autres. Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).

L’enregistreur prend également en charge des fonctionnalités plus avancées, ce qui vous permet d’effectuer les opérations suivantes :

-   Modifiez les métadonnées dans l’en-tête du fichier.
-   Écrire des exemples précompressés.
-   Écrire dans les récepteurs réseau pour la diffusion en continu des données actives.
-   Écrire dans les récepteurs de fichiers pour les options de contrôle de fichier avancées.
-   Écrire dans des récepteurs de notifications push pour la distribution aux serveurs qui fourniront du contenu aux utilisateurs finaux.
-   Fournissez des exemples postview pour la vérification de la sortie.
-   Fournir l’enregistreur-statistiques de performances.

Les sections suivantes décrivent en détail l’utilisation de l’objet Writer.



| Section                                                                    | Description                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Pour utiliser des profils avec l’auteur](to-use-profiles-with-the-writer.md)     | Décrit comment spécifier un profil à utiliser avec le writer.                                             |
| [Utilisation des entrées](working-with-inputs.md)                             | Décrit comment identifier et configurer les paramètres d’entrée dans le writer.                              |
| [Pour modifier des métadonnées avec le writer](to-edit-metadata-with-the-writer.md)   | Décrit comment utiliser le writer pour modifier les métadonnées d’un nouveau fichier.                                       |
| [Pour écrire des exemples](to-write-samples.md)                                   | Décrit comment passer des exemples au writer.                                                           |
| [Définition des extensions d’unité de données](setting-data-unit-extensions.md)           | Décrit comment ajouter des données étendues à des exemples.                                                         |
| [Écriture d’exemples compressés](writing-compressed-samples.md)               | Décrit comment passer des échantillons précompressés au writer.                                            |
| [Écriture d’une image Flux](writing-image-streams.md)                         | Décrit comment configurer une entrée pour un flux d’image.                                               |
| [Écriture d’exemples d’images vidéo](writing-video-image-samples.md)             | Décrit comment configurer des exemples d’images vidéo.                                                        |
| [Écriture d’une vitesse de transmission variable Flux](writing-variable-bit-rate-streams.md) | Décrit comment écrire des flux à débit binaire variable (VBR).                                                |
| [Utilisation de l’encodage Two-Pass](using-two-pass-encoding.md)                     | Décrit comment faire en sorte que le codec effectue une étape préliminaire avant d’écrire le fichier.                    |
| [Pour forcer l’insertion d' Key-Frame](to-force-key-frame-insertion.md)           | Décrit comment forcer manuellement le codec à encoder un exemple en tant qu’image clé.                           |
| [Pour gérer la latence de l’enregistreur](to-manage-writer-latency.md)                   | Décrit comment réduire le temps nécessaire au Writer pour traiter des exemples dans un fichier ou un récepteur de sortie. |
| [Utilisation des récepteurs d’écriture](working-with-writer-sinks.md)                 | Décrit comment utiliser des récepteurs d’enregistreur pour distribuer votre contenu à des fichiers ou à des emplacements réseau.               |
| [Pour connaître les statistiques de l’enregistreur](to-get-writer-statistics.md)                   | Décrit comment obtenir des statistiques pour l’enregistreur.                                                        |
| [Pour utiliser l’enregistreur Postview](to-use-writer-postview.md)                       | Décrit comment obtenir des exemples non compressés quand vous écrivez un fichier à des fins de vérification.                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> <dt>

[**Récepteur de fichiers d’auteur, objet**](writer-file-sink-object.md)
</dt> <dt>

[**Objet récepteur réseau de l’enregistreur**](writer-network-sink-object.md)
</dt> <dt>

[**Auteur, objet**](writer-object.md)
</dt> </dl>

 

 




