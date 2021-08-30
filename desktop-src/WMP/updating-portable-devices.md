---
title: Mise à jour des appareils mobiles
description: Mise à jour des appareils mobiles
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Lecteur Windows Media des magasins en ligne, mise à jour des appareils mobiles
- magasins en ligne, mise à jour des appareils mobiles
- tapez 1 magasins en ligne, mise à jour des appareils portables
- Lecteur Windows Media des magasins en ligne et des appareils mobiles
- magasins en ligne, appareils mobiles
- tapez 1 magasins en ligne, appareils mobiles
- mise à jour des appareils mobiles
- appareils mobiles, mise à jour
- appareils mobiles, Lecteur Windows Media magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6abc07eeecd61d287308bcc256c01f321219968d33d400b5b79aeff33d9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001659"
---
# <a name="updating-portable-devices"></a>Mise à jour des appareils mobiles

Lecteur Windows Media permet aux utilisateurs de synchroniser le contenu multimédia numérique avec des appareils mobiles. Cela peut inclure du contenu musical acheté ou loué à partir d’un magasin en ligne. Dans certains cas, les fournisseurs de magasins en ligne peuvent souhaiter écrire du code pour travailler sur un appareil mobile connecté dans le cadre de la gestion du contenu fourni par le magasin. pour permettre au plug-in de la boutique en ligne de travailler avec un appareil connecté, Lecteur Windows Media appelle [IWMPContentPartner :: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) et fournit le nom canonique du périphérique portable. Si le code du plug-in détermine qu’un travail doit être effectué avec l’appareil connecté, il doit immédiatement retourner \_ la valeur OK à partir de l’appel à **UpdateDevice** avant de continuer le travail. S’il n’y a pas de travail à effectuer, le plug-in doit retourner un code d’erreur.

une fois que le plug-in a terminé d’utiliser l’appareil, il doit appeler [IWMPContentPartnerCallback :: UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) pour notifier Lecteur Windows Media que l’appareil est disponible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation pour les magasins de type 1 en ligne**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




