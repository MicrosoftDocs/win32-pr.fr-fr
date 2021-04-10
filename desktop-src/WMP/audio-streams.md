---
title: Flux audio
description: Flux audio
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Windows Media Player Online stores, flux audio
- magasins en ligne, flux audio
- types 1 magasins en ligne, flux audio
- Windows Media Player Online stores, flux de serveurs musicaux
- magasins en ligne, flux de serveurs musicaux
- types 1 magasins en ligne, flux de serveurs musicaux
- Magasins en ligne du lecteur Windows Media, flux de serveur de musique
- magasins en ligne, flux de serveurs de musique
- types 1 magasins en ligne, flux de serveur de musique
- flux audio
- flux de serveur de musique
- flux de serveurs musicaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030829"
---
# <a name="audio-streams"></a>Flux audio

Les magasins en ligne peuvent fournir de la musique sous forme de flux à partir d’un serveur de musique. Cela est utile pour fournir des exemples, des éléments promotionnels spéciaux ou pour permettre aux utilisateurs d’abonnements de profiter de la musique sans avoir à télécharger le contenu. Il est courant de ne pas stocker l’URL du flux en tant que partie du catalogue musical, mais de résoudre l’URL juste avant la lecture en fonction de l’ID de piste. Pour activer cette fonction, le lecteur Windows Media appelle [IWMPContentPartner :: GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) et fournit le type de diffusion en continu (en tant que valeur d’énumération [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) ) et l’ID du flux. Le plug-in retourne l’URL du flux via le paramètre *pbstrURL* .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




