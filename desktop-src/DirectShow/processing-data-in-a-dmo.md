---
description: Traitement des données dans une DMO
ms.assetid: 715482d9-23f4-40d0-9c09-7a81e148c543
title: Traitement des données dans une DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd4dd05df960bd27b34eb55b604c8469e7bbaedd57ea928f5b4f412ad4bff04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748239"
---
# <a name="processing-data-in-a-dmo"></a>Traitement des données dans une DMO

Cette section explique comment traiter un flux de données à l’aide d’un DMO. Les étapes répertoriées dans cette section sont le comportement par défaut. toutes les DMOs doivent prendre en charge les méthodes décrites ici. Ces méthodes utilisent des mémoires tampons distinctes pour l’entrée et la sortie. Certains DMOs prennent également en charge le traitement sur place, à l’aide d’une seule mémoire tampon. Pour plus d’informations sur le traitement sur place, consultez [traitement sur place](in-place-processing.md).

**Allouer des tampons**

Le client est responsable de toutes les allocations de mémoire tampon. une fois que vous avez défini les types de média sur le DMO, interrogez le DMO pour les exigences de mémoire tampon de chaque flux. Celles-ci peuvent changer en fonction du type de média. Pour chaque flux, appelez la méthode [**IMediaObject :: GetInputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo) ou [**IMediaObject :: GetOutputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo) . Ces méthodes retournent les informations suivantes :

-   Taille minimale de la mémoire tampon, en octets.
-   Exigences d’alignement, le cas échéant. Une mémoire tampon est alignée si l’adresse de début est un multiple d’un entier spécifié.
-   quantité maximale de données que le DMO contiendra pour la préanalyse. Ce nombre s’applique uniquement aux flux d’entrée. pour certains types de données (par exemple, l’encodage MPEG), une DMO devra peut-être anticiper le flux. la valeur de préanalyse indique la quantité de données d’entrée dont l’DMO aura besoin avant de produire une sortie.

Le client doit allouer des tampons qui répondent à ces exigences. en outre, l’DMO peut avoir des exigences quant à la façon dont le client conditionne les données d’entrée. par exemple, l’DMO peut nécessiter que chaque mémoire tampon contienne exactement un échantillon (ou image vidéo). Pour déterminer ces exigences, appelez la méthode [**IMediaObject :: GetInputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo) . La méthode [**IMediaObject :: GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) retourne des informations similaires sur un flux de sortie.

Dans le modèle de diffusion en continu par défaut, le client ne passe pas de pointeurs de tampon brut à l’DMO. Au lieu de cela, il utilise un objet COM léger qui expose l’interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) . L’interface **IMediaBuffer** joue le rôle de wrapper com pour un bloc de mémoire. Étant donné qu’il s’agit d’un objet COM, il prend en charge le décompte de références, qui permet de s’assurer que les tampons ne sont pas libérés quand ils sont en cours d’utilisation.

> [!Note]  
> L’interface **IMediaBuffer** sert de fonction similaire à l’interface **IMediaSample** dans DirectShow.

 

Le client doit implémenter l’objet **IMediaBuffer** . Pour plus d’informations, consultez [implémentation de IMediaBuffer](implementing-imediabuffer.md).

**Traitement des données**

Pour traiter les données, procédez comme suit :

1.  Pour chaque flux d’entrée, remplissez une mémoire tampon avec des données d’entrée.
2.  Appelez [**IMediaObject ::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput) pour fournir chaque mémoire tampon.
3.  Appelez [**IMediaObject ::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) pour traiter les données. Cette méthode prend un tableau de mémoires tampons, un pour chaque flux de sortie.
4.  Répétez l’opération jusqu’à ce qu’il n’y ait plus de données d’entrée.

La méthode **ProcessInput** accepte l’entrée d’un flux à la fois. en général, la méthode est retournée immédiatement, et la DMO contient un décompte de références sur l’objet **IMediaBuffer** . Il libère l’objet après avoir traité toutes les données de la mémoire tampon, ou lorsque l’application vide le DMO. ne réutilisez pas une mémoire tampon tant que le DMO ne l’a pas libérée. Pour déterminer si un flux d’entrée peut accepter plus de données, appelez la méthode [**IMediaObject :: GetInputStatus**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstatus) . cette méthode retourne le DMO \_ \_ indicateur d’acceptation de données STATUSF d’entrée \_ \_ si le flux peut accepter davantage d’entrées.

La méthode **ProcessOutput** génère une sortie pour tous les flux de sortie en même temps. l’application passe dans un tableau de [**DMO structures de \_ \_ \_ tampons de données de sortie**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) , une pour chaque flux de sortie. Chaque structure du tableau a un pointeur vers un objet **IMediaBuffer** . le DMO écrit autant de données de sortie que possible dans les mémoires tampons. Il définit également différents indicateurs pour signaler l’état de l’opération. l’indicateur de DMO \_ \_ données \_ de sortie BUFFERF \_ incomplet indique que le DMO peut produire plus de sortie à partir de l’entrée existante. Dans ce cas, le client peut appeler de nouveau **ProcessOutput** . Dans le cas contraire, elle doit appeler **ProcessInput** avec davantage de données d’entrée. le DMO ne modifie jamais les données dans les mémoires tampons d’entrée ; Il écrit uniquement dans les mémoires tampons de sortie.

Une fois que vous avez remis toutes les données à un flux d’entrée, appelez la méthode [**IMediaObject ::D iscontinuity**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-discontinuity) . la DMO n’accepte pas d’entrée supplémentaire dans ce flux tant que vous n’avez pas traité la sortie restante (ou vidé la DMO).

à tout moment après le début de la diffusion en continu, le DMO est en mesure de recevoir une sortie d’entrée ou de production, ou les deux. par conséquent, soit **GetInputStatus** retourne DMO \_ entrée \_ STATUSF acceptent les \_ \_ données, soit **ProcessOutput** retourne DMO données de \_ sortie \_ \_ BUFFERF \_ incomplètes. L’application maintient les données transmises en testant ces indicateurs et en appelant **ProcessInput** ou **ProcessOutput** en conséquence. Pour interrompre le workflow, appelez la méthode [**IMediaObject :: Flush**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-flush) . cette méthode fait en sorte que la DMO ignore les mémoires tampons qu’elle détient en interne.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hébergement direct d’un DMO](directly-hosting-a-dmo.md)
</dt> <dt>

[Traitement sur place](in-place-processing.md)
</dt> </dl>

 

 



