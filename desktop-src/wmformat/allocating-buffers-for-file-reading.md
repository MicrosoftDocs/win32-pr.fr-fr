---
title: Allocation de tampons pour la lecture de fichiers
description: Allocation de tampons pour la lecture de fichiers
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- Windows Media Format SDK, lire des fichiers ASF
- Fichiers ASF (Advanced Systems Format), lecture des fichiers
- ASF (format des systèmes avancés), lire les fichiers
- Windows Media Format SDK, allouer des tampons
- ASF (Advanced Systems Format), allouer des tampons
- ASF (format de systèmes avancés), allouer des tampons
- ASF (Advanced Systems Format), allocation de mémoire tampon
- ASF (format de systèmes avancés), allocation de mémoire tampon
- allocation de mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381467"
---
# <a name="allocating-buffers-for-file-reading"></a>Allocation de tampons pour la lecture de fichiers

Dans le scénario de lecture de fichiers le plus basique, les mémoires tampons utilisées pour fournir des exemples sont allouées par l’objet de lecture (l’objet lecteur ou l’objet lecteur synchrone). Toutefois, vous pouvez allouer vous-même des tampons. Pour plus d’informations sur les avantages de l’allocation de vos propres tampons, consultez [prise en charge de l’exemple alloué](user-allocated-sample-support.md)par l’utilisateur.

Pour utiliser vos propres mémoires tampons pour la lecture de fichiers, procédez comme suit.

1.  Implémentez un rappel ou des rappels pour que le lecteur appelle lorsqu’il a besoin d’une mémoire tampon. Si vous lisez des exemples de sortie, utilisez [**IWMReaderAllocatorEx :: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex). Si vous lisez des exemples de flux, utilisez [**IWMReaderAllocatorEx :: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex). Incluez la logique de gestion des mémoires tampon adaptée à votre application.
2.  Allouez un pool de mémoires tampons que vous allez utiliser pour la lecture de fichiers.
    -   Recherchez la taille requise pour vos mémoires tampons en appelant [**IWMReaderAdvanced :: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) ou [**IWMReaderAdvanced :: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) pour chaque sortie et/ou flux pour lequel la mémoire tampon est utilisée. Si vous utilisez le lecteur synchrone, utilisez [**IWMSyncReader :: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) ou [**IWMSyncReader :: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) à la place.
    -   Créez chaque mémoire tampon pour le pool.
3.  Configurez le lecteur ou le lecteur synchrone pour la lecture. Pour plus d’informations, consultez [lecture de fichiers avec le lecteur asynchrone](reading-files-with-the-asynchronous-reader.md) ou [lecture de fichiers avec le lecteur synchrone](reading-files-with-the-synchronous-reader.md).
4.  Avant de commencer l’écriture, appelez [**IWMReaderAdvanced :: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) ou [**IWMReaderAdvanced :: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) pour chaque sortie et flux pour lesquels vous allouez des tampons à l’aide de l’objet lecteur. Pour le lecteur synchrone, appelez [**IWMSyncReader2 :: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) ou [**IWMSyncReader2 :: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) à la place.
5.  Commencez la lecture du fichier.

L’objet de lecture appelle le rappel d’allocateur approprié et récupère des exemples de votre application. La logique de gestion de la mémoire tampon doit inclure un moyen de signaler qu’une mémoire tampon est libre d’être réutilisée. En général, une mémoire tampon est replacée dans le pool lors du rendu de son contenu. Selon votre application, il se peut que vous ayez besoin de quelques tampons dans le pool ou un grand nombre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> </dl>

 

 




