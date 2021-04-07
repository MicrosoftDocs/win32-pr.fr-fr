---
title: Lecture de flux Web dans DirectShow
description: Lecture de flux Web dans DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, lecture de flux Web
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), lecture de flux Web
- ASF (format de systèmes avancés), lecture de flux Web
- DirectShow, lecture de flux Web
- Flux Web, DirectShow
- Flux Web, lecture dans DirectShow
- flux, lecture de flux Web dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939785"
---
# <a name="web-stream-playback-in-directshow"></a>Lecture de flux Web dans DirectShow

Microsoft DirectShow prend en charge les flux Web (pour plus d’informations, consultez [flux Web](web-streams.md) ) dans les scénarios de lecture de fichiers via le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) , mais vous devez écrire votre propre filtre DirectShow pour capturer et conserver le flux.

> [!Note]  
> Pour lire des flux Web dans du contenu diffusé en continu à partir d’un serveur exécutant Windows Media Services, utilisez le contrôle® ActiveX de Windows Media Player 9 Series dans une page Web.

 

Lorsqu’un fichier contenant des flux de type WMMEDIATYPE \_ filetransfer est donné, le lecteur ASF WM crée une broche de sortie pour celui-ci. Le bloc de format sera une structure de [**\_ \_ format webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) . Si aucun filtre en aval ne peut gérer ce type de média, le code confidentiel restera non connecté, mais le fichier continuera de lire les flux audio et/ou vidéo.

Il est important de comprendre que chaque échantillon de média dans un flux Web contient une structure d' [**\_ \_ \_ en-tête d’exemple de flux d’en-tête WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , qui a une longueur variable en fonction de la longueur de son membre **wszURL** . Le pointeur vers les exemples de données pointe initialement vers cette structure, et vous devez avancer le pointeur au-delà de la structure afin d’accéder aux données réelles dans le flux. Le filtre de votre gestionnaire de flux Web doit être basé sur la classe **CBaseRenderer** . Dans la méthode **DoRenderSample** , le filtre doit analyser la structure pour obtenir des informations sur le flux Web, puis exécuter l’action appropriée. En général, cela implique l’enregistrement du fichier sur le disque, puis l’appel de **CommitUrlCacheEntry** et **CreateUrlCacheEntry** pour placer les fichiers dans le cache Internet Explorer. Le filtre doit gérer des fichiers à parties multiples, autrement dit, des fichiers qui sont plus grands qu’un exemple, et doivent également gérer les commandes de rendu, qui sont spécifiées par le membre d' **\_ \_ en-tête de l’exemple d' \_ en-tête webstream WMT.** Le filtre envoie un **\_ \_ événement OLE EC** à l’application, ainsi que le texte de l' **exemple d' \_ \_ \_ en-tête d’exemple webstream WMT. wszURL** qui contient le nom du fichier à restituer. L’application fait ensuite en sorte que le navigateur affiche la page spécifiée. Si le flux Web a été créé correctement, le fichier doit déjà être dans le cache.

Pour plus d’informations sur les événements **CBaseRenderer**, **DoRenderSample** et **EC \_ OLE \_**, consultez la documentation du kit de développement logiciel (SDK) DirectShow.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Flux Web**](web-streams.md)
</dt> </dl>

 

 




