---
title: copie Flux sans décompression des données
description: copie Flux sans décompression des données
ms.assetid: c268ce44-a09d-4304-bc39-8b6657da2bdb
keywords:
- Windows Media Format SDK, copie de flux
- ASF (Advanced Systems Format), copie de flux
- ASF (format de systèmes avancés), copie de flux
- flux, copier sans décompresser les données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831b85ad431a6c4d3f4255c281d22ca17004674f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294471"
---
# <a name="copying-streams-without-decompressing-the-data"></a>copie Flux sans décompression des données

La méthode la plus simple et la plus courante pour copier un flux d’un fichier vers un autre consiste à récupérer les exemples dans leur état compressé, puis à les écrire dans le nouveau fichier sans les décompresser et les recompresser. Les exemples obtenus à partir d’un fichier dans leur état compressé sont appelés exemples de flux, car ils ne sont pas modifiés par rapport à leur représentation dans le flux. Il est recommandé de toujours utiliser des exemples de flux pour copier des flux, car la décompression et la recompression des données multimédias numériques dégradent la qualité. si vous devez copier un flux à partir de données décompressées, consultez [copie d’Flux à l’aide d’exemples décompressés](copying-streams-using-decompressed-samples.md).

Il est possible de concaténer deux ou plusieurs flux en un seul flux à l’aide d’exemples compressés, mais uniquement si les vitesses de transmission sont identiques. Le processus est fondamentalement le même que les étapes décrites ci-dessous, sauf que vous devez lire plusieurs fichiers originaux pour obtenir tout le contenu dont vous avez besoin. Toutefois, vous pouvez uniquement écrire des exemples compressés à partir de plusieurs fichiers dans un seul flux si les structures de **\_ \_ type de média WM** (y compris tous les membres de la structure **pbFormat** ) de tous les flux compressés sont identiques. Pour combiner des données provenant de plusieurs flux qui ne sont pas du même format, vous devez décompresser le contenu et le recompresser dans le flux de destination. En outre, lorsque vous combinez des données de deux ou plusieurs flux en un seul flux, vous devez ajouter les valeurs de fenêtre de mémoire tampon pour tous les flux afin d’obtenir la fenêtre de mémoire tampon pour le nouveau flux. Cela est dû au fait qu’il est impossible de déterminer la quantité de mémoire tampon qui est prise à la fin d’un flux de données et au début d’un autre.

Vous pouvez récupérer des exemples de flux avec le lecteur asynchrone à l’aide de [**IWMReaderAdvanced :: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples). Les exemples de flux sont remis à [**IWMReaderCallbackAdvanced :: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample), et non à [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Si vous lisez un fichier et récupérez des flux compressés et des fichiers décompressés, vous devez implémenter les deux méthodes de rappel.

Le lecteur synchrone offre plus de souplesse pour la récupération des exemples. Vous pouvez basculer librement entre les exemples compressés et compressés pendant la lecture à l’aide de [**IWMSyncReader :: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples).

Pour copier l’intégralité d’un flux d’un fichier ASF dans un nouveau fichier ASF, procédez comme suit. Ces étapes utilisent le lecteur synchrone, car il est bien plus simple à utiliser pour ce type d’opération.

1.  Créez un objet lecteur synchrone en appelant la fonction [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) .
2.  Ouvrez un fichier dans le lecteur à l’aide d’un appel à [**IWMSyncReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).
3.  Obtenir un pointeur vers l’interface [**IWMProfile**](iwmprofile.md) de l’objet lecteur synchrone en appelant **IWMSyncReader :: QueryInterface**.
4.  Récupérez les propriétés du flux souhaité en appelant [**IWMProfile :: GetStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber). Cela permet de récupérer un pointeur vers l’interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) de l’objet de configuration de flux pour le flux de votre choix.
5.  Obtient une copie de la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) pour le flux. Effectuez deux appels à [**IWMMediaProps :: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype): la première pour récupérer la taille de la structure, la seconde pour récupérer la structure elle-même.
6.  Créez un objet de gestionnaire de profils en appelant la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
7.  Appelez [**IWMProfileManager :: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) pour créer un nouveau profil (ou ouvrez un profil existant auquel vous souhaitez ajouter le flux). Appelez [**IWMProfile :: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) sur le nouveau profil pour ajouter le flux à partir du fichier existant. Lors de l’ajout du flux, utilisez le pointeur **IWMStreamConfig** obtenu à l’étape 4.
8.  Créez un objet Writer avec un appel à la fonction [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . Définissez le profil nouvellement créé en tant que profil actif dans le writer en appelant [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). Créez un fichier pour la sortie en appelant [**IWMWriter :: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).
9.  Pour chaque entrée associée au flux ou aux flux que vous copiez, appelez [**IWMWriter :: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops), en passant la **valeur null** pour l’interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) . Cela informe l’objet Writer qu’il n’a pas besoin de valider les données que vous passez. Vous devez effectuer cet appel avant d’appeler **BeginWriting** (étape 14); dans le cas contraire, un objet de lecture peut ne pas être en mesure de décoder le contenu.
10. Définissez le lecteur synchrone pour fournir des exemples de flux compressés pour le flux sélectionné en appelant [**IWMSyncReader :: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) avec le paramètre *FCompressed* défini sur true.
11. Obtenez des informations de codec pour chaque flux en cours de copie et ajoutez les informations du codec à l’en-tête avant d’écrire. Pour obtenir les informations du codec, appelez [**IWMHeaderInfo2 :: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) et [**IWMHeaderInfo2 :: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) pour énumérer les codecs associés au fichier dans le lecteur. Sélectionnez les informations du codec qui correspondent à la configuration du flux. Définissez ensuite les informations du codec dans le writer en appelant [**IWMHeaderInfo3 :: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), en passant les informations obtenues à partir du lecteur.
12. Obtenez un pointeur vers l’interface [**IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced) en appelant **IWMWriter :: QueryInterface**.
13. Définissez le writer en mode d’écriture en appelant [**IWMWriter :: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).
14. Effectuez des appels répétés à [**IWMSyncReader :: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample), en spécifiant le numéro de flux souhaité. Lorsque des exemples sont reçus, transmettez-les au writer avec des appels à [**IWMWriterAdvanced :: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample). Pour les flux vidéo, vous devez vérifier les indicateurs (le cas échéant) définis par le writer sur chaque appel à **GetNextSample**. Si WM \_ DF \_ CLEANPOINT est défini, vous devez également le définir sur votre appel à **WriteStreamSample**.
15. Une fois la lecture terminée, appelez [**IWMWriter :: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting). Le flux doit être transféré.

> [!Note]  
> Les flux d’images ne peuvent pas être copiés d’un fichier à un autre à l’aide d’exemples de flux. Pour copier des données de flux d’image, récupérez les exemples non compressés, puis traitez-les par le biais du writer comme vous le feriez normalement.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Copie de données d’un fichier vers un autre**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**copie Flux à l’aide d’exemples décompressés**](copying-streams-using-decompressed-samples.md)
</dt> </dl>

 

 




