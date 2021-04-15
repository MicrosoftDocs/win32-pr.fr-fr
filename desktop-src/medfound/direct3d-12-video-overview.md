---
description: Cet article contient des conseils généraux sur l’utilisation des API vidéo Direct3D 12.
ms.assetid: ''
title: Vue d’ensemble vidéo Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: b21587f2784b34131da9c050655b6f3fbe43582d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524564"
---
# <a name="direct3d-12-video-overview"></a>Vue d’ensemble vidéo Direct3D 12

Cet article contient des conseils généraux sur l’utilisation des API vidéo Direct3D 12.

## <a name="about-direct3d-12-video"></a>À propos de la vidéo Direct3D 12

L’interface vidéo Direct3D 12 offre aux applications une nouvelle façon d’implémenter le décodage et le traitement de vidéos. L’interface Direct3D 12 est différente de l’interface Direct3D 11 précédente, car elle a été conçue pour être cohérente avec les principes et le style Direct3D 12, qui incluent les éléments suivants :

- Donnez plus de contrôle aux développeurs
 - Allocation de mémoire accessible sur le matériel
 - Threads d’UC utilisés pour générer & les commandes Submit
   - Génération et soumission indépendantes
   - Non bloquant
 - Planification du travail matériel
- Aborde les fonctionnalités existantes, y compris la plupart des fonctionnalités vidéo de Direct3D 11, mais en même temps, la simplicité et la facilité d’utilisation sont à l’esprit.
- Puissance et performances des applications Direct3D 12 principales égales ou supérieures à Direct3D 11
- Cohérence avec les autres API Direct3D 12
- Interopérabilité avec les API Graphics existantes


## <a name="video-decoding"></a>Décodage vidéo

Les sections suivantes décrivent certaines des tâches impliquées dans l’implémentation du décodage vidéo Direct3D 12.

### <a name="query-for-decoding-capabilities"></a>Interroger les fonctionnalités de décodage

Appelez [ID3D12VideoDevice :: CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) pour vérifier les détails de prise en charge des opérations de décodage vidéo Direct3D 12. Transmettez une valeur de l’énumération [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) pour spécifier la fonctionnalité pour laquelle vous demandez des informations de support.

### <a name="create-the-video-decoder"></a>Créer le décodeur vidéo

Appelez [ID3D12VideoDevice :: CreateVideoDecoder](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder) pour créer une instance de l’interface [ID3D12VideoDecoder](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder) . Le décodeur conserve l’état d’une session de décodage, y compris les données liées à la référence, telles que les vecteurs de mouvement.  En cas de modification de la résolution ou de modification d’un [MaxDecodePictureBufferCount](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc) , l’objet décodeur est recréé. La largeur et la hauteur de décodage spécifient la résolution du flux natif avant toute échelle.  Le nombre maximal de tampons d’images décodés (DPB) spécifie le plus grand nombre de DPB qui peut être utilisé sans recréer le décodeur vidéo.

Le décodeur peut être utilisé pour enregistrer des commandes à partir de plusieurs listes de commandes, mais il ne peut être associé qu’à une seule liste de commandes à la fois.  L’application est chargée de synchroniser l’accès au décodeur.

### <a name="create-the-video-decoder-heap"></a>Créer le tas du décodeur vidéo 

Appelez [ID3D12VideoDevice :: CreateVideoDecoderHeap](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) pour créer une instance de l’interface [ID3D12VideoDecoderHeap](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoderheap) . Cet objet contient les ressources et l’état des pilotes dépendants de la résolution.

### <a name="decoding-a-frame"></a>Décodage d’un frame

Tous les paramètres d’entrée et de sortie pour les opérations de traitement vidéo sont organisés dans une structure de paramètres d’entrée, [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)et une structure de paramètre de sortie, [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments).
L’application gère les frames de référence et, par conséquent, doit définir les frames de référence pour chaque opération de décodage.
Lorsque la liste de commandes est correctement enregistrée, appelez [ID3D12CommandQueue :: ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) dans la file d’attente de commandes vidéo pour envoyer le décodage de trame au GPU.


### <a name="enabling-decoder-output-conversions"></a>Activation des conversions de sortie du décodeur
Si le décodeur prend en charge la conversion, activez les conversions souhaitées en remplissant correctement la structure [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) . Le format et les résolutions de la sortie souhaitée par rapport à la sortie native du décodeur sont communiqués via la différence dans l’espace de couleurs et les résolutions spécifiées dans les paramètres de conversion.

##  <a name="querying-decoding-status"></a>Interrogation de l’état de décodage 
Utilisez les méthodes [ID3D12VideoDecodeCommandList :: BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery) et [ID3D12VideoDecodeCommandList :: EndQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery) pour interroger l’état de l’opération de décodage.

La structure [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics) est utilisée pour décrire les statistiques de décodage vidéo. Pour obtenir une instance de cette structure, appelez [ID3D12VideoDecodeCommandList :: EndQuery](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery), en passant la valeur de type de requête du tas de [D3D12_QUERY_TYPE_VIDEO_DECODE_STATISTIC](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Notez que cette requête n’utilise pas [ID3D12VideoDecodeCommandList :: BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery).

## <a name="video-processing"></a>Traitement vidéo

Les API vidéo Direct3D 12 adoptent une approche rationalisée pour le traitement vidéo, en éliminant les fonctionnalités de Direct3D 11 qui n’étaient pas largement utilisées et qui suppriment les vérifications de fonctionnalité pour les fonctionnalités qui sont obligatoires sur les appareils. Le processus d’énumération pour le traitement vidéo est éliminé. Au lieu de cela, appelez [ID3D12VideoDevice :: CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) , ce qui permet à une application d’identifier les fonctionnalités du processeur vidéo. La vidéo souhaitée, les formats d’entrelacement, les formats stéréo et les tarifs sont fournis comme entrée pour **CheckFeatureSupport**.

### <a name="removed-capabilities"></a>Fonctionnalités supprimées

Les fonctionnalités suivantes de Direct3D 11 ne sont pas prises en charge dans le traitement vidéo Direct3D 12 :
- Tarifs personnalisés.  Au lieu de cela, il existe un taux d’entrée et de sortie donné lors de l’enregistrement de commande [ID3D12VideoProcessCommandList ::P rocessframes](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) .
- Il n’y a que deux modes de désentrelacement disponibles maintenant : [Bob](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) et [personnalisé](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags). D’autres modes ont été éliminés. PERSONNALISÉ est un mode de désentrelacement de haute qualité fourni par le fournisseur de matériel.
- Tous les formats stéréo facultatifs dans [D3D11_VIDEO_PROCESSOR_STEREO_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_caps) ne sont plus pris en charge. Au lieu de cela, [nono](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format), [horizontal](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format), [vertical](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)et [distinct](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) sont obligatoires pour tous les périphériques matériels si le stéréo est pris en charge.
- Il n’existe aucun équivalent pour [D3D11_VIDEO_PROCESSOR_FORMAT_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_caps) ou [D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps). Au lieu de cela, les formats d’entrée et de sortie sont des arguments pour la création du processeur vidéo et, à ce moment-là, il doit être connu si le processeur vidéo peut ou ne peut pas effectuer l’opération avec le format donné. Le [D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_auto_processing_flags) est utilisé pour indiquer si les fonctionnalités de traitement automatique sont disponibles.
- Il n’existe aucun équivalent pour [D3D11_VIDEO_PROCESSOR_CAPS_LEGACY](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- Il n’existe aucun équivalent pour [D3D11_VIDEO_PROCESSOR_CAPS_CONSTRICTION](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- Lors de la conversion d’un stéréo en mono, nous supposons que la vue de ligne de base est 0.
- Le traitement vidéo Direct3D 12 ne prend pas en charge la conversion de mono en stéréo et il n’existe pas de prise en charge du décalage mono. 


### <a name="creating-a-video-processor"></a>Création d’un processeur vidéo

Appelez [ID3D12VideoDevice :: CreateVideoProcessor](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor) pour créer une instance du [ID3D12VideoProcessor](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocessor). Le processeur vidéo conserve l’état d’une session de traitement vidéo, y compris la mémoire intermédiaire requise, les données de traitement mises en cache ou un autre espace de travail temporaire. Les arguments de création du processeur vidéo spécifient les opérations qui sont effectuées ou disponibles à [ID3D12VideoProcessCommandList1 ::P rocessframes1](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) .  Les allocations de pilotes pour effectuer l’opération de traitement vidéo (par exemple, intermédiaires) sont allouées au moment de la création du processeur vidéo.  Utilisez [D3D12_FEATURE_VIDEO_PROCESSOR_SIZE](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) pour déterminer la taille d’allocation du processeur vidéo à l’avance.

Le processeur vidéo peut uniquement être utilisé pour enregistrer des commandes à partir de plusieurs listes de commandes, mais il ne peut être associé qu’à une seule liste de commandes à la fois.  L’application est chargée de synchroniser l’accès au processeur vidéo.  L’application doit également enregistrer les commandes de traitement vidéo sur la vidéo procoessor dans l’ordre dans lequel elles sont exécutées sur le GPU.

Tous les arguments d’entrée et de sortie pour les opérations de traitement vidéo sont organisés dans une structure d’arguments d’entrée, [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)et une structure d’argument de sortie, [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments). L’application doit appeler [ID3D12VideoProcessCommandList ::P rocessframes](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) pour enregistrer l’opération de traitement vidéo qu’elle souhaite exécuter. 

Lors de l’enregistrement de la liste de commandes, appelez [ID3D12CommandQueue :: ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) dans la file d’attente de commandes vidéo pour envoyer le traitement du frame au GPU.


## <a name="tiers"></a>Niveaux

La vidéo Direct3D 12 définit des niveaux qui regroupent les fonctionnalités des périphériques matériels, afin que l’application puisse avoir moins de chemins de code pour répondre à la variété du matériel. Les niveaux sont spécifiés avec l’énumération [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier) .

Dans tous les niveaux, les éléments suivants sont disponibles :

- Vous n’avez pas besoin de recréation de décodeur pour les modifications de résolution. Seul le tas du décodeur doit être recréé lors de la modification de la résolution.
- Tous les frames de référence seront gérés par l’application. Cela permet au système d’économiser de la mémoire, car nous n’avons pas besoin d’allouer le nombre maximal de DPBs au moment de la création du décodeur dans certains niveaux, et offre aux applications une plus grande flexibilité dans les scénarios changeants de résolution.

Notez que les niveaux sont des superensembles. Une application peut décider d’effectuer le niveau 1 et ne pas utiliser les fonctionnalités de niveau supérieur, ce qui est autorisé, mais peut ne pas fournir de performances optimales. Pour plus d’informations sur les fonctionnalités associées aux différents niveaux de niveau, consultez [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier).

## <a name="reference-frames"></a>Frames de référence

Avec Direct3D 12 Video, les frames de référence sont passés explicitement. Cela permet d’effacer l’utilisation d’un tableau de textures ou de tableaux de texture lors du décodage des frames. L’application n’est pas obligée de passer exactement le même descripteur de ressource lorsqu’elle est utilisée comme référence. par exemple, il peut décider de copier une ressource dans une autre, puis de la transmettre à la place de la copie d’origine. Les index DXVA *RefFrameList* et *CurrPic* sont toujours utilisés par le pilote pour stocker les données pertinentes pour chaque trame décodée.


## <a name="directx-12-fences"></a>Limites DirectX 12

Dans DirectX 12, l’application est chargée de synchroniser l’accès à leurs tampons. Pour le cas de décodage, il est nécessaire d’ajouter des délimiteurs aux mémoires tampons d’entrée et aux mémoires tampons de sortie. Chaque clôture est associée à une valeur et est utilisée pour la synchronisation de l’UC et des moteurs matériels. Pour plus d’informations, consultez [utilisation de barrières de ressources pour synchroniser les États des ressources dans Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12).

Une implémentation classique aura une clôture pour chaque mémoire tampon d’entrée. Dans le cas des mémoires tampons d’entrée, il est possible que la mémoire tampon soit disponible avant l’exécution de l’ensemble du processus de décodage. Le système ignore ce cas et suppose que la mémoire tampon d’entrée est disponible lorsque le décodage est terminé.
Une implémentation aura également une clôture pour chaque mémoire tampon de sortie. Dans le cas de l’envoi de la sortie au compositeur, par exemple, une clôture est signalée lorsque cette présentation de ce frame est terminée, ce qui indique que la sortie est de nouveau disponible pour le décodeur.


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>API vidéo Direct3D 
[12](direct3d-12-video-apis.md) 
 [Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 
