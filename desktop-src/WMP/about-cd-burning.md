---
title: À propos de la gravure de CD
description: À propos de la gravure de CD
ms.assetid: 1ecc73ed-c49d-4190-baa9-93162f075a4c
keywords:
- Lecteur Windows Media, gravure de CD
- Windows Media Player Object Model, gravage de CD
- modèle d’objet, gravage de CD
- Contrôle ActiveX du lecteur Windows Media, gravure de CD
- Contrôle ActiveX, gravage de CD
- Windows Media Player Mobile contrôle ActiveX, gravure de CD
- Lecteur Windows Media Mobile, gravure de CD
- Gravage de CD, à propos de
- gravure de CD, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc921080d02bef6ffbf916fe4d7d1df09f1e8bbc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724055"
---
# <a name="about-cd-burning"></a>À propos de la gravure de CD

Le kit de développement logiciel (SDK) du lecteur Windows Media 11 introduit de nouvelles fonctionnalités pour la création de CD. Ce processus s’appelle la *gravure*.

Pour énumérer les lecteurs de CD sur l’ordinateur de l’utilisateur, utilisez l’interface **IWMPCdromCollection** . Vous récupérez un pointeur vers cette interface en appelant [IWMPCore :: obtenir \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). En utilisant les méthodes **Count** et **Item** , vous pouvez effectuer une itération de la collection pour récupérer un pointeur d’interface **IWMPCDROM** pour chaque lecteur de CD sur l’ordinateur de l’utilisateur. L’interface **IWMPCdrom** représente un lecteur de CD individuel.

Avant de commencer à graver un CD, vous devez d’abord appeler **QueryInterface** à l’aide d’un pointeur **IWMPCdrom** pour récupérer un pointeur vers l’interface **IWMPCdromBurn** . À l’aide de la méthode **isAvailable** , vous pouvez déterminer si un lecteur de CD peut graver des CD, s’il y a un CD dans le lecteur et comment le CD peut être utilisé.

Pour spécifier les éléments à graver sur CD, vous devez créer une sélection. Le lecteur Windows Media représente des sélections à l’aide de l’interface **IWMPPlaylist** . Vous pouvez créer cette sélection comme vous le souhaitez. Par exemple, vous pouvez simplement récupérer une sélection à partir de la bibliothèque en appelant [IWMPMediaCollection :: getByAlbum](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum). Une fois que vous avez créé la sélection que vous souhaitez graver sur CD, vous devez appeler la méthode [IWMPCdromBurn ::p ut \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) et transmettre le pointeur de sélection en tant qu’argument. Cela définit votre sélection comme celle que le lecteur Windows Media copie sur le CD.

Si vous récupérez une sélection à partir de la bibliothèque, toute modification apportée à la sélection sera reflétée dans la bibliothèque de l’utilisateur. Pour éviter cela, appelez [IWMPPlaylist :: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo), en passant le nom d’attribut « Temporary » et la valeur « true ». Cela convertit votre instance de playlist en sélection temporaire, qui peut être modifiée sans modifier la sélection d’origine.

Chaque fois que vous définissez une nouvelle sélection pour la gravure ou que vous modifiez une sélection de gravure existante, vous devez appeler [IWMPCdromBurn :: refreshStatus](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) pour mettre à jour les informations d’État. Cela permet de s’assurer que le lecteur Windows Media effectue le traitement nécessaire pour obtenir des informations d’État précises sur l’opération de gravure de CD.

Pour spécifier le type de CD à graver, appelez [IWMPCdromBurn ::p ut \_ burnFormat](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat). Le lecteur Windows Media vous permet de graver deux types de CD : CD audio et CD de données. L’énumération [WMPBurnFormat](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat) définit les types de CD.

Vous pouvez spécifier un nom de volume pour le CD en appelant [IWMPCdromBurn ::p \_ ut](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label).

Quand vous êtes prêt à commencer la gravure du CD, appelez [IWMPCdromBurn :: startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn). Vous pouvez surveiller la progression de l’opération de gravure en appelant périodiquement [IWMPCdromBurn :: obten \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress). Cette méthode récupère une valeur de progression pour l’ensemble de l’opération de gravure. La valeur récupérée est un nombre qui représente le pourcentage de la gravure effectuée. Vous pouvez surveiller l’état de l’opération de gravure en gérant l’événement [IWMPEvents3 :: CdromBurnStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) , qui utilise l’énumération [WMPBurnState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) pour indiquer l’état actuel. Veillez à comparer le pointeur **IWMPCdromBurn** (fourni par l’événement) au pointeur qui représente votre opération de gravure pour vous assurer que l’événement a été déclenché par votre opération. Vous pouvez arrêter l’opération de gravure en appelant [IWMPCdromBurn :: stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).

Il existe deux événements que vous pouvez gérer pour recevoir des notifications d’erreurs relatives à votre opération de gravure. L’événement [IWMPEvents3 :: CdromBurnError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) est déclenché lorsqu’une erreur générique se produit. [IWMPEvents3 :: CdromBurnMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) est déclenché lorsqu’un élément multimédia particulier provoque une erreur lors de la gravure. À l’instar de l’événement **CdromBurnStateChange** , chacun de ces événements fournit un pointeur **IWMPCdromBurn** qui représente l’opération de gravure qui a déclenché l’événement. L’événement **CdromBurnMediaError** fournit un pointeur **IDispatch** qui représente l’élément multimédia qui a déclenché l’événement. Vous pouvez appeler **QueryInterface** via ce pointeur pour récupérer un pointeur **IWMPMedia** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du modèle objet Player**](about-the-player-object-model.md)
</dt> <dt>

[**Interface IWMPCdrom**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Interface IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
</dt> <dt>

[**Interface IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**Interface IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**Interface IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Interface IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Attribut temporaire**](temporary-attribute.md)
</dt> </dl>

 

 




