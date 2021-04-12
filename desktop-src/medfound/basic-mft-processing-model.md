---
description: Cette rubrique décrit comment un client utilise une transformation de Media Foundation (MFT) pour traiter les données. Le client est tout ce qui appelle directement des méthodes sur la table MFT. Il peut s’agir de l’application ou du pipeline Media Foundation.
ms.assetid: be977d75-999e-4e57-9672-00a89246a2c1
title: Modèle de traitement MFT de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca54df6d9765aaf54456c3d9dc4461a82a93d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033821"
---
# <a name="basic-mft-processing-model"></a>Modèle de traitement MFT de base

Cette rubrique décrit comment un client utilise une transformation de Media Foundation (MFT) pour traiter les données. Le *client* est tout ce qui appelle directement des méthodes sur la table MFT. Il peut s’agir de l’application ou du pipeline Media Foundation.

Lisez cette rubrique si vous êtes :

-   Écriture d’une application qui effectue des appels directs à un ou plusieurs MFTs.
-   Écriture d’une table MFT personnalisée et compréhension du comportement attendu d’une table MFT.

Cette rubrique décrit un modèle de traitement *synchrone* . Dans ce modèle, toutes les méthodes de traitement des données sont bloquées jusqu’à ce qu’elles se terminent. MFTs peut également prendre en charge un modèle *asynchrone* , qui est décrit dans la rubrique [MFTS asynchrone](asynchronous-mfts.md).

-   [Modèle de traitement de base](#basic-processing-model)
    -   [Créer la table MFT](#create-the-mft)
    -   [Obtient les identificateurs de flux](#get-stream-identifiers)
    -   [Définir les types de médias](#set-media-types)
    -   [Connaître les exigences du tampon](#get-buffer-requirements)
    -   [Traiter des données](#process-data)
-   [Extensions du modèle de base](#extensions-to-the-basic-model)
-   [IMF2DBuffer](#imf2dbuffer)
-   [Vidage d’une table MFT](#flushing-an-mft)
-   [Vidage d’une table MFT](#draining-an-mft)
-   [Exemples d’attributs](#sample-attributes)
-   [Discontinuités](#discontinuities)
-   [Modifications de format dynamique](#dynamic-format-changes)
-   [Événements de flux](#stream-events)
-   [Rubriques connexes](#related-topics)

## <a name="basic-processing-model"></a>Modèle de traitement de base

### <a name="create-the-mft"></a>Créer la table MFT

Il existe plusieurs façons de créer une table MFT :

-   Appelez la fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) .
-   Appelez la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .
-   Si vous connaissez déjà le CLSID de la MFT, appelez simplement **CoCreateInstance**.

Certains MFTs peuvent fournir d’autres options, telles qu’une fonction de création spécialisée.

### <a name="get-stream-identifiers"></a>Obtient les identificateurs de flux

Une table MFT possède un ou plusieurs *flux*. Les flux d’entrée reçoivent des données d’entrée, et les flux de sortie génèrent des données de sortie. Les flux ne sont pas représentés en tant qu’objets distincts. Au lieu de cela, différentes méthodes MFT prennent des identificateurs de flux en tant que paramètres.

Certains MFTs permettent au client d’ajouter ou de supprimer des flux d’entrée. Pendant la diffusion en continu, une table MFT peut ajouter ou supprimer des flux de sortie. (Le client ne peut pas ajouter ou supprimer des flux de sortie.)

1.  (Facultatif.) Appelez [**IMFTransform :: GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits) pour connaître le nombre minimal et maximal de flux que la MFT peut prendre en charge. Si les valeurs minimale et maximale sont identiques, la table MFT a un nombre fixe de flux.
2.  Appelez [**IMFTransform :: GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) pour connaître le nombre initial de flux.
3.  Appelez [**IMFTransform :: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) pour récupérer les identificateurs de flux. Si cette méthode retourne E \_ NOTIMPL, cela signifie que la table MFT a un nombre fixe de flux et que les identificateurs de flux sont consécutifs à partir de zéro.
4.  (Facultatif.) Si la MFT n’a pas un nombre fixe de flux, appelez [**IMFTransform :: AddInputStreams**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-addinputstreams) pour ajouter d’autres flux d’entrée, ou [**IMFTransform ::D eleteinputstream**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream) pour supprimer des flux d’entrée. (Vous ne pouvez pas ajouter ou supprimer des flux de sortie.)

### <a name="set-media-types"></a>Définir les types de médias

Avant qu’une table MFT puisse traiter des données, le client doit définir des types de médias pour chacun des flux de la table MFT. Une table MFT peut nécessiter que le client définisse les types d’entrée avant de définir les types de sortie, ou qu’il ait besoin de l’ordre inverse (types de sortie en premier). Certains MFTs n’ont pas d’exigence sur la commande.

Une table MFT peut fournir une liste de types de médias préférés pour un flux. En outre, MFTs peut indiquer les formats généraux qu’ils prennent en charge en ajoutant ces informations au registre.

Pour définir les types de médias, procédez comme suit :

1.  (Facultatif.) Pour chaque flux d’entrée, appelez [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) pour obtenir la liste des types préférés pour ce flux.
    -   Si cette méthode retourne \_ \_ le type de transformation MF E \_ \_ non \_ défini, vous devez d’abord définir les types de sortie ; passez à l’étape 3.
    -   Si la méthode retourne E \_ NOTIMPL, la MFT n’a pas de liste de types d’entrée préférés ; passez à l’étape 2.
2.  Pour chaque flux d’entrée, appelez [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) pour définir le type d’entrée. Vous pouvez utiliser un type de média de l’étape 1 ou un type qui décrit vos données d’entrée. Si un flux retourne le \_ type de transformation MF E \_ \_ \_ non \_ défini, passez à l’étape 3.
3.  (Facultatif.) Pour chaque flux de sortie, appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour obtenir la liste des types préférés pour ce flux.
    -   Si cette méthode retourne \_ \_ le type de transformation MF E \_ \_ non \_ défini, vous devez d’abord définir les types d’entrée, puis revenir à l’étape 1.
    -   Si un flux retourne E \_ NOTIMPL, la MFT n’a pas de liste de types de sortie préférés ; passez à l’étape 4.
4.  Pour chaque flux de sortie, appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) pour définir le type de sortie. Vous pouvez utiliser un type de média de l’étape 3 ou un type qui décrit le format de sortie requis.
5.  Si des flux d’entrée n’ont pas de type de média, revenez à l’étape 1.

### <a name="get-buffer-requirements"></a>Connaître les exigences du tampon

Une fois que le client a défini les types de médias, il doit obtenir les exigences de mémoire tampon pour chaque flux :

-   Pour chaque flux d’entrée, appelez [**IMFTransform :: GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo).
-   Pour chaque flux de sortie, appelez [**IMFTransform :: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).

### <a name="process-data"></a>Traiter les données

Un MFT est conçu pour être un ordinateur d’état fiable. Il n’effectue aucun rappel au client.

1.  Appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message [**MFT \_ message de début de diffusion en \_ \_ \_ continu**](mft-message-notify-begin-streaming.md) . Ce message demande à la MFT d’allouer toutes les ressources dont elle a besoin lors de la diffusion en continu.
2.  Appelez [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) sur au moins un flux d’entrée pour remettre un exemple d’entrée à la table MFT.
3.  (Facultatif.) Appelez [**IMFTransform :: GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus) pour demander si la table MFT peut générer un exemple de sortie. Si la méthode retourne la valeur \_ OK, vérifiez le paramètre *pdwFlags* . Si *pdwFlags* contient l’indicateur de préparation de l' **\_ exemple d’état de sortie \_ \_ \_ MFT** , passez à l’étape 4. Si *pdwFlags* est égal à zéro, revenez à l’étape 2. Si la méthode retourne E \_ NOTIMPL, passez à l’étape 4.
4.  Appelez [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) pour accéder aux données de sortie.
    -   Si la méthode retourne **la \_ transformation MF E nécessite \_ \_ \_ plus \_ d’entrées**, cela signifie que la table MFT requiert davantage de données d’entrée ; revenez à l’étape 2.
    -   Si la méthode retourne **la \_ \_ modification du \_ flux \_ de transformation MF E**, cela signifie que le nombre de flux de sortie a changé ou que le format de sortie a changé. Le client peut avoir besoin d’interroger de nouveaux identificateurs de flux ou de définir de nouveaux types de médias. Pour plus d’informations, consultez la documentation de [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).
5.  Si des données sont toujours entrées à traiter, passez à l’étape 2. Si la MFT a consommé toutes les données d’entrée disponibles, passez à l’étape 6.
6.  Appelez [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le [**message \_ \_ de la \_ fin de la notification de la fin \_ du \_ flux du message MFT**](mft-message-notify-end-of-stream.md) .
7.  Appelez [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de [**\_ drainage de \_ commande \_ de message MFT**](mft-message-command-drain.md) .
8.  Appelez [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) pour récupérer la sortie restante. Répétez cette étape jusqu’à ce que la méthode retourne **MF \_ E \_ Transform \_ ait besoin \_ d’une \_ entrée supplémentaire**. Cette valeur de retour signale que toutes les sorties ont été vidées de la MFT. (Ne traitez pas ceci comme une condition d’erreur.)

La séquence décrite ici conserve le moins de données possible dans la table MFT. Après chaque appel à [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), le client tente d’accéder à la sortie. Plusieurs exemples d’entrée peuvent être nécessaires pour produire un échantillon de sortie, ou un exemple d’entrée unique peut générer plusieurs exemples de sortie. Le comportement optimal pour le client consiste à extraire des échantillons de sortie de la MFT jusqu’à ce que la MFT nécessite davantage d’entrées.

Toutefois, la table MFT doit pouvoir gérer un ordre différent des appels de méthode par le client. Par exemple, le client peut simplement alterner entre les appels à [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) et [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). La table MFT doit limiter la quantité d’entrée qu’elle obtient en retournant **MF \_ E \_ NOTACCEPTING** à partir de **ProcessInput** chaque fois qu’elle a une sortie à produire.

L’ordre des appels de méthode décrits ici n’est pas la seule séquence d’événements valide. Par exemple, les étapes 3 et 4 supposent que le client commence par les types d’entrée, puis essaie les types de sortie. Le client peut également inverser cet ordre et démarrer avec les types de sortie. Dans les deux cas, si la table MFT requiert l’ordre inverse, elle doit retourner le code d’erreur « \_ type de transformation MF E \_ \_ \_ non défini » \_ .

Le client peut appeler des méthodes d’information, telles que [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype) et [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo), à tout moment pendant la diffusion en continu. Le client peut également tenter de modifier les types de média à tout moment. La table MFT doit retourner un code d’erreur s’il ne s’agit pas d’une opération valide. En bref, MFTs doit assumer très peu l’ordre des opérations, à l’exception de ce qui est documenté dans les appels eux-mêmes.

Le diagramme suivant montre un organigramme des procédures décrites dans cette rubrique.

![organigramme qui amène à recevoir des identificateurs de flux par le biais de boucles qui définissent les types d’entrée, obtiennent une entrée et traitent la sortie](images/mft-processing.gif)

## <a name="extensions-to-the-basic-model"></a>Extensions du modèle de base

Éventuellement, une table MFT peut prendre en charge certaines extensions du modèle de diffusion en continu de base.

-   Flux de lecture tardive. Si la méthode [**IMFTransform :: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) retourne l’indicateur de **\_ \_ \_ \_ lecture tardive du flux de sortie MFT** pour un flux de sortie, le client n’a pas besoin de collecter des données à partir de ce flux de sortie. La table MFT continue d’accepter les entrées et, à un moment donné, la table MFT ignore les données de sortie de ce flux. Si tous les flux de sortie ont cet indicateur, le MFT n’arrivera jamais à accepter l’entrée. Il peut s’agir, par exemple, d’une transformation de visualisation, où le client obtient la sortie uniquement lorsqu’elle a des cycles d’UC de rechange pour dessiner la visualisation.
-   Flux ignorables. Si la méthode [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) retourne l’indicateur de suppression de **\_ \_ flux \_ de sortie MFT** pour un flux de sortie, le client peut demander à la MFT d’ignorer la sortie, mais la table MFT n’ignore aucune sortie, sauf si elle est demandée. Lorsque la table MFT atteint sa mémoire tampon d’entrée maximale, le client doit collecter des données de sortie ou demander à la MFT d’ignorer la sortie.
-   Flux facultatifs. Si la méthode [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) retourne l' **indicateur \_ \_ \_ facultatif du flux de sortie MFT** pour un flux de sortie, ou si la méthode [**IMFTransform :: GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo) retourne l’indicateur **\_ \_ \_ facultatif de flux d’entrée MFT** pour un flux d’entrée, ce flux est facultatif. Le client n’a pas besoin de définir un type de média sur le flux. Si le client ne définit pas le type, le flux est désélectionné. Un flux de sortie désélectionné ne produit pas d’exemples et le client ne fournit pas de mémoire tampon pour le flux lors de l’appel de [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Un flux d’entrée désélectionné n’accepte pas les données d’entrée. Une table MFT peut marquer tous ses flux d’entrée et de sortie comme facultatifs. Toutefois, il est prévu qu’au moins une entrée et une sortie doivent être sélectionnées pour que la MFT fonctionne.
-   Traitement asynchrone. Le modèle de traitement asynchrone a été introduit dans Windows 7. Elle est décrite dans la rubrique [MFTS asynchrone](asynchronous-mfts.md).

## <a name="imf2dbuffer"></a>IMF2DBuffer

Si une table MFT traite des données vidéo non compressées, elle doit utiliser l’interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) pour manipuler les exemples de mémoires tampons. Pour obtenir cette interface, interrogez l’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) sur n’importe quelle mémoire tampon d’entrée ou de sortie. Si cette interface n’est pas utilisée, cela peut entraîner des copies supplémentaires de la mémoire tampon. Pour utiliser correctement cette interface, la transformation ne doit pas verrouiller la mémoire tampon à l’aide de l’interface **IMFMediaBuffer** lorsque **IMF2DBuffer** est disponible.

Pour plus d’informations sur le traitement des données vidéo, consultez [mémoires tampons vidéo non compressées](uncompressed-video-buffers.md).

## <a name="flushing-an-mft"></a>Vidage d’une table MFT

Le *vidage* d’une table MFT entraîne l’annulation de toutes ses données d’entrée par la MFT. Cela peut provoquer une rupture dans le flux de sortie. Un client vide généralement un MFT avant de rechercher un nouveau point dans le flux d’entrée ou de basculer vers un nouveau flux d’entrée, lorsque le client ne se soucie pas de la perte de données.

Pour vider une table MFT, appelez [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de vidage de la [**\_ \_ commande \_ MFT message**](mft-message-command-flush.md) .

## <a name="draining-an-mft"></a>Vidage d’une table MFT

Le *vidage* d’une table MFT fait que la table MFT produit autant de sortie que possible, quelles que soient les données d’entrée déjà envoyées. Si la table MFT ne peut pas générer un exemple complet de sortie à partir de l’entrée disponible, elle supprimera les données d’entrée. Un client draine généralement une table MFT lorsqu’elle a atteint la fin du flux source, ou immédiatement avant une modification de format dans le flux source. Pour vider une table MFT, procédez comme suit :

1.  Appelez [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) avec le message de [**\_ drainage de \_ commande \_ de message MFT**](mft-message-command-drain.md) . Ce message indique au MFT qu’il doit fournir autant de données de sortie qu’il le peut à partir des données d’entrée qui ont déjà été envoyées.
2.  Appelez [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) pour obtenir les données de sortie, jusqu’à ce que la méthode retourne **MF \_ E \_ Transform \_ nécessite \_ plus \_ d’entrée**.

Pendant que la MFT est vidée, elle n’accepte plus d’entrée.

## <a name="sample-attributes"></a>Exemples d’attributs

Les exemples d’entrée peuvent avoir des attributs qui doivent être copiés dans les exemples de sortie correspondants.

-   Si la table MFT retourne la **\_ valeur variant true** pour la propriété [**MFPKEY \_ exattribute \_ pris en charge**](mfpkey-exattribute-supported-property.md) , la table MFT doit copier les attributs.
-   Si la propriété [**MFPKEY \_ exattribute \_ prise en charge**](mfpkey-exattribute-supported-property.md) est de **type Variant \_ false** ou n’est pas définie, le client doit copier les attributs.

Pour une table MFT avec une entrée et une sortie, vous pouvez utiliser la règle générale suivante :

-   Si chaque exemple d’entrée produit exactement un échantillon de sortie, vous pouvez laisser le client copier les attributs. Laissez la [**propriété \_ \_ prise en charge MFPKEY exattribute**](mfpkey-exattribute-supported-property.md) non définie.
-   S’il n’existe pas de correspondance un-à-un entre les exemples d’entrée et les exemples de sortie, la MFT doit déterminer les attributs corrects pour les exemples de sortie. Affectez à la propriété [**MFPKEY des \_ attributs \_ pris en charge**](mfpkey-exattribute-supported-property.md) la **\_ valeur variant true**.

## <a name="discontinuities"></a>Discontinuités

Une discontinuation est une rupture dans un flux audio ou vidéo. Les discontinuités peuvent être provoquées par des paquets supprimés sur une connexion réseau, des données de fichier endommagées, un basculement d’un flux source à un autre ou une large gamme d’autres causes. Les discontinuités sont signalées en définissant l’attribut de [**\_ discontinuité MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) sur le premier échantillon après la discontinuation. Il n’est pas possible de signaler une discontinuité au milieu d’un exemple. Par conséquent, toutes les données discontinues doivent être envoyées dans des exemples séparés.

Certaines transformations, en particulier celles qui gèrent des données non compressées, telles que des effets audio et vidéo, doivent ignorer les discontinuités lorsqu’elles traitent des données d’entrée. Ces MFTs sont généralement conçues pour gérer des données continues et doivent traiter toutes les données qu’elles reçoivent comme continues, même après une discontinuité.

Si une table MFT ignore une discontinuité sur les données d’entrée, elle doit toujours définir l’indicateur de discontinuité sur l’exemple de sortie, si l’exemple de sortie a le même horodatage que l’exemple d’entrée. Toutefois, si l’exemple de sortie a un horodatage différent, la table MFT ne doit pas propager la discontinuité. (Cela peut être le cas dans certains rééchantillonneurs audio, par exemple). Une discontinuité au mauvais endroit dans le flux est plus mauvais qu’aucune discontinuation.

La plupart des décodeurs ne peuvent pas ignorer les discontinuités, car une discontinuation affecte l’interprétation de l’exemple suivant. Toute technologie d’encodage qui utilise la compression inter-frame, telle que MPEG-2, est incluse dans cette catégorie. Certains schémas d’encodage utilisent uniquement la compression intra-image, par exemple DV et MJPEG. Ces décodeurs peuvent ignorer en toute sécurité les discontinuités.

Les transformations qui répondent aux discontinuités doivent généralement sortir autant de données avant la discontinuation qu’elles le peuvent et ignorer le reste. L’exemple d’entrée avec l’indicateur de discontinuation doit être traité comme s’il s’agissait du premier exemple dans le flux. (Ce comportement correspond à ce qui est spécifié pour le message de drainage de la [**\_ commande de message \_ \_ MFT**](mft-message-command-drain.md) .) Toutefois, les détails exacts dépendent du format du média.

Si un décodeur ne fait rien pour atténuer une discontinuité, il doit copier l’indicateur de discontinuité dans les données de sortie. Les démultiplexeurs et les autres MFTs qui fonctionnent entièrement avec des données compressées doivent copier les discontinuités dans leurs flux de sortie. Dans le cas contraire, les composants en aval ne seront peut-être pas en mesure de décoder correctement les données compressées. En général, il est presque toujours correct de passer les discontinuités en aval, à moins que la table MFT contienne du code explicite pour atténuer les discontinuités.

## <a name="dynamic-format-changes"></a>Modifications de format dynamique

Les formats peuvent changer pendant la diffusion en continu. Par exemple, les proportions peuvent changer au milieu d’un flux vidéo.

Pour plus d’informations sur la façon dont les modifications de flux de données sont gérées par une table MFT, consultez [gestion des modifications de flux](handling-stream-changes.md).

## <a name="stream-events"></a>Événements de flux

Pour envoyer un événement à une table MFT, appelez [**IMFTransform ::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent). Si la méthode retourne **l' \_ événement de transformation MF S \_ \_ ne \_ pas se \_ propager \_**, la table MFT retourne l’événement à l’appelant lors d’un appel ultérieur à [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Si la méthode retourne une autre valeur **HRESULT** , la table MFT ne retourne pas l’événement au client dans **ProcessOutput**. Dans ce cas, le client est chargé de propager l’événement en aval au composant suivant dans le pipeline, le cas échéant. Pour plus d’informations, consultez [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



