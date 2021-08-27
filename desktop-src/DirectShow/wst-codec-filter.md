---
description: Filtre de codec WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Filtre de codec WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e729e13500317711076f6cdbd39c9a6ab25bea77e8d378e12f917f2e20e4a561
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083449"
---
# <a name="wst-codec-filter"></a>Filtre de codec WST

> [!IMPORTANT]
> ce composant a été supprimé de Windows Vista et des systèmes d’exploitation ultérieurs. il peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.

 

à partir de Windows Vista, ce filtre est remplacé par le filtre VBICodec, qui est documenté dans la documentation Microsoft TV Technologies.

WST (World standard Teletext) est la norme européenne pour la transmission de données à l’aide de VBI sur des signaux de télévision analogiques PAL. Les services de sous-titrage et de données sont fournis à l’aide de cette norme. Le codec WST est un filtre en mode noyau qui reçoit des exemples bruts VBI et, éventuellement, des exemples de télétexte décodé à partir du filtre de capture via le filtre de [convertisseur tee/Sink-to-Sink](tee-sink-to-sink-converter.md) . Ce codec décode et/ou duplique les données de télétexte décodées et corrigées par erreur pour le filtre de [décodeur WST](wst-decoder-filter.md) . Le codec WST correspond au filtre de décodeur CC pour les transmissions NTSC. Le décodeur WST correspond au [décodeur de ligne 21](line-21-decoder-filter.md) pour NTSC ; ces filtres créent les bitmaps qui sont envoyés à la superposition Mixer ou le convertisseur de mixage vidéo.

Ce filtre a deux broches d’entrée, VBI et HWCC. Le code confidentiel VBI est utilisé pour les données de VBI brutes, et le code PIN HWCC est utilisé lorsque le décodage VBI est effectué dans le matériel par le filtre de capture. Lorsque les données sont reçues sur le code PIN HWCC, le codec WST fonctionne en mode « pass-through » et envoie les données directement au décodeur WST sans le traiter de quelque manière que ce soit. Si le filtre de capture expose un code confidentiel HWCC, il doit être connecté directement au code PIN correspondant sur le codec WST.

Le filtre de codec WST s’affiche dans la catégorie de filtre « codecs VBI de flux WDM » (**am \_ KSCATEGORY \_ VBICODEC**).

Étant donné qu’il s’agit d’un filtre en mode noyau, les applications ne peuvent pas la créer directement à l’aide de **CoCreateInstance**. Utilisez plutôt l' [énumérateur du périphérique système](system-device-enumerator.md). Pour plus d’informations, consultez [création de filtres de Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> <dt>

[Affichage du télétexte standard du monde](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



