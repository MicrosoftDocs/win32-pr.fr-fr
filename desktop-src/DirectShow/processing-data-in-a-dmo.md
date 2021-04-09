---
description: Traitement des données dans une DMO
ms.assetid: 715482d9-23f4-40d0-9c09-7a81e148c543
title: Traitement des données dans une DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9f5d5d820dc1467c25f9d411d46a9c66935e8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846425"
---
# <a name="processing-data-in-a-dmo"></a>Traitement des données dans une DMO

Cette section explique comment traiter un flux de données à l’aide d’un DMO. Les étapes répertoriées dans cette section sont le comportement par défaut. toutes les DMOs doivent prendre en charge les méthodes décrites ici. Ces méthodes utilisent des mémoires tampons distinctes pour l’entrée et la sortie. Certains DMOs prennent également en charge le traitement sur place, à l’aide d’une seule mémoire tampon. Pour plus d’informations sur le traitement sur place, consultez [traitement sur place](in-place-processing.md).

**Allouer des tampons**

Le client est responsable de toutes les allocations de mémoire tampon. Une fois que vous avez défini les types de médias sur le DMO, interrogez DMO pour obtenir les exigences de mémoire tampon de chaque flux. Celles-ci peuvent changer en fonction du type de média. Pour chaque flux, appelez la méthode [**IMediaObject :: GetInputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo) ou [**IMediaObject :: GetOutputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo) . Ces méthodes retournent les informations suivantes :

-   Taille minimale de la mémoire tampon, en octets.
-   Exigences d’alignement, le cas échéant. Une mémoire tampon est alignée si l’adresse de début est un multiple d’un entier spécifié.
-   Quantité maximale de données que le DMO contiendra pour la préanalyse. Ce nombre s’applique uniquement aux flux d’entrée. Pour certains types de données (par exemple, l’encodage MPEG), un DMO devra peut-être effectuer une recherche dans le flux. La valeur de préanalyse indique la quantité de données d’entrée requises par DMO avant de pouvoir produire une sortie.

Le client doit allouer des tampons qui répondent à ces exigences. En outre, DMO peut avoir des exigences quant à la façon dont le client conditionne les données d’entrée. Par exemple, DMO peut exiger que chaque mémoire tampon contienne exactement un échantillon (ou image vidéo). Pour déterminer ces exigences, appelez la méthode [**IMediaObject :: GetInputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo) . La méthode [**IMediaObject :: GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) retourne des informations similaires sur un flux de sortie.

Dans le modèle de diffusion en continu par défaut, le client ne transmet pas de pointeurs de tampon brut à DMO. Au lieu de cela, il utilise un objet COM léger qui expose l’interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) . L’interface **IMediaBuffer** joue le rôle de wrapper com pour un bloc de mémoire. Étant donné qu’il s’agit d’un objet COM, il prend en charge le décompte de références, qui permet de s’assurer que les tampons ne sont pas libérés quand ils sont en cours d’utilisation.

> [!Note]  
> L’interface **IMediaBuffer** sert de fonction similaire à l’interface **IMediaSample** dans DirectShow.

 

Le client doit implémenter l’objet **IMediaBuffer** . Pour plus d’informations, consultez [implémentation de IMediaBuffer](implementing-imediabuffer.md).

**Traitement des données**

Pour traiter les données, procédez comme suit :

1.  Pour chaque flux d’entrée, remplissez une mémoire tampon avec des données d’entrée.
2.  Appelez [**IMediaObject ::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput) pour fournir chaque mémoire tampon.
3.  Appelez [**IMediaObject ::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) pour traiter les données. Cette méthode prend un tableau de mémoires tampons, un pour chaque flux de sortie.
4.  Répétez l’opération jusqu’à ce qu’il n’y ait plus de données d’entrée.

La méthode **ProcessInput** accepte l’entrée d’un flux à la fois. En général, la méthode est retournée immédiatement, et la méthode DMO contient un décompte de références sur l’objet **IMediaBuffer** . Il libère l’objet après avoir traité toutes les données de la mémoire tampon, ou lorsque l’application vide la DMO. Ne réutilisez pas une mémoire tampon tant que DMO ne l’a pas libérée. Pour déterminer si un flux d’entrée peut accepter plus de données, appelez la méthode [**IMediaObject :: GetInputStatus**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstatus) . Cette méthode retourne l' \_ indicateur d' \_ \_ acceptation STATUSF Accept Data de DMO \_ si le flux peut accepter davantage d’entrées.

La méthode **ProcessOutput** génère une sortie pour tous les flux de sortie en même temps. L’application passe dans un tableau de structures de [**\_ \_ \_ tampons de données de sortie DMO**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) , une pour chaque flux de sortie. Chaque structure du tableau a un pointeur vers un objet **IMediaBuffer** . Le DMO écrit autant de données de sortie que possible dans les tampons. Il définit également différents indicateurs pour signaler l’état de l’opération. L' \_ \_ \_ \_ indicateur BUFFERF Incomplete des données de sortie DMO indique que DMO peut produire plus de sortie à partir de l’entrée existante. Dans ce cas, le client peut appeler de nouveau **ProcessOutput** . Dans le cas contraire, elle doit appeler **ProcessInput** avec davantage de données d’entrée. Le DMO ne modifie jamais les données dans les mémoires tampons d’entrée ; Il écrit uniquement dans les mémoires tampons de sortie.

Une fois que vous avez remis toutes les données à un flux d’entrée, appelez la méthode [**IMediaObject ::D iscontinuity**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-discontinuity) . DMO n’accepte pas d’entrée supplémentaire dans ce flux tant que vous n’avez pas traité la sortie restante (ou vidé le DMO).

À tout moment après le début de la diffusion en continu, DMO est en mesure de recevoir une sortie d’entrée ou de production, ou les deux. Par conséquent, **GetInputStatus** retourne DMO \_ entrée \_ STATUSF \_ Accept \_ Data, ou **ProcessOutput** retourne DMO \_ Output \_ Data \_ BUFFERF \_ Incomplete. L’application maintient les données transmises en testant ces indicateurs et en appelant **ProcessInput** ou **ProcessOutput** en conséquence. Pour interrompre le workflow, appelez la méthode [**IMediaObject :: Flush**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-flush) . Avec cette méthode, DMO rejette les tampons qu’elle détient en interne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hébergement direct d’un DMO](directly-hosting-a-dmo.md)
</dt> <dt>

[Traitement sur place](in-place-processing.md)
</dt> </dl>

 

 



