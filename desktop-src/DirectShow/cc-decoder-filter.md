---
description: Filtre de décodeur CC
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: Filtre de décodeur CC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950036"
---
# <a name="cc-decoder-filter"></a>Filtre de décodeur CC

> [!IMPORTANT]
> Ce composant a été supprimé de Windows Vista et des systèmes d’exploitation ultérieurs. Il peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.

 

Le décodeur CC VBI est un filtre de classe de flux en mode noyau. Il apparaît dans GraphEdit sous la catégorie « codecs VBI de streaming WDM ». Il accepte les exemples d’onde fournis par un filtre de capture et fournit des données décodées de sous-titrage au [décodeur de ligne 21](line-21-decoder-filter.md) et/ou aux applications intéressées.

Ce filtre a deux broches d’entrée, VBI et HWCC. Le code confidentiel VBI est utilisé pour les données de VBI brutes, et le code PIN HWCC est utilisé lorsque le décodage VBI est effectué dans le matériel par le filtre de capture. Lorsque les données sont reçues sur le code confidentiel HWCC, le décodeur CC fonctionne en mode « pass-through » et envoie les données directement au décodeur de ligne 21 sans le traiter de quelque manière que ce soit. Si le filtre de capture expose un code confidentiel HWCC, il doit être connecté directement au code PIN correspondant sur le décodeur CC. La catégorie pin est **PINNAME \_ vidéo \_ cc \_ capture**.

Le décodeur CC contient jusqu’à huit broches de sortie, chacune pouvant sélectionner ses propres lignes et sous-flux. La première broche de sortie est connectée au décodeur Line-21.

Le filtre de décodeur CC apparaît dans la catégorie de filtre « codecs VBI de flux WDM » (**am \_ KSCATEGORY \_ VBICODEC**).

Étant donné qu’il s’agit d’un filtre en mode noyau, les applications ne peuvent pas la créer directement à l’aide de **CoCreateInstance**. Utilisez plutôt l' [énumérateur du périphérique système](system-device-enumerator.md). Pour plus d’informations, consultez [création de filtres de Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> <dt>

[Affichage des sous-titres](viewing-closed-captions.md)
</dt> </dl>

 

 



