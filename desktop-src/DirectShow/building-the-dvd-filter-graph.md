---
description: Génération du filtre de DVD Graph
ms.assetid: 1d2f8284-2deb-4207-b067-24a54d6b286c
title: Génération du filtre de DVD Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d15c7d84ec138771e1f5da8be4270faae049cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111410"
---
# <a name="building-the-dvd-filter-graph"></a>Génération du filtre de DVD Graph

comme pour toute application DirectShow, une application de lecture de DVD commence par créer un graphique de filtre. DirectShow fournit les composants suivants pour la lecture de DVD :

-   [générateur de Graph DVD](dvd-graph-builder.md). Objet d’assistance qui construit le graphique de filtre. Il expose l’interface [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) .
-   Filtre de [navigateur DVD](dvd-navigator-filter.md) . filtre de DirectShow qui gère la lecture des DVD, la navigation et d’autres commandes.

La lecture des DVD nécessite également un décodeur MPEG-2. Les décodeurs MPEG-2 matériels et logiciels sont disponibles auprès de tiers. tout d’abord, créez une instance de l’objet DVD Graph Builder.


```C++
IDvdGraphBuilder *pBuild = NULL;
hr = CoCreateInstance(CLSID_DvdGraphBuilder, NULL, 
    CLSCTX_INPROC_SERVER, IID_IDvdGraphBuilder, (void **)&pBuild);
```



À ce stade, vous pouvez sélectionner et configurer le convertisseur vidéo avant de générer le reste du graphique. Cette étape, qui est facultative, est décrite plus en détail dans la section suivante. si vous omettez cette étape, le générateur de Graph DVD sélectionne un convertisseur par défaut. Ensuite, générez le graphique en appelant la méthode [**IDvdGraphBuilder :: RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) .


```C++
AM_DVD_RENDERSTATUS buildStatus;
hr = pBuild->RenderDvdVideoVolume(L"Z:\\video_ts", 0, &buildStatus);
```



Le premier paramètre est le nom d’un répertoire qui contient les fichiers de DVD. Sur un disque DVD, ces fichiers résident dans un répertoire nommé VIDEO \_ TS. si le premier paramètre est **NULL**, le générateur de Graph dvd utilise le premier lecteur qui contient un volume DVD.

Le deuxième paramètre contient différents indicateurs facultatifs permettant de choisir le type de décodeur (matériel ou logiciel) et d’autres options.

Le troisième paramètre est une [**structure \_ \_ RENDERSTATUS de DVD am**](/windows/win32/api/strmif/ns-strmif-am_dvd_renderstatus) qui reçoit des informations d’État. Si la méthode [**RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume) retourne S \_ false, cela signifie que l’appel a été partiellement réussi (ou partiellement échoué, si vous êtes un pessimiste). Par exemple, la méthode peut ne pas réussir à restituer le flux de sous-image, même si les autres flux ont été restitués avec succès. Si la méthode **RenderDvdVideoVolume** retourne un code d’erreur ou si la valeur S \_ est false, vous pouvez examiner la structure **am \_ DVD \_ RENDERSTATUS** pour plus d’informations sur l’erreur.

ensuite, récupérez un pointeur vers le gestionnaire de Graph de filtre en appelant [**IDvdGraphBuilder :: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getfiltergraph). cette méthode retourne un pointeur vers l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) du gestionnaire de Graph de filtre.


```C++
IGraphBuilder *pGraph = NULL;
hr =  pBuild->GetFiltergraph(&m_pGraph);
```



Utilisez la méthode [**IDvdGraphBuilder :: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) pour récupérer des interfaces relatives aux DVD, y compris les éléments suivants :

-   [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2). Contrôle les commandes de lecture et de DVD
-   [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2). Retourne des informations sur l’état actuel du navigateur DVD.
-   [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder). Contrôle l’affichage de la légende fermée. L’affichage des sous-titres est activé par défaut. Pour le désactiver, appelez [**IAMLine21Decoder :: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) avec l' \_ indicateur AM L21 \_ CCSTATE \_ off.
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio). Contrôle le volume audio et l’équilibre.

Par exemple, le code suivant retourne l’interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .


```C++
IDvdControl2 *pDvdControl = NULL;
hr = pBuild->GetDvdInterface(IID_IDvdControl2, (void**)&pDvdControl);
```



la méthode recommandée pour générer le graphique de filtre de lecture de dvd consiste à faire en sorte qu’un objet [dvd Graph Builder](dvd-graph-builder.md) le fasse automatiquement. Cette approche est illustrée ci-dessous et dans l’exemple d’application de DVD. si vous avez besoin de créer votre graphique de filtre de DVD manuellement, vous pouvez le faire en suivant les règles de base de la création de graphiques présentées ailleurs dans la documentation de DirectShow. en règle générale, vous ne devez pas ajouter, supprimer, connecter ou déconnecter manuellement des filtres individuels dans le graphique créé par le générateur de Graph DVD, car cela peut entraîner une confusion dans le code de nettoyage.

Configuration du convertisseur vidéo

DirectShow fournit plusieurs filtres de convertisseur vidéo. Avant de générer le graphique, vous pouvez choisir le convertisseur vidéo que vous préférez. Sélectionnez le convertisseur en appelant [**IDvdGraphBuilder :: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) et en demandant une interface spécifique à ce convertisseur :

-   filtre de Mixer de superposition : [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo).
-   Convertisseur de mixage vidéo 7 (VMR-7) : [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig).
-   Convertisseur de mixage vidéo 9 (VMR-9) : [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9).
-   Rendu vidéo amélioré (EVR) : [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig).

si vous demandez l’une de ces interfaces avant de générer le graphique de filtre, le générateur de Graph DVD crée le convertisseur vidéo correspondant. plus tard, lorsque vous générerez le graphique, le générateur de Graph DVD essaiera d’utiliser ce convertisseur. Toutefois, s’il ne peut pas générer le graphique à l’aide du convertisseur que vous avez sélectionné, il peut basculer vers un autre convertisseur. par exemple, votre décodeur MPEG-2 peut ne pas être compatible avec le filtre VMR. dans ce cas, le générateur de Graph DVD est utilisé par défaut pour la superposition Mixer.

Ces interfaces vous donnent également la possibilité de configurer le convertisseur avant qu’il ne soit connecté au décodeur. Par exemple, vous pouvez configurer VMR pour utiliser le mode sans fenêtre au lieu du mode fenêtre par défaut. Pour plus d’informations sur les convertisseurs vidéo, consultez la rubrique [à propos du rendu vidéo dans DirectShow](about-video-rendering-in-directshow.md).

sur Windows XP et versions ultérieures, le générateur de DVD Graph utilise toujours le [convertisseur de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7), à moins que :

-   l’appelant interroge les interfaces uniquement la [superposition Mixer](overlay-mixer-filter.md), par exemple [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). cela envoie une indication au générateur de Graph DVD que l’application souhaite utiliser la superposition Mixer et non VMR. Lecteur Windows Media dispose également d’une option de boîte de dialogue pour forcer l’utilisation du Mixer de superposition.
-   Le décodeur installé n’est pas compatible avec VMR. Lors de la génération du graphique, la nouvelle interface [**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps) est utilisée pour vérifier la prise en charge VMR du décodeur. si ce n’est pas le cas, le générateur de DVD Graph utilise le Mixer de superposition.
-   Lors de l’utilisation d’un décodeur matériel, le décodeur ne peut pas se connecter au [Gestionnaire de port vidéo](video-port-manager.md) (VPM). si un décodeur matériel ne peut pas utiliser le VPM, il ne peut pas utiliser VMR, et par conséquent, le générateur de Graph DVD tente alors de créer un graphique à l’aide de la Mixer de superposition.
-   Les ressources et/ou les fonctionnalités de la carte d’affichage sont insuffisantes pour prendre en charge VMR, mais elles ne sont pas signalées correctement dans le pilote. (certains cas connus sont spécifiquement exclus par le générateur de DVD Graph.)
-   La connexion entre le décodeur et VMR échoue pour une raison quelconque, généralement en raison d’un manque de VRAM pour créer les surfaces nécessaires. dans ce cas, le générateur de Graph DVD désactive l’utilisation de VMR et tente d’utiliser l’Mixer de superposition pour créer un graphique.

Mode fenêtre

en mode fenêtre (superposition Mixer ou VMR), le convertisseur crée sa propre fenêtre vidéo. Pour faire de cette fenêtre un enfant de la fenêtre d’application, appelez [**IVideoWindow ::p ut \_ propriétaire**](/windows/desktop/api/Control/nf-control-ivideowindow-put_owner) avec un handle pour l’application. Appelez également [**IVideoWindow ::p ut \_ WindowStyle**](/windows/desktop/api/Control/nf-control-ivideowindow-put_windowstyle) pour définir les \_ styles WS Child et WS \_ CLIPSIBLINGS dans la fenêtre vidéo du convertisseur. Pour obtenir des messages de souris à partir de la fenêtre vidéo du convertisseur, appelez [**IVideoWindow ::p ut \_ MessageDrain**](/windows/desktop/api/Control/nf-control-ivideowindow-put_messagedrain) avec un handle vers la fenêtre d’application. Cette méthode configure un « drain de message »; la fenêtre vidéo transfère tous les messages de souris qu’elle reçoit vers la fenêtre drain de message.


```C++
pVideoWindow->put_Owner((OAHWND)hwnd);
pVideoWindow->put_WindowStyle(WS_CHILD | WS_CLIPSIBLINGS);
pVideoWindow->put_MessageDrain((OAHWND)hwnd) ;
```



Le vidage des messages permet de sélectionner des boutons de menu DVD quelque peu compliqués. En supposant que la fenêtre vidéo ne remplit pas l’intégralité de la zone cliente de l’application, certains événements de souris se situent en dehors de la fenêtre vidéo. Quand vous recevez un événement de souris *à partir de* la fenêtre vidéo, vous devez le traiter pour la navigation dans les menus DVD. Les événements de souris *en dehors* de la fenêtre vidéo ne doivent pas être traités. Avec la vidange de message, il n’existe aucun moyen de faire la distinction entre les deux. En outre, les coordonnées des événements de souris de la fenêtre vidéo sont relatives à la zone cliente de la fenêtre vidéo. Toutefois, les événements de souris en dehors de la fenêtre vidéo sont relatifs à la zone cliente de l’application.

Mode sans fenêtre

Le mode sans fenêtre évite les problèmes liés aux messages de la souris. Vous n’avez pas besoin d’un drain de message, car VMR (ou EVR) ne crée pas sa propre fenêtre en mode sans fenêtre. Au lieu de cela, il crée directement dans la fenêtre de votre application. Si le rectangle de destination est plus petit que la zone cliente de l’application, le navigateur DVD prend cela en compte lorsqu’il calcule les positions du bouton DVD. Par conséquent, lorsque vous recevez un message de souris, vous pouvez transmettre les coordonnées directement au navigateur DVD, comme décrit dans la section navigation dans les menus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 
