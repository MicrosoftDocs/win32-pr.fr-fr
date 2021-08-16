---
description: Lecture de flux Web ASF dans DirectShow
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: Lecture de flux Web ASF dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28d9d3b7ea4fba5537383a846e6eff64f3815eefa21613c6056a15a5e497f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824624"
---
# <a name="asf-web-stream-playback-in-directshow"></a>Lecture de flux Web ASF dans DirectShow

Microsoft DirectShow prend en charge les flux web dans les scénarios de lecture de fichiers par le biais du filtre de [lecteur ASF WM](wm-asf-reader-filter.md) , mais vous devez écrire votre propre filtre DirectShow pour capturer et conserver le flux.

> [!Note]  
> pour lire des flux web dans du contenu diffusé en continu à partir d’un serveur exécutant Services Windows Media, utilisez la série Lecteur Windows Media 9 ActiveX® contrôle incorporé dans une page web.

 

Lorsqu’un fichier contenant des flux de type WMMEDIATYPE \_ filetransfer est donné, le lecteur ASF WM crée une broche de sortie pour celui-ci. Le bloc de format sera une structure de [**\_ \_ format webstream WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) . (cette structure est documentée dans la documentation du kit de développement logiciel (SDK) Windows Media Format.) Si aucun filtre en aval ne peut gérer ce type de média, le code confidentiel restera non connecté, mais le fichier continuera de lire les flux audio et/ou vidéo.

chaque échantillon de média dans un flux web contient une structure d' [**\_ \_ \_ en-tête d’exemple webstream WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , qui est documentée dans la documentation du kit de développement logiciel (SDK) Windows media Format. La structure a une longueur variable en fonction de la longueur de son membre **wszURL** . Le pointeur vers les exemples de données pointe initialement vers cette structure, et vous devez avancer le pointeur au-delà de la structure afin d’accéder aux données réelles dans le flux.

Le filtre de votre gestionnaire de flux Web doit être basé sur la classe [**CBaseRenderer**](cbaserenderer.md) . Dans la méthode [**CBaseRenderer ::D orendersample**](cbaserenderer-dorendersample.md) , le filtre doit analyser la structure pour obtenir des informations sur le flux Web, puis exécuter l’action appropriée. En général, cela implique l’enregistrement du fichier sur le disque, puis l’appel des fonctions [**CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) et [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) ou [**CommitUrlCacheEntryA**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) pour placer les fichiers dans le cache Internet Explorer. Le filtre doit gérer des fichiers à parties multiples, autrement dit, des fichiers qui sont plus grands qu’un exemple, et doivent également gérer les commandes de rendu, qui sont spécifiées par le membre d' **\_ \_ en-tête de l’exemple d' \_ en-tête webstream WMT.** Le filtre envoie un événement d' [**\_ \_ événement OLE EC**](ec-ole-event.md) à l’application, ainsi que le texte de **l' \_ exemple d' \_ \_ en-tête d’exemple webstream WMT. wszURL** qui contient le nom du fichier à restituer. L’application fait ensuite en sorte que le navigateur affiche la page spécifiée. Si le flux Web a été créé correctement, le fichier doit déjà être dans le cache.

pour plus d’informations sur \_ le format de flux de données en chaîne wmt \_ et sur \_ \_ l’exemple d’en-tête d’exemple webstream wmt \_ , consultez la documentation du SDK Windows Media format.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture des fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
