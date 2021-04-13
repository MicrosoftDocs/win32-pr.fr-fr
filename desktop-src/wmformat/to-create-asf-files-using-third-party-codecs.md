---
title: Pour créer des fichiers ASF à l’aide de codecs tiers
description: Pour créer des fichiers ASF à l’aide de codecs tiers
ms.assetid: 5cd348ca-1f86-429d-92ee-4eab4ced8571
keywords:
- Windows Media Format SDK, création de fichiers ASF
- Windows Media Format SDK, codecs tiers
- ASF (Advanced Systems Format), création de fichiers
- ASF (format des systèmes avancés), création de fichiers
- Formats ASF (Advanced Systems Format) et codecs tiers
- ASF (format de systèmes avancés), codecs tiers
- codecs tiers
- codecs, tiers
- codecs, création de fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6c057f1785ed50e328ac6094ff7dbe078e98fc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314504"
---
# <a name="to-create-asf-files-using-third-party-codecs"></a>Pour créer des fichiers ASF à l’aide de codecs tiers

Vous pouvez utiliser le kit de développement logiciel (SDK) Windows Media format pour créer des fichiers ASF qui contiennent des médias numériques encodés avec n’importe quel codec de votre choix. Lorsque vous utilisez un codec autre que celui inclus dans ce kit de développement logiciel (SDK), vous devez effectuer les étapes suivantes.

1.  Encodez le contenu avec le codec souhaité.
2.  Recherchez ou créez une valeur GUID pour identifier le contenu encodé avec le codec utilisé à l’étape 1.
3.  Créez un nouveau profil ou modifiez un profil existant pour l’utiliser avec le contenu encodé.
    -   Créez un flux pour le contenu encodé avec le type principal approprié. Pour plus d’informations sur les principaux types de médias, consultez [types de médias](media-types.md). Utilisez le GUID identifié à l’étape 2 comme sous-type de média.
    -   Définissez la vitesse de transmission et la fenêtre de mémoire tampon pour le flux sur des valeurs qui n’entraînent pas un dépassement de mémoire tampon. Vous devez être en mesure d’obtenir ces valeurs à partir du codec au moment de l’encodage. Les composants d’exécution du kit de développement logiciel (SDK) vérifient les valeurs des fenêtres binaires/de mémoire tampon et déposent les échantillons si nécessaire pour que les données spécifiées tiennent compte de ces valeurs. Si vous définissez les valeurs de manière incorrecte, le fichier n’est pas correctement diffusé, ce qui entraîne une mauvaise lecture.
    -   Pour les flux vidéo, vous devez définir le membre de **bicompression** de la structure **BITMAPINFOHEADER** contenue dans la structure [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) sur la valeur FourCC appropriée pour le contenu. Cette valeur doit être égale aux quatre premiers octets du GUID de sous-type. Par exemple, si la **compression** est MAKEFOURCC (« t », « E », « t ») = 0x54455354, le GUID de sous-type commencera comme suit : 54455354-XXXX-XXXX-xxxx-xxxxxxxxxxxx.
4.  Créez un objet Writer et chargez le profil créé à l’étape précédente. Pour plus d’informations sur l’écriture de fichiers, consultez [écriture de fichiers ASF](writing-asf-files.md).
5.  Parcourez les entrées du fichier et affectez des propriétés d’entrée pour chaque comme vous le feriez normalement. Pour plus d’informations sur les entrées, consultez [utilisation des entrées](working-with-inputs.md). Pour le flux encodé à l’aide d’un codec tiers, définissez le pointeur d’interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) sur la **valeur null** avant d’appeler [**IWMWriter :: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).
6.  Utilisez le nouveau profil créé à l’étape précédente pour écrire le fichier. Transmettez les exemples compressés à l’aide de [**IWMWriterAdvanced :: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) au lieu de [**IWMWriter :: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Pour la vidéo, vous devez spécifier les exemples qui sont des images clés en passant WM \_ DF \_ CLEANPOINT comme paramètre *dwFlags* .

Pour traiter et décompresser le flux encodé à l’aide d’un codec tiers, vous devez lire les exemples de flux compressés. Votre application de lecture doit également gérer l’exemple de décompression du flux.

## <a name="putting-mpeg-2-streams-into-asf"></a>Placer des flux MPEG-2 dans ASF

> [!Note]  
> Cette rubrique s’applique aux applications qui utilisent le kit de développement logiciel (SDK) Windows Media format pour placer MPEG-2 (ou d’autres formats de compression qui utilisent des frames B) dans le conteneur de fichiers ASF.

 

L’objet Writer requiert que tous les échantillons d’entrée aient des horodatages, et il suppose que chaque exemple d’entrée a une durée de présentation ultérieure à celle qui l’a précédé. Si pratiquement toutes les vidéos non compressées et même certains flux vidéo compressés remplissent ces conditions, les flux MPEG-2 ne le font pas. Dans MPEG-2, tous les échantillons ne sont pas horodatés et, lorsque les frames B sont présents, l’exemple de décodage est différent de l’ordre de rendu. Lorsque l’objet Writer rencontre des exemples non ordonnés, il les réorganise dans l’ordre « correct ». Par conséquent, pour stocker des flux MPEG-2 en mode natif (non décodés) dans un conteneur ASF, vous devez effectuer les étapes suivantes :

Lors de l’écriture du fichier :

1.  Ajoutez une extension d’unité de données de taille fixe (DUE) à chaque exemple d’entrée qui contiendra une structure contenant les valeurs de temps et d’heure de début et d’heure de début MPEG réelles de l’exemple. Utilisez-1 pour ces valeurs si l’exemple n’a pas d’horodatage.
2.  Donnez aux objets d’enregistreur des horodateurs d’entrée « factices » qui s’améliorent toujours afin qu’ils écrivent les exemples dans le fichier exactement dans le même ordre que celui dans lequel ils sont reçus. Les horodatages factices doivent correspondre approximativement aux durées de présentation réelles, en moyenne dans le temps. Les horodatages factices forment la chronologie de recherche. par conséquent, s’ils divergent par rapport aux horodatages en temps réel, les opérations de recherche sur le fichier produisent des résultats inattendus. Toutefois, une quantité limitée d’instabilité entre les temps d’échantillonnage n’affectera pas sérieusement les opérations de recherche.

Lors de la lecture du fichier :

-   Pour chaque exemple lu à partir du fichier, examinez le dû. S’il contient une heure de début supérieure ou égale à zéro, copiez cette valeur sur l’horodatage de l’échantillon de sortie avant qu’il ne soit remis au décodeur. Affectez à tous les autres horodatages sur les échantillons de sortie la **valeur null**. Dans DirectShow, cette opération est effectuée en appelant **IMediaSample :: setTime**(**null**,**null**).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Mise en mémoire tampon du contenu**](buffering-content.md)
</dt> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Interface IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Pour distribuer des exemples compressés avec le lecteur asynchrone**](to-deliver-compressed-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Pour récupérer des exemples de flux avec le lecteur synchrone**](to-retrieve-stream-samples-with-the-synchronous-reader.md)
</dt> <dt>

[**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)
</dt> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




