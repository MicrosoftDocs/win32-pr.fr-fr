---
title: Flux audio
description: Flux audio
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Lecteur Windows Media des magasins en ligne, flux audio
- magasins en ligne, flux audio
- types 1 magasins en ligne, flux audio
- Lecteur Windows Media des magasins en ligne, des flux de serveurs musicaux
- magasins en ligne, flux de serveurs musicaux
- types 1 magasins en ligne, flux de serveurs musicaux
- Lecteur Windows Media des magasins en ligne, flux de serveurs de musique
- magasins en ligne, flux de serveurs de musique
- types 1 magasins en ligne, flux de serveur de musique
- flux audio
- flux de serveur de musique
- flux de serveurs musicaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856108"
---
# <a name="audio-streams"></a>Flux audio

Les magasins en ligne peuvent fournir de la musique sous forme de flux à partir d’un serveur de musique. Cela est utile pour fournir des exemples, des éléments promotionnels spéciaux ou pour permettre aux utilisateurs d’abonnements de profiter de la musique sans avoir à télécharger le contenu. Il est courant de ne pas stocker l’URL du flux en tant que partie du catalogue musical, mais de résoudre l’URL juste avant la lecture en fonction de l’ID de piste. pour ce faire, Lecteur Windows Media appelle [IWMPContentPartner :: GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) et fournit le type de diffusion en continu (en tant que valeur d’énumération [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) ) et l’ID du flux. Le plug-in retourne l’URL du flux via le paramètre *pbstrURL* .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




