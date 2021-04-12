---
description: Lecture de flux Web ASF dans DirectShow
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: Lecture de flux Web ASF dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d14a83d2baf9c11aa824f5d6358f62790c16b30
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317750"
---
# <a name="asf-web-stream-playback-in-directshow"></a>Lecture de flux Web ASF dans DirectShow

Microsoft DirectShow prend en charge les flux Web dans les scénarios de lecture de fichiers par le biais du filtre de [lecteur ASF WM](wm-asf-reader-filter.md) , mais vous devez écrire votre propre filtre DirectShow pour capturer et conserver le flux.

> [!Note]  
> Pour lire des flux Web dans du contenu diffusé en continu à partir d’un serveur exécutant Windows Media Services, utilisez le contrôle® ActiveX de Windows Media Player 9 Series dans une page Web.

 

Lorsqu’un fichier contenant des flux de type WMMEDIATYPE \_ filetransfer est donné, le lecteur ASF WM crée une broche de sortie pour celui-ci. Le bloc de format sera une structure de [**\_ \_ format webstream WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) . (Cette structure est documentée dans la documentation du kit de développement logiciel (SDK) Windows Media format.) Si aucun filtre en aval ne peut gérer ce type de média, le code confidentiel restera non connecté, mais le fichier continuera de lire les flux audio et/ou vidéo.

Chaque échantillon de média dans un flux Web contient une structure d' [**\_ \_ \_ en-tête d’exemple webstream WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , qui est décrite dans la documentation du kit de développement logiciel (SDK) du format Windows Media. La structure a une longueur variable en fonction de la longueur de son membre **wszURL** . Le pointeur vers les exemples de données pointe initialement vers cette structure, et vous devez avancer le pointeur au-delà de la structure afin d’accéder aux données réelles dans le flux.

Le filtre de votre gestionnaire de flux Web doit être basé sur la classe [**CBaseRenderer**](cbaserenderer.md) . Dans la méthode [**CBaseRenderer ::D orendersample**](cbaserenderer-dorendersample.md) , le filtre doit analyser la structure pour obtenir des informations sur le flux Web, puis exécuter l’action appropriée. En général, cela implique l’enregistrement du fichier sur le disque, puis l’appel des fonctions [**CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) et [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) ou [**CommitUrlCacheEntryA**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) pour placer les fichiers dans le cache Internet Explorer. Le filtre doit gérer des fichiers à parties multiples, autrement dit, des fichiers qui sont plus grands qu’un exemple, et doivent également gérer les commandes de rendu, qui sont spécifiées par le membre d' **\_ \_ en-tête de l’exemple d' \_ en-tête webstream WMT.** Le filtre envoie un événement d' [**\_ \_ événement OLE EC**](ec-ole-event.md) à l’application, ainsi que le texte de **l' \_ exemple d' \_ \_ en-tête d’exemple webstream WMT. wszURL** qui contient le nom du fichier à restituer. L’application fait ensuite en sorte que le navigateur affiche la page spécifiée. Si le flux Web a été créé correctement, le fichier doit déjà être dans le cache.

Pour plus d’informations sur \_ le format de flux de données \_ et l’exemple d’en-tête de flux de données à diffusion en continu WMT \_ \_ \_ , consultez la documentation du SDK Windows Media format.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture de fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
