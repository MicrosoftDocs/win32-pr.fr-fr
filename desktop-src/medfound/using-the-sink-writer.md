---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Utilisation de l’enregistreur du récepteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951615"
---
# <a name="using-the-sink-writer"></a>Utilisation de l’enregistreur du récepteur

## <a name="overview"></a>Vue d’ensemble

### <a name="file-container-types"></a>Types de conteneurs de fichiers

L’enregistreur du récepteur offre une prise en charge intégrée de plusieurs types de conteneurs de fichiers. Pour obtenir une liste complète, consultez la page relative au [ \_ transcodage MF \_ CONTAINERTYPE](mf-transcode-containertype.md). Vous pouvez prendre en charge des types de conteneur supplémentaires en écrivant un [récepteur multimédia](media-sinks.md)personnalisé. Le conteneur de fichiers est spécifié lorsque vous créez une nouvelle instance du writer du récepteur.

### <a name="stream-formats"></a>Formats de flux

Pour chaque flux, l’application doit spécifier les éléments suivants.

-   Le format *d’entrée* est le format que l’application envoie à l’enregistreur du récepteur.
-   Le format de *sortie* est le format qui sera écrit dans le fichier.

Les formats d’entrée et de sortie peuvent être compressés ou non compressés. Le writer du récepteur prend en charge les combinaisons suivantes :

-   Entrée non compressée avec sortie compressée. C’est généralement le cas et est utilisé pour l’encodage ou le transcodage de scénarios. Un encodeur de Microsoft Media Foundation doit être disponible qui accepte le type d’entrée et encode le type de sortie.
-   Entrée compressée avec une sortie identique. Utilisez cette combinaison pour REMUX un fichier sans transcodage.
-   Entrée non compressée avec une sortie identique. Utilisez cette combinaison pour écrire du contenu audio ou vidéo non compressé dans un conteneur de fichiers.

L’enregistreur du récepteur ne prend pas en charge le redimensionnement vidéo, la conversion de la fréquence d’images ou le rééchantillonnage audio, sauf si ces fonctions sont fournies par l’encodeur. Dans le cas contraire, l’application peut utiliser des [processeurs de signaux numériques](windowsmediadigitalsignalprocessors.md) pour convertir les données d’entrée avant d’envoyer les données au

## <a name="creating-the-sink-writer"></a>Création du writer du récepteur

Il existe deux fonctions qui créent l’enregistreur du récepteur :

-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) prend l’URL d’un fichier de sortie ou un pointeur vers un flux d’octets. Cette fonction crée le récepteur multimédia en interne.
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) prend un pointeur vers un récepteur multimédia qui a déjà été créé par l’application.

Si vous utilisez l’un des récepteurs multimédias intégrés, la fonction [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) est préférable, car l’appelant n’a pas besoin de configurer le récepteur multimédia.

La méthode [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) fournit plusieurs options pour spécifier le type de conteneur de fichiers. Dans le cas le plus simple, la fonction utilise l’extension de nom de fichier dans l’URL pour sélectionner le conteneur de fichiers. Pour plus d’informations, reportez-vous à la page de référence des fonctions.

Par exemple, le code suivant spécifie le nom de fichier « output. wmv » pour l’URL. En fonction de l’extension de nom de fichier, l’enregistreur du récepteur chargera le [récepteur de média ASF](asf-media-sinks.md) pour créer un fichier ASF (Advanced Systems Format).


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



Dans le cas de [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), le type de fichier est déterminé par le récepteur multimédia.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistreur du récepteur](sink-writer.md)
</dt> </dl>

 

 



