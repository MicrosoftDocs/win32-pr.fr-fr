---
description: Cette rubrique décrit quand et comment utiliser un récepteur MFT et MP4 REMUX H. 264/AVC.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Quand et comment utiliser H. 264/AVC REMUX MFT et le récepteur MP4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ce5b6d63a21e7a9d6b75acd29690cdeaeba5b0105dcf8d45fe0c93e6b768f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357949"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Quand et comment utiliser H. 264/AVC REMUX MFT et le récepteur MP4

Cette rubrique décrit quand et comment utiliser un récepteur MFT et MP4 REMUX H. 264/AVC.

## <a name="when-to-use-h264avc-remux-mft"></a>Quand utiliser H. 264/AVC REMUX MFT

Le format de fichier MPEG-4 requiert que chaque exemple compressé contienne une image principale avec des unités NAL dans le bon ordre. (Reportez-vous à la définition de l’image principale et à l’ordre des unités NAL obligatoires dans la section 7.4.1.2.3, **ordre des unités nal et des images codées et Association aux unités d’accès**, de la spécification AVC H. 264.) Elle requiert également que chaque exemple compressé soit associé à un horodatage de présentation, un horodatage de décodage et une durée d’échantillonnage.

Dans de nombreux scénarios, lorsque les applications doivent enregistrer la vidéo H. 264/AVC dans un conteneur de fichiers MPEG-4, l’exemple compressé peut ne pas répondre aux exigences ci-dessus. Par exemple, il se peut qu’un exemple compressé ne contienne pas d’image principale complète ou qu’il ne soit pas associé à un horodatage de présentation correct. Voici quelques exemples d’applications :

-   Écrire une vidéo élémentaire de streaming H. 264/AVC dans un conteneur de fichiers MPEG-4.
-   Enregistrement caméra capture d’une vidéo élémentaire H. 264/AVC dans le conteneur de fichiers MPEG-4.
-   Enregistrez la conférence vidéo H. 264/AVC dans le conteneur de fichiers MPEG-4.
-   Concaténez deux vidéos H. 264/AVC dans MPEG-2 TS ou MP4 et écrivez dans le conteneur de fichiers MPEG-4 avec des horodatages corrects.
-   Vidéo REMUX H. 264/AVC à partir du format de fichier AVCHD, MPEG-2 TS/PS au format de fichier MPEG-4.
-   Découpez le fichier vidéo H. 264/AVC sans transcodage.

Dans ce cas, l’application doit utiliser une table MFT REMUX H. 264/AVC pour convertir les exemples compressés qui ne contiennent pas d’image principale complète avant qu’ils ne soient écrits dans le conteneur de fichiers MPEG-4.

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Comment utiliser H. 264/AVC REMUX MFT et le récepteur MP4

Définissez le type de média de sortie source sur **MFVideoFormat \_ H264 – \_ es**, ce qui indique que chaque exemple ne peut pas contenir une image principale complète. Définissez le type de média d’entrée du récepteur MP4 sur **MFVideoFormat \_ H264 –**. Par conséquent, le type de média d’entrée de la MFT H. 264/AVC REMUX est **MFVideoFormat \_ H264 – \_ es** et le type de support de sortie de la MFT h. 264/AVC REMUX est **MFVideoFormat \_ H264 –**, qui sera automatiquement inséré dans le programme de résolution de topologie.

La durée de l’échantillon est ignorée par le H. 264/AVC REMUX, car la durée de l’échantillon pour un exemple ne contenant pas d’image principale complète n’a pas de signification claire. Au lieu de cela, la durée de l’échantillon est calculée à partir de la fréquence d’images. La fréquence d’images est calculée à partir du paramètre Sequence. Si les informations n’existent pas dans le paramètre Sequence, la fréquence d’images est calculée à partir des paramètres du type de média d’entrée. Si les informations de fréquence d’images ne sont pas disponibles, la fréquence d’images par défaut de 29,97 fps est utilisée.

H. 264/AVC REMUX MFT interpole de manière linéaire les horodatages de décodage pour chaque image compressée en fonction de la fréquence d’images. H. 264/AVC REMUX MFT honore les horodatages de présentation d’entrée (PTS) dans les exemples d’entrée et les transmet à la sortie s’ils existent. Il effectue une interpolation PTS en fonction de la fréquence d’images, de la PTS précédente et de l’ordre de sortie des images par le biais du processus de mise en mémoire tampon des images décodées (DBP), comme indiqué dans **l’annexe C.** point de vue du détourage de la spécification AVC H. 264. Chaque échantillon de sortie de la MFT H. 264/AVC REMUX doit avoir des PTS, DTS et Sample Duration. H. 264/AVC REMUX MFT identifie également les images de m dans le flux binaire et les définit comme point de nettoyage avec l’attribut MF de [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md).

Actuellement, la MFT H. 264/AVC REMUX peut gérer un maximum de 64 frame de réorganisation. Si le nombre de frames réorganisés dépasse 64 avec un cadre de référence à long terme, la MFT H. 264/AVC REMUX effectue l’interpolation d’une PTS erronée pour ce frame et génère cette trame à un moment incorrect.

Pour instancier une table MFT REMUX H. 264/AVC, définissez les types de médias d’entrée et de sortie corrects sur la MFT H. 264/AVC REMUX, définissez le type de média d’entrée pour le récepteur MP4 et résolvez la topologie.

L’exemple de code suivant montre comment initialiser le récepteur MFT. 264/AVC REMUX.

Pour la MFT H. 264/AVC REMUX,


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



Aucune autre configuration n’est nécessaire.

Pour le récepteur MP4,


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Formats multimédias pris en charge dans Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



