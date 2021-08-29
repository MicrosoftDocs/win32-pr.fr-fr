---
description: Comment les décodeurs utilisent IAMVideoAccelerator
ms.assetid: 0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d
title: Comment les décodeurs utilisent IAMVideoAccelerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12918383808cfb492f010c7a99704111229ea551f5b7efe9d641aebab5786c3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102739"
---
# <a name="how-decoders-use-iamvideoaccelerator"></a>Comment les décodeurs utilisent IAMVideoAccelerator

L’interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) active les opérations d’accélération vidéo génériques, y compris l’accélération vidéo DirectX (va). Pour l’accélération non DirectX VA, le décodeur et le pilote vidéo doivent tous deux adhérer à un protocole commun.

Cette section décrit l’ordre général des opérations que tout décodeur doit suivre lors de l’utilisation de cette interface. Pour plus d’informations sur les décodeurs DirectX basés sur VA, consultez [mappage de l’accélération vidéo DirectX à IAMVideoAccelerator](mapping-directx-video-acceleration-to-iamvideoaccelerator.md).

> [!Note]  
> cette interface est disponible dans Windows 2000 et versions ultérieures.

 

l’interface [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) est exposée sur la broche d’entrée de la [superposition Mixer](overlay-mixer-filter.md) ou le convertisseur de mixage vidéo (VMR). L’interface [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) est exposée sur la broche de sortie du décodeur. La séquence d’événements pour la connexion des codes confidentiels du filtre est la suivante :

1.  le gestionnaire de Graph de filtre appelle [**IPin :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) sur la broche de sortie du filtre de décodeur. Un [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) est un paramètre facultatif.
    -   [**Am \_ Le \_ type de média**](/windows/win32/api/strmif/ns-strmif-am_media_type) est une structure de données qui décrit un type de média. Il contient un GUID MajorType (qui, dans notre cas, doit être une \_ vidéo MediaType), un GUID de sous-type (qui, dans notre cas, doit être un GUID d’accélérateur vidéo) et un grand nombre d’autres choses. L’un de ces éléments est un GUID de type de format contenant des informations sur le support, y compris dans notre cas la largeur et la hauteur d’une image vidéo non compressée, le plus souvent dans une structure [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
    -   Le cas échéant, la structure du [**\_ \_ type de média**](/windows/win32/api/strmif/ns-strmif-am_media_type) indique au décodeur qu’il doit fonctionner à l’aide du type de média spécifié, qui peut être « entièrement spécifié » ou « partiellement spécifié ». Si « entièrement spécifié », le décodeur tente normalement de fonctionner avec ce type de média. Si « partiellement spécifié », il tente de trouver un mode d’opération compatible « entièrement spécifié » qu’il peut utiliser pour se connecter de manière cohérente avec le type de média « partiellement spécifié ».
    -   Pour tenter de trouver un type de média « entièrement spécifié » à utiliser pour une connexion, il suffit d’exécuter une liste de chaque type de média « entièrement spécifié » que la broche de sortie prend en charge, ce qui est compatible avec le type de média « partiellement spécifié » et de tenter de se connecter à chacun d’eux jusqu’à ce qu’il réussisse. le processus serait normalement similaire si aucun \_ \_ TYPE de média AM n’est contenu dans l’appel de [**IPin :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , mais avec la broche de sortie qui doit vérifier tous ses types de média.
2.  Si le décodeur souhaite vérifier si un [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) spécifique (y compris un GUID d’accélérateur vidéo) est pris en charge par la broche d’entrée en aval, il peut appeler [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) (avec le GUID de l’accélérateur vidéo comme sous-type du **\_ média am \_**) ou il peut simplement essayer de se connecter à ce code confidentiel comme décrit dans le point 5 ci-dessous
3.  Si le décodeur ne connaît pas les GUID d’accélérateur vidéo pris en charge par la broche d’entrée en aval et ne souhaite pas proposer simplement un GUID d’accélérateur vidéo particulier en appelant le [**IPIN :: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)du pin d’entrée en aval, le décodeur peut appeler [**IAMVideoAccelerator :: GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) pour obtenir une liste des GUID d’accélérateur vidéo pris en charge par le pin.
4.  Pour certains GUID d’accélérateur vidéo particuliers, le décodeur peut appeler la [**IAMVideoAccelerator :: GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) du pin d’entrée en aval pour obtenir une liste des formats de pixel **DDPIXELFORMAT** qui peuvent être utilisés pour afficher un GUID d’accélérateur vidéo spécifique. La liste renvoyée doit être considérée comme étant dans un ordre de préférence décroissant (c’est-à-dire, avec le format le plus préféré répertorié en premier).
5.  Le décodeur appelle le [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)du pin d’entrée en aval, en lui transmettant un [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) avec le GUID d’accélérateur vidéo approprié comme sous-type du type de média. Cela configure la connexion pour l’opération, y compris la création des surfaces de sortie non compressées (qui sont allouées à l’aide de la largeur et de la hauteur trouvées dans le **\_ \_ type de média am**, et le nombre de surfaces à allouer trouvées par un appel décrit ci-dessous, et toutes les autres informations que l’accélérateur vidéo a disponibles et qui souhaite l’utiliser à cette Si la broche d’entrée en aval rejette le GUID de l’accélérateur vidéo ou un autre aspect de la connexion, cela peut entraîner l’échec de **IPIN :: ReceiveConnection** . Si **IPIN :: ReceiveConnection** échoue, cela est indiqué dans un **HRESULT** retourné et le décodeur peut tenter à nouveau d’effectuer l’appel, par exemple avec un nouveau GUID d’accélérateur vidéo dans la structure du **\_ \_ type de média am** .
    -   [!Note]  
        > Il s’agit d’une autre méthode (et la méthode la plus définitive) pour le décodeur afin de déterminer ce qui est pris en charge par la broche d’entrée en aval, en appelant simplement [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) et en tentant de se connecter, puis en vérifiant si la tentative de connexion a réussi.

         

    -   Pendant le [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection), le convertisseur appelle le [**IAMVideoAcceleratorNotify :: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo)du décodeur, en lui transmettant le GUID de l’accélérateur vidéo et une structure [**AMVAUncompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompbufferinfo) , afin de déterminer le nombre de surfaces non compressées à allouer. Le décodeur remplit et retourne la structure, qui contient le nombre minimal et maximal de surfaces à allouer du type particulier, et une structure **DDPIXELFORMAT** décrivant le format de pixel des surfaces à allouer.
    -   [!Note]  
        > Rien n’est réellement passé au décodeur dans l’appel à [**IAMVideoAcceleratorNotify :: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo) autre que le GUID de l’accélérateur vidéo.

         

6.  Le convertisseur appelle le [**IAMVideoAcceleratorNotify :: SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)du décodeur, en passant au décodeur le nombre réel de surfaces non compressées qui ont été allouées.
7.  Le convertisseur appelle le [**IAMVideoAcceleratorNotify :: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) du décodeur pour obtenir toutes les données nécessaires pour initialiser l’accélérateur vidéo.
8.  Le décodeur appelle [**IAMVideoAccelerator :: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo), en lui transmettant un GUID d’accélérateur vidéo, une structure [**AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) et le nombre de types de tampons compressés, pour obtenir un ensemble de structures de données [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) , l’une correspondant à chaque type de mémoire tampon de données COMpressées utilisé par le GUID de l’accélérateur vidéo.
    -   La structure [**AMVAUncompDataInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) contient la largeur et la hauteur des données décompressées décodées (en pixels) et le DDPIXELFORMAT de l’image non compressée.
    -   Les structures de données [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) retournées chaque contiennent :
        -   Nombre de mémoires tampons compressées nécessaires du type spécifique.
        -   La largeur et la hauteur de la surface à créer (champs qui peuvent avoir ou non une signification réelle).
            > [!Note]  
            > L’opération d’allocation de surface DirectDraw pour les mémoires tampons compressées ne fournit pas actuellement la largeur ou la hauteur de ces surfaces pour être supérieures ou égales à 2 ^ 15, bien que l’appel d’allocation de surface puisse ne pas échouer si cette limite n’est pas respectée. Par conséquent, le pilote peut structurer ses demandes de mémoire tampon compressée afin d’éviter des tailles extrêmes. Par exemple, au lieu de demander une mémoire tampon avec width = "1" et Height = "65536", le pilote doit demander une mémoire tampon de width = "1024" et Height = "64".

             

        -   Nombre total d’octets à utiliser par l’aire.
        -   Structure de type **DDSCAPS2** définissant un objet DirectDrawSurface, décrivant les fonctionnalités permettant de créer des surfaces pour stocker des données compressées.
        -   DDPIXELFORMAT, décrivant le format de pixel utilisé pour créer des surfaces pour stocker des données compressées (un champ qui peut avoir ou non une signification réelle).

> [!Note]  
> Les appels du convertisseur à certaines méthodes d’interface [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) du décodeur peuvent (et normalement) se produire à l’intérieur de l’appel du décodeur à [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)du convertisseur. Plus précisément, cela s’applique aux éléments suivants :
>
> -   [**IAMVideoAcceleratorNotify :: GetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo),
> -   [**IAMVideoAcceleratorNotify :: SetUncompSurfacesInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)et
> -   [**IAMVideoAcceleratorNotify :: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata).

 

> [!Note]  
> Pour prendre en charge les modifications de format dynamiques, le décodeur peut également appeler [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) et d’autres méthodes par dessus, alors que les filtres sont connectés et en cours d’exécution. Cette fonctionnalité est fournie pour prendre en charge les modifications de format dynamiques (bien qu’elles ne soient pas dans le H. 263, annexe P, sens, car tous les jeux de données sont redémarrés à partir de zéro et toutes les informations de l’image de référence sont donc perdues).

 

Vous trouverez ci-dessous une description de l’utilisation de [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) lors de l’opération après l’initialisation :

1.  Pour chaque surface non compressée, le décodeur appelle [**IAMVideoAccelerator :: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) pour commencer le traitement de la création de l’image de sortie. Dans ce cas, le décodeur envoie une structure [**AMVABeginFrameInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) .
    -   La structure [**AMVABeginFrameInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) contient un index pour une mémoire tampon de destination, un pointeur vers certaines données à envoyer en aval et un pointeur vers un emplacement où l’accélérateur peut placer des données pour le décodeur à lire.
    -   Remarque 1 : l’accélérateur ne reçoit pas réellement l’index de la mémoire tampon de destination, car il est traduit par le convertisseur avant de passer en aval.
    -   Remarque 2 : [**IAMVideoAccelerator :: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) peut être appelé plusieurs fois entre des appels à [**IAMVideoAccelerator :: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe).
    -   Remarque 3 : il n’existe aucune hypothèse dans l’opération d’interface que [**IAMVideoAccelerator :: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) et [**IAMVideoAccelerator :: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) doivent être appelées pour le traitement de chaque image individuelle dans le flux binaire.

        Ce que [**IAMVideoAccelerator :: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) fait, en ce qui concerne l’interface, crée une association dans le convertisseur entre un index et une surface non compressée. Il fournit également un moyen d’appeler une fonction spécifique dans un pilote de périphérique (avec la prise en charge d’un moyen de passer des données arbitraires entre le décodeur et le pilote de périphérique).

        (Toutefois, dans l’opération DirectX VA, il existe une spécification décrite ci-dessous : [**IAMVideoAccelerator :: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) et [**IAMVideoAccelerator :: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) doivent être appelés pour le traitement de chaque image individuelle dans le flux binaire.)

2.  Pour envoyer des données non compressées à l’accélérateur, le décodeur appelle :
    -   [**IAMVideoAccelerator :: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) pour déterminer si une mémoire tampon est sécurisée pour la lecture ou l’écriture dans.
    -   [**IAMVideoAccelerator :: GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) pour verrouiller et obtenir l’accès à une mémoire tampon spécifiée (si elle ne l’a pas précédemment appelée pour obtenir cet accès). **GetBuffer** peut également être utilisé pour obtenir une copie du contenu de la dernière image de sortie non compressée pour laquelle [**IAMVideoAccelerator :: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) a été appelé, en fournissant [**IAMVideoAccelerator :: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) n’a pas été appelé pour cet index de tampon de destination. Si la DDI retourne un état de rendu de DDERR \_ WASSTILLDRAWING pour la mémoire tampon demandée, une boucle de mise en veille est traitée dans **GetBuffer** jusqu’à ce que cette condition soit désactivée. Pour appeler **GetBuffer**, le décodeur aura besoin de certaines informations d’une structure de données [**AMVACompBufferInfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) qui est obtenue en appelant [**IAMVideoAccelerator :: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo).
    -   [**IAMVideoAccelerator :: Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) pour indiquer que les données d’un ensemble de mémoires tampons compressées, comme indiqué dans un tableau de structures de données [**AMVABUFFERINFO**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabufferinfo) , doivent être traitées. Un code de fonction dwFunction est passé au pilote dans cet appel. Un pointeur lpPrivateInputData est également passé à certaines données à envoyer en aval, et un pointeur lpPrivateOutputData est passé à un emplacement où le processus en aval peut placer des données pour le décodeur à lire.
    -   [**IAMVideoAccelerator :: ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) pour indiquer que le décodeur a terminé l’utilisation d’une mémoire tampon spécifiée pendant le moment et n’a plus besoin d’un accès verrouillé à la mémoire tampon. (Si le décodeur souhaite continuer à utiliser la mémoire tampon, il peut simplement ne pas appeler **IAMVideoAccelerator :: ReleaseBuffer** pour le moment, ce qui évite d’avoir à appeler [**IAMVideoAccelerator :: GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) jusqu’à ce qu’il envisage vraiment de ne pas utiliser la mémoire tampon.) Le décodeur ne doit pas écrire dans la mémoire tampon après l’appel de la méthode [**Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) jusqu’à ce que [**QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) indique que la mémoire tampon est sécurisée pour l’écriture.
3.  Pour terminer le traitement de sortie pour une mémoire tampon de destination, le décodeur appelle [**IAMVideoAccelerator :: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe). Il peut passer des données arbitraires en aval avec cet appel, et c’est essentiellement tout ce qui se produit à la suite de cet appel. Il n’envoie pas d’index de tampon de destination dans cet appel. il ne peut donc pas indiquer précisément la mémoire tampon de destination qui est terminée, sauf si cette indication est contenue dans les données arbitraires transmises.
4.  Pour afficher un frame, le décodeur appelle [**IAMVideoAccelerator ::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) avec l’index du frame à afficher et une structure [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) contenant les horodatages de début et de fin, ainsi que les indicateurs pertinents tels que **dwTypeSpecificFlags** dans la structure des [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) et **dwInterlaceFlags** dans la structure [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Le décodeur doit vérifier que toutes les opérations de décompression qui affectent le contenu du frame se sont terminées avant d’appeler **DisplayFrame**.
5.  Enfin, le décodeur doit, à la fin de tout le traitement, indiquer la fin de tous les autres frames de sortie commencés en appelant [**IAMVideoAccelerator :: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) et libérer toutes ses mémoires tampons verrouillées en appelant [**IAMVideoAccelerator :: ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) pour chaque mémoire tampon non publiée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces et spécifications du décodeur](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



